all: buildWholeGenome build2ndLevelIndex extractTranscriptSeq extractSJfromGTF GTF2GAF

OPTFLAGS = -O0 -g -rdynamic -std=c++0x
OUTPUTDIR = ./

CFLAGS += $(OPTFLAGS) -fopenmp

buildIndex:
	g++  $(CFLAGS) -o $(OUTPUTDIR)buildIndex src/buildIndex.cpp
	g++  $(CFLAGS) -o $(OUTPUTDIR)buildWholeGenome src/buildGlobalAndLocalIndex/buildWholeGenomeIndex.cpp
	g++  $(CFLAGS) -o $(OUTPUTDIR)buildWholeGenome_mergedFa src/buildGlobalAndLocalIndex/buildWholeGenomeIndex_mergedFa.cpp
	g++  $(CFLAGS) -o $(OUTPUTDIR)build2ndLevelIndex src/buildGlobalAndLocalIndex/buildAll2ndLevelIndex.cpp

buildWholeGenome:
	g++  $(CFLAGS) -o $(OUTPUTDIR)buildWholeGenome src/buildGlobalAndLocalIndex/buildWholeGenomeIndex.cpp
buildWholeGenome_mergedFa:
	g++  $(CFLAGS) -o $(OUTPUTDIR)buildWholeGenome_mergedFa src/buildGlobalAndLocalIndex/buildWholeGenomeIndex_mergedFa.cpp
buildWholeGenome_mergedFa_noPreIndex:
	g++  $(CFLAGS) -o $(OUTPUTDIR)buildWholeGenome_mergedFa_noPreIndex src/buildGlobalAndLocalIndex/buildWholeGenomeIndex_mergedFa_noPreIndex.cpp	
buildWholeGenome_mergedFa_noPreIndex_varyLineNumPerFa:
	g++  $(CFLAGS) -o $(OUTPUTDIR)buildWholeGenome_mergedFa_noPreIndex_varyLineNumPerFa src/buildGlobalAndLocalIndex/buildWholeGenomeIndex_mergedFa_noPreIndex_varyLineNumPerFa.cpp
build2ndLevelIndex:
	g++  $(CFLAGS) -o $(OUTPUTDIR)build2ndLevelIndex src/buildGlobalAndLocalIndex/buildAll2ndLevelIndex.cpp
extractTranscriptSeq:
	g++  $(CFLAGS) -o $(OUTPUTDIR)extractTranscriptSeq src/extractTranscriptSeq/retrieveTranscriptSeq.cpp
extractSJfromGTF:
	g++  $(CFLAGS) -o $(OUTPUTDIR)extractSJfromGTF src/extractSJfromAnnotation/extractSJfromGTF.cpp
extractSJfromGTF_strand:
	g++  $(CFLAGS) -o $(OUTPUTDIR)extractSJfromGTF_strand src/extractSJfromAnnotation/extractSJfromGTF_strand.cpp
GTF2GAF:
	g++  $(CFLAGS) -o $(OUTPUTDIR)GTF2GAF src/Converter/convertGTF2GAF.cpp
Beers2GTF:
	g++  $(CFLAGS) -o $(OUTPUTDIR)Beers2GTF src/Converter/convertBeersTranscriptInfo2GTF.cpp
MPS3junc2HISATjunc:
	g++ $(CFLAGS) -o $(OUTPUTDIR)MPS3junc2HISATjunc src/Converter/convertMPS3juncToHISATjunc.cpp
HISATjunc2STARjunc:
	g++ $(CFLAGS) -o $(OUTPUTDIR)HISATjunc2STARjunc src/Converter/convertHISATjuncToSTARjunc.cpp
BeersGTF2GSNAPgtf:
	g++ $(CFLAGS) -o $(OUTPUTDIR)BeersGTF2GSNAPgtf src/Converter/convertBeersGTF2GSNAPformat_addGeneIDandTranscriptID.cpp
#separateMergedChromFile:
#	g++ $(CFLAGS) -o $(OUTPUTDIR)separateMergedChromFile src/utils/separateMergedChromFile.cpp

clean_buildIndex:
	rm $(OUTPUTDIR)buildIndex
	rm $(OUTPUTDIR)buildWholeGenome
	rm $(OUTPUTDIR)buildWholeGenome_mergedFa
	rm $(OUTPUTDIR)build2ndLevelIndex

clean:
	rm $(OUTPUTDIR)buildWholeGenome
	rm $(OUTPUTDIR)build2ndLevelIndex
	rm $(OUTPUTDIR)extractTranscriptSeq
	rm $(OUTPUTDIR)extractSJfromGTF
	rm $(OUTPUTDIR)GTF2GAF
clean_extractTranscriptSeq:
	rm $(OUTPUTDIR)extractTranscriptSeq
clean_extractSJfromGTF:
	rm $(OUTPUTDIR)extractSJfromGTF
clean_extractSJfromGTF_strand:
	rm $(OUTPUTDIR)extractSJfromGTF_strand
clean_GTF2GAF:
	rm $(OUTPUTDIR)GTF2GAF
clean_Beers2GTF:
	rm $(OUTPUTDIR)Beers2GTF
clean_MPS3junc2HISATjunc:
	rm $(OUTPUTDIR)MPS3junc2HISATjunc
clean_HISATjunc2STARjunc:
	rm $(OUTPUTDIR)HISATjunc2STARjunc
clean_BeersGTF2GSNAPgtf:
	rm $(OUTPUTDIR)BeersGTF2GSNAPgtf
clean_buildWholeGenome_mergedFa:
	rm $(OUTPUTDIR)buildWholeGenome_mergedFa
clean_buildWholeGenome_mergedFa_noPreIndex:
	rm $(OUTPUTDIR)buildWholeGenome_mergedFa_noPreIndex
#clean_separateMergedChromFile:
#	rm $(OUTPUTDIR)separateMergedChromFile
