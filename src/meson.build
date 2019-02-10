uchardet_src = files(
    'CharDistribution.cpp',
    'JpCntx.cpp',
    'LangModels/LangArabicModel.cpp',
    'LangModels/LangBulgarianModel.cpp',
    'LangModels/LangCroatianModel.cpp',
    'LangModels/LangCzechModel.cpp',
    'LangModels/LangEsperantoModel.cpp',
    'LangModels/LangEstonianModel.cpp',
    'LangModels/LangFinnishModel.cpp',
    'LangModels/LangFrenchModel.cpp',
    'LangModels/LangDanishModel.cpp',
    'LangModels/LangGermanModel.cpp',
    'LangModels/LangGreekModel.cpp',
    'LangModels/LangHungarianModel.cpp',
    'LangModels/LangHebrewModel.cpp',
    'LangModels/LangIrishModel.cpp',
    'LangModels/LangItalianModel.cpp',
    'LangModels/LangLithuanianModel.cpp',
    'LangModels/LangLatvianModel.cpp',
    'LangModels/LangMalteseModel.cpp',
    'LangModels/LangPolishModel.cpp',
    'LangModels/LangPortugueseModel.cpp',
    'LangModels/LangRomanianModel.cpp',
    'LangModels/LangRussianModel.cpp',
    'LangModels/LangSlovakModel.cpp',
    'LangModels/LangSloveneModel.cpp',
    'LangModels/LangSwedishModel.cpp',
    'LangModels/LangSpanishModel.cpp',
    'LangModels/LangThaiModel.cpp',
    'LangModels/LangTurkishModel.cpp',
    'LangModels/LangVietnameseModel.cpp',
    'nsHebrewProber.cpp',
    'nsCharSetProber.cpp',
    'nsBig5Prober.cpp',
    'nsEUCJPProber.cpp',
    'nsEUCKRProber.cpp',
    'nsEUCTWProber.cpp',
    'nsEscCharsetProber.cpp',
    'nsEscSM.cpp',
    'nsGB2312Prober.cpp',
    'nsMBCSGroupProber.cpp',
    'nsMBCSSM.cpp',
    'nsSBCSGroupProber.cpp',
    'nsSBCharSetProber.cpp',
    'nsSJISProber.cpp',
    'nsUTF8Prober.cpp',
    'nsLatin1Prober.cpp',
    'nsUniversalDetector.cpp',
    'uchardet.cpp'
)
uchardet_headers = files('uchardet.h')

uchardet = library('uchardet', uchardet_src, install: true)

uchardet_dep = declare_dependency(link_with: uchardet)

install_headers(uchardet_headers, subdir: meson.project_name())

if get_option('build-binary')
    #subdir('tools')
endif
