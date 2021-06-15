## This program is free software: you can redistribute it and/or modify
## it under the terms of the GNU General Public License as published by
## the Free Software Foundation, version 3 of the License.

## This program is distributed in the hope that it will be useful,
## but WITHOUT ANY WARRANTY; without even the implied warranty of
## MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
## GNU General Public License for more details.

## You should have received a copy of the GNU General Public License
## along with this program.  If not, see <http://www.gnu.org/licenses/>.

LANG1=fin
LANG2=olo
PREFIX1=$(LANG1)-$(LANG2)
PREFIX2=$(LANG2)-$(LANG1)

BASENAME=apertium-$(PREFIX1)


## apevis gh-pages
if CAN_SAXON
LANG1HTML=Finnish
LANG2HTML=Karelian

noinst_DATA=$(BASENAME).$(PREFIX1).dix.html \
			$(BASENAME).$(PREFIX2).dix.html \
			$(BASENAME).$(PREFIX1).t1x.html \
			$(BASENAME).$(PREFIX1).t2x.html \
			$(BASENAME).$(PREFIX1).t3x.html \
			$(BASENAME).$(PREFIX2).t1x.html \
			$(BASENAME).$(PREFIX2).t2x.html \
			$(BASENAME).$(PREFIX2).t3x.html \
			statistics.html

bidix2html-split.xslt:
	wget https://raw.githubusercontent.com/flammie/apevis-xslt/master/$@

bidix2html.xslt:
	wget https://raw.githubusercontent.com/flammie/apevis-xslt/master/$@

tix2html.xslt:
	wget https://raw.githubusercontent.com/flammie/apevis-xslt/master/$@

dix2stats.xslt:
	wget https://raw.githubusercontent.com/flammie/apevis-xslt/master/$@

$(BASENAME).$(PREFIX1).dix.html: $(top_srcdir)/$(BASENAME).$(PREFIX1).dix bidix2html.xslt
	$(SAXON) -s:$< bidix2html.xslt from=$(LANG1HTML) to=$(LANG2HTML) pair=$(PREFIX1) antipair=$(PREFIX2) > $@

$(BASENAME).$(PREFIX2).dix.html: $(top_srcdir)/$(BASENAME).$(PREFIX1).dix bidix2html.xslt
	$(SAXON) -s:$< bidix2html.xslt from=$(LANG2HTML) to=$(LANG1HTML) pair=$(PREFIX1) antipair=$(PREFIX2)  invert=true > $@

$(BASENAME).$(PREFIX1).t1x.html: $(top_srcdir)/$(BASENAME).$(PREFIX1).t1x tix2html.xslt
	$(SAXON) -s:$< tix2html.xslt from=$(LANG1HTML) to=$(LANG2HTML) pair=$(PREFIX2) antipair=$(PREFIX1)  > $@

$(BASENAME).$(PREFIX1).t2x.html: $(top_srcdir)/$(BASENAME).$(PREFIX1).t2x tix2html.xslt
	$(SAXON) -s:$< tix2html.xslt  from=$(LANG1HTML) to=$(LANG2HTML) pair=$(PREFIX2) antipair=$(PREFIX1)  > $@

$(BASENAME).$(PREFIX1).t3x.html: $(top_srcdir)/$(BASENAME).$(PREFIX1).t3x tix2html.xslt
	$(SAXON) -s:$< tix2html.xslt  from=$(LANG1HTML) to=$(LANG2HTML) pair=$(PREFIX2) antipair=$(PREFIX1)  > $@

$(BASENAME).$(PREFIX2).t1x.html: $(top_srcdir)/$(BASENAME).$(PREFIX2).t1x tix2html.xslt
	$(SAXON) -s:$< tix2html.xslt from=$(LANG1HTML) to=$(LANG2HTML) pair=$(PREFIX1) antipair=$(PREFIX2)  > $@

$(BASENAME).$(PREFIX2).t2x.html: $(top_srcdir)/$(BASENAME).$(PREFIX2).t2x tix2html.xslt
	$(SAXON) -s:$< tix2html.xslt  from=$(LANG1HTML) to=$(LANG2HTML) pair=$(PREFIX1) antipair=$(PREFIX2)  > $@

$(BASENAME).$(PREFIX2).t3x.html: $(top_srcdir)/$(BASENAME).$(PREFIX2).t3x tix2html.xslt
	$(SAXON) -s:$< tix2html.xslt  from=$(LANG1HTML) to=$(LANG2HTML) pair=$(PREFIX1) antipair=$(PREFIX2)  > $@

stats-$(BASENAME).$(PREFIX1).dix.html: $(top_srcdir)/$(BASENAME).$(PREFIX1).dix dix2stats.xslt
	$(SAXON) -s:$< dix2stats.xslt > $@

stats-$(BASENAME).$(PREFIX1).t1x.html: $(top_srcdir)/$(BASENAME).$(PREFIX1).t1x dix2stats.xslt
	$(SAXON) -s:$< dix2stats.xslt > $@

stats-$(BASENAME).$(PREFIX1).t2x.html: $(top_srcdir)/$(BASENAME).$(PREFIX1).t2x dix2stats.xslt
	$(SAXON) -s:$< dix2stats.xslt > $@

stats-$(BASENAME).$(PREFIX1).t3x.html: $(top_srcdir)/$(BASENAME).$(PREFIX1).t3x dix2stats.xslt
	$(SAXON) -s:$< dix2stats.xslt > $@

stats-$(BASENAME).$(PREFIX2).t1x.html: $(top_srcdir)/$(BASENAME).$(PREFIX2).t1x dix2stats.xslt
	$(SAXON) -s:$< dix2stats.xslt > $@

stats-$(BASENAME).$(PREFIX2).t2x.html: $(top_srcdir)/$(BASENAME).$(PREFIX2).t2x dix2stats.xslt
	$(SAXON) -s:$< dix2stats.xslt > $@

stats-$(BASENAME).$(PREFIX2).t3x.html: $(top_srcdir)/$(BASENAME).$(PREFIX2).t3x dix2stats.xslt
	$(SAXON) -s:$< dix2stats.xslt > $@

statistics.html: stats-$(BASENAME).$(PREFIX1).dix.html \
				 stats-$(BASENAME).$(PREFIX1).t1x.html \
				 stats-$(BASENAME).$(PREFIX2).t1x.html \
				 stats-$(BASENAME).$(PREFIX1).t2x.html \
				 stats-$(BASENAME).$(PREFIX2).t2x.html \
				 stats-$(BASENAME).$(PREFIX1).t3x.html \
				 stats-$(BASENAME).$(PREFIX2).t3x.html
	$(AWK) '/DOCTYPE/,/<\/h1>/ {print;}' < \
		stats-$(BASENAME).$(PREFIX1).dix.html > $@
	$(AWK) '/<h2>/,/<\/div>/ {print;}' < \
		stats-$(BASENAME).$(PREFIX1).dix.html | fgrep -v '</div>' >> $@
	$(AWK) '/<h2>/,/<\/div>/ {print;}' < \
		stats-$(BASENAME).$(PREFIX1).t1x.html | fgrep -v '</div>' >> $@
	$(AWK) '/<h2>/,/<\/div>/ {print;}' < \
		stats-$(BASENAME).$(PREFIX1).t2x.html | fgrep -v '</div>' >> $@
	$(AWK) '/<h2>/,/<\/div>/ {print;}' < \
		stats-$(BASENAME).$(PREFIX1).t3x.html | fgrep -v '</div>' >> $@
	$(AWK) '/<h2>/,/<\/div>/ {print;}' < \
		stats-$(BASENAME).$(PREFIX2).t1x.html | fgrep -v '</div>' >> $@
	$(AWK) '/<h2>/,/<\/div>/ {print;}' < \
		stats-$(BASENAME).$(PREFIX2).t2x.html | fgrep -v '</div>' >> $@
	$(AWK) '/<h2>/,/<\/div>/ {print;}' < \
		stats-$(BASENAME).$(PREFIX2).t3x.html | fgrep -v '</div>' >> $@
	echo '</div><div class="row">' >> $@
	$(AWK) '/<div id="footer"/,/<\/html/ {print;}' < \
		stats-$(BASENAME).$(PREFIX1).dix.html | fgrep -v '</div>' >> $@

endif

