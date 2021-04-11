---
description: 下表定義可用的字碼頁識別碼。
ms.assetid: 5d6fc86a-f205-4d14-bb7c-ecd71682e0fe
title: 字碼頁識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fb0482247313e8d61d61d7d3178906536ab9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112817"
---
# <a name="code-page-identifiers"></a>字碼頁識別碼

下表定義可用的字碼頁識別碼。

> [!Note]  
> 不同電腦上的 ANSI 字碼頁可能會不同，或可針對單一電腦進行變更，導致資料損毀。 針對最一致的結果，應用程式應該使用 Unicode，例如 UTF-8 或 UTF-16，而不是特定的字碼頁。

 



| 識別碼 | .NET 名稱               | 其他資訊                                                                              |
|------------|-------------------------|-----------------------------------------------------------------------------------------------------|
| 037        | IBM037                  | IBM EBCDIC US-Canada                                                                                |
| 437        | IBM437                  | OEM 美國                                                                                   |
| 500        | IBM500                  | IBM EBCDIC 國際                                                                            |
| 708        | ASMO-708                | 阿拉伯文 (ASMO 708)                                                                                    |
| 709        |                         | 阿拉伯文 (ASMO-449 +、BCON V4)                                                                          |
| 710        |                         | 阿拉伯文-透明阿拉伯文                                                                         |
| 720        | DOS-720                 | 阿拉伯文 (透明 ASMO) ;阿拉伯文 (DOS)                                                              |
| 737        | ibm737                  | OEM 希臘文 (先前 437G) ;希臘文 (DOS)                                                               |
| 775        | ibm775                  | OEM 波羅的海文;波羅的海 (DOS)                                                                             |
| 850        | ibm850                  | OEM 多語系拉丁 1;西歐 (DOS)                                                     |
| 852        | ibm852                  | OEM 拉丁 2;歐洲中部 (DOS)                                                                  |
| 855        | IBM855                  | OEM 斯拉夫 (主要是俄文)                                                                     |
| 857        | ibm857                  | OEM 土耳其文;土耳其文 (DOS)                                                                           |
| 858        | IBM00858                | OEM 多語系拉丁 1 + 歐洲符號                                                              |
| 860        | IBM860                  | OEM 葡萄牙文;葡萄牙文 (DOS)                                                                     |
| 861        | ibm861                  | OEM 冰島文;冰島 (DOS)                                                                       |
| 862        | DOS-862                 | OEM 希伯來文;希伯來文 (DOS)                                                                             |
| 863        | IBM863                  | OEM 法文（加拿大）加拿大法文 (DOS)                                                           |
| 864        | IBM864                  | OEM 阿拉伯文;阿拉伯文 (864)                                                                             |
| 865        | IBM865                  | OEM 北歐;北歐 (DOS)                                                                             |
| 866        | cp866                   | OEM 俄文;斯拉夫 (DOS)                                                                          |
| 869        | ibm869                  | OEM 新式希臘文;希臘文、新式 (DOS)                                                                |
| 870        | IBM870                  | IBM EBCDIC 多語系//ROECE (拉丁 2) ;IBM EBCDIC 多語系拉丁2                            |
| 874        | windows-874             |  (Windows) 的泰語                                                         |
| 875        | cp875                   | IBM EBCDIC 現代希臘文                                                                             |
| 932        | shift-jis \_              | ANSI/OEM 日文;日文 (Shift-jis)                                                              |
| 936        | gb2312                  | ANSI/OEM 簡體中文 (PRC，新加坡) ;簡體中文 (GB2312)                            |
| 949        | ks \_ c \_ 5601-1987        | ANSI/OEM 韓文 (統一的韓文程式碼)                                                                |
| 950        | big5                    |  (臺灣的 ANSI/OEM 繁體中文香港特別行政區、PRC) ;繁體中文 (Big5)                |
| 1026       | IBM1026                 | IBM EBCDIC 土耳其文 (拉丁 5)                                                                         |
| 1047       | IBM01047                | IBM EBCDIC 拉丁 1/開放式系統                                                                      |
| 1140       | IBM01140                | IBM EBCDIC US-Canada (037 + 歐元符號) ;IBM EBCDIC (US-加拿大-歐洲)                                |
| 1141       | IBM01141                | IBM EBCDIC 德國 (20273 + 歐洲符號) ;IBM EBCDIC (德國-歐洲)                                  |
| 1142       | IBM01142                | IBM EBCDIC Denmark-Norway (20277 + 歐元符號) ;IBM EBCDIC (丹麥-挪威-歐洲)                    |
| 1143       | IBM01143                | IBM EBCDIC Finland-Sweden (20278 + 歐元符號) ;IBM EBCDIC (芬蘭-瑞典-歐洲)                    |
| 1144       | IBM01144                | IBM EBCDIC 義大利 (20280 + 歐洲符號) ;IBM EBCDIC (義大利-歐洲)                                      |
| 1145       | IBM01145                | IBM EBCDIC 拉丁 America-Spain (20284 + 歐元符號) ;IBM EBCDIC (西班牙-歐洲)                        |
| 1146       | IBM01146                | IBM EBCDIC 英國 (20285 + 歐洲符號) ;IBM EBCDIC (UK-歐洲)                                |
| 1147       | IBM01147                | IBM EBCDIC 法國 (20297 + 歐洲符號) ;IBM EBCDIC (法國-歐洲)                                    |
| 1148       | IBM01148                | IBM EBCDIC 國際 (500 + 歐洲符號) ;IBM EBCDIC (國際-歐洲)                        |
| 1149       | IBM01149                | IBM EBCDIC 冰島文 (20871 + 歐洲符號) ;IBM EBCDIC (冰島文-歐洲)                              |
| 1200       | utf-16                  | ISO 10646 的 Unicode UTF-16、位元組由小到大位元組順序 (BMP) ;僅適用于受控應用程式 |
| 1201       | unicodeFFFE             | Unicode UTF-16、位元組位元組由大到小的順序;僅適用于受控應用程式                       |
| 1250       | windows-1250            | ANSI 中部歐洲;歐洲中部 (Windows)                                                    |
| 1251       | windows-1251            | ANSI 斯拉夫文; (Windows) 的斯拉夫文                                                                   |
| 1252       | windows-1252            | ANSI 拉丁 1;西歐 (Windows)                                                             |
| 1253       | windows-1253            | ANSI 希臘文;Windows) 的希臘文 (                                                                         |
| 1254       | windows-1254            | ANSI 土耳其文;土耳其文 (Windows)                                                                      |
| 1255       | windows-1255            | ANSI 希伯來文;希伯來文 (Windows)                                                                        |
| 1256       | windows-1256            | ANSI 阿拉伯文;阿拉伯文 (Windows)                                                                        |
| 1257       | windows-1257            | ANSI 波羅的海文;Windows) 的波羅的海文 (                                                                       |
| 1258       | windows-1258            | ANSI/OEM 越南文;越南文 (Windows)                                                            |
| 1361       | Johab                   | 韓文 (Johab)                                                                                       |
| 10000      | Macintosh               | MAC 羅馬;西歐 (Mac)                                                                    |
| 10001      | x-mac-日文          | 日文 (Mac)                                                                                       |
| 10002      | x-mac-chinesetrad       | MAC 繁體中文 (Big5) ;繁體中文 (Mac)                                            |
| 10003      | x-mac-韓文            | 韓文 (Mac)                                                                                        |
| 10004      | x-mac-阿拉伯文            | 阿拉伯文 (Mac)                                                                                         |
| 10005      | x-mac-希伯來文            | 希伯來文 (Mac)                                                                                         |
| 10006      | x-mac-希臘文             | 希臘文 (Mac)                                                                                          |
| 10007      | x-mac-斯拉夫文          |  (Mac) 的斯拉夫                                                                                      |
| 10008      | x-mac-chinesesimp       | MAC 簡體中文 (GB 2312) ;簡體中文 (Mac)                                           |
| 10010      | x-mac-羅馬尼亞文          | 羅馬尼亞 (Mac)                                                                                       |
| 10017      | x-mac-烏克蘭         |  (Mac) 的烏克蘭                                                                                     |
| 10021      | x-mac-泰文              | 泰文 (Mac)                                                                                           |
| 10029      | x-mac-ce                | MAC 拉丁 2;歐洲中部 (Mac)                                                                  |
| 10079      | x-mac-冰島文         | 冰島 (Mac)                                                                                      |
| 10081      | x-mac-土耳其文           | 土耳其 (Mac)                                                                                        |
| 10082      | x-mac-克羅地亞          |  (Mac) 的克羅地亞                                                                                      |
| 12000      | utf-32                  | Unicode UTF-32、位元組由小到小的順序;僅適用于受控應用程式                    |
| 12001      | utf-16 32BE                | Unicode UTF-16 （位元組由大32到小）順序;僅適用于受控應用程式                       |
| 20000      | x-中文 \_ cn          | CN 臺灣;繁體中文 (CN)                                                                |
| 20001      | x-cp20001               | TCA 臺灣                                                                                          |
| 20002      | x \_ 中文-倚天         | 倚天臺灣;繁體中文 (倚天)                                                              |
| 20003      | x-cp20003               | IBM5550 臺灣                                                                                      |
| 20004      | x-cp20004               | TeleText 臺灣                                                                                     |
| 20005      | x-cp20005               | Wang 臺灣                                                                                         |
| 20105      | x-IA5                   | IA5 (IRV 國際字母否。 5、7位) ;西歐 (IA5)                                |
| 20106      | x-IA5-德文            | IA5 德文 (7 位)                                                                                   |
| 20107      | x-IA5-瑞典文           | IA5 瑞典文 (7 位)                                                                                  |
| 20108      | x-IA5-挪威文         | IA5 挪威 (7 位)                                                                                |
| 20127      | 美國-ascii                | US-ASCII (7 位)                                                                                     |
| 20261      | x-cp20261               | T 61                                                                                                |
| 20269      | x-cp20269               | ISO 6937 沒有空格的重音                                                                         |
| 20273      | IBM273                  | IBM EBCDIC 德國                                                                                  |
| 20277      | IBM277                  | IBM EBCDIC Denmark-Norway                                                                           |
| 20278      | IBM278                  | IBM EBCDIC Finland-Sweden                                                                           |
| 20280      | IBM280                  | IBM EBCDIC 義大利                                                                                    |
| 20284      | IBM284                  | IBM EBCDIC 拉丁 America-Spain                                                                      |
| 20285      | IBM285                  | IBM EBCDIC 英國                                                                           |
| 20290      | IBM290                  | IBM EBCDIC 日文片假名擴充                                                               |
| 20297      | IBM297                  | IBM EBCDIC 法國                                                                                   |
| 20420      | IBM420                  | IBM EBCDIC 阿拉伯文                                                                                   |
| 20423      | IBM423                  | IBM EBCDIC 希臘文                                                                                    |
| 20424      | IBM424                  | IBM EBCDIC 希伯來文                                                                                   |
| 20833      | x-EBCDIC-KoreanExtended | IBM EBCDIC 韓文擴充                                                                          |
| 20838      | IBM-Thai                | IBM EBCDIC 泰國                                                                                     |
| 20866      | koi8-r-r                  | 俄文 (KOI8-R-R) ;斯拉夫 (KOI8-R-R)                                                                  |
| 20871      | IBM871                  | IBM EBCDIC 冰島文                                                                                |
| 20880      | IBM880                  | IBM EBCDIC 斯拉夫俄文                                                                         |
| 20905      | IBM905                  | IBM EBCDIC 土耳其文                                                                                  |
| 20924      | IBM00924                | IBM EBCDIC 拉丁 1/Open System (1047 + 歐元符號)                                                  |
| 20932      | EUC-JP                  | 日文 (JIS 0208-1990 和 0212-1990)                                                               |
| 20936      | x-cp20936               | 簡體中文 (GB2312) ;簡體中文 (GB2312-80)                                          |
| 20949      | x-cp20949               | 韓文 Korean-wansung-unicode                                                                                      |
| 21025      | cp1025                  | IBM EBCDIC 斯拉夫 Serbian-Bulgarian                                                               |
| 21027      |                         |  (已淘汰)                                                                                         |
| 21866      | koi8-r-u                  | 烏克蘭 (KOI8-R-U) ;斯拉夫 (KOI8-R-U)                                                                |
| 28591      | iso-8859-1              | ISO 8859-1 拉丁 1;西歐 (ISO)                                                           |
| 28592      | iso-8859-2              | ISO 8859-2 中部歐;歐洲中部 (ISO)                                                  |
| 28593      | iso-8859-3              | ISO 8859-3 拉丁3                                                                                  |
| 28594      | iso-8859-4              | ISO 8859-4 波羅的海文                                                                                   |
| 28595      | iso-8859-5              | ISO 8859-5 斯拉夫語                                                                                 |
| 28596      | iso-8859-6              | ISO 8859-6 阿拉伯文                                                                                   |
| 28597      | iso-8859-7              | ISO 8859-7 希臘文                                                                                    |
| 28598      | iso-8859-8              | ISO 8859-8 希伯來文;希伯來文 (ISO-Visual)                                                               |
| 28599      | iso-8859-9              | ISO 8859-9 土耳其文                                                                                  |
| 28603      | iso-8859-13             | ISO 8859-13 愛沙尼亞文                                                                                |
| 28605      | iso-8859-15             | ISO 8859-15 拉丁9                                                                                 |
| 29001      | x-Europa                | Europa 3                                                                                            |
| 38598      | iso-8859-8-i            | ISO 8859-8 希伯來文;希伯來文 (ISO-邏輯)                                                              |
| 50220      | iso-2022-jp             | ISO 2022 日文（沒有半形片假名）;日文 (JIS)                                         |
| 50221      | csISO2022JP             | ISO 2022 日文（含半形片假名）;日文 (JIS-允許1個位元組的假名)                          |
| 50222      | iso-2022-jp             | ISO 2022 日文 JIS X 0201-1989;日文 (JIS-允許1個位元組的假名-SO/SI)                          |
| 50225      | iso-2022-kr             | ISO 2022 韓文                                                                                     |
| 50227      | x-cp50227               | ISO 2022 簡體中文;簡體中文 (ISO 2022)                                           |
| 50229      |                         | ISO 2022 繁體中文                                                                        |
| 50930      |                         | EBCDIC 日文 (片假名) 擴充                                                                 |
| 50931      |                         | EBCDIC US-Canada 和日文                                                                       |
| 50933      |                         | EBCDIC 韓文擴充和韓文                                                                   |
| 50935      |                         | EBCDIC 簡化中文擴充和簡體中文                                           |
| 50936      |                         | EBCDIC 簡體中文                                                                           |
| 50937      |                         | EBCDIC US-Canada 與繁體中文                                                            |
| 50939      |                         | EBCDIC 日文 (拉丁) 擴充和日文                                                       |
| 51932      | euc-jp                  | EUC 日文                                                                                        |
| 51936      | EUC-CN                  | EUC 簡體中文;簡體中文 (EUC)                                                     |
| 51949      | euc-kr                  | EUC 韓文                                                                                          |
| 51950      |                         | EUC 繁體中文                                                                             |
| 52936      | hz-gb-2312              | HZ-GB2312 簡體中文;簡體中文 (HZ)                                                |
| 54936      | 含                 | **WINDOWS XP 和更新版本：** GB18030 簡體中文 (4 位元組) ;簡體中文 (GB18030)          |
| 57002      | x-iscii-de              | ISCII 梵文                                                                                    |
| 57003      | x-iscii-是              | ISCII 孟加拉國文                                                                                        |
| 57004      | x-iscii-ta              | ISCII 泰米爾                                                                                         |
| 57005      | x-iscii-te              | ISCII 泰泰                                                                                        |
| 57006      | x-iscii-as              | ISCII 阿阿薩姆文                                                                                      |
| 57007      | x-iscii 或              | ISCII 奧裡亞                                                                                          |
| 57008      | x-iscii-ka              | ISCII 埃德文                                                                                       |
| 57009      | x-iscii-ma              | ISCII 馬拉雅德                                                                                     |
| 57010      | x-iscii-gu              | ISCII 古文                                                                                      |
| 57011      | x-iscii-pa              | ISCII 旁遮普文                                                                                       |
| 65000      | utf-7                   | Unicode (UTF-7)                                                                                      |
| 65001      | utf-8                   | Unicode (UTF-8)                                                                                     |



 

 

 



