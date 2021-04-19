---
description: 字碼頁位欄位用於 FONTSIGNATURE 和 LOCALESIGNATURE 結構中。注意：所有地區設定都不支援字碼頁。
ms.assetid: 830b1a88-cb0c-4719-b857-4cc2cd67dd5d
title: 字碼頁位欄位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f9df44ac14d935a026a10ab1e71eb7378840de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986416"
---
# <a name="code-page-bitfields"></a>字碼頁位欄位

字碼頁位欄位用於 [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) 和 [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) 結構中。

> [!Note]  
> 所有地區設定都不支援字碼頁。 本主題所述的位欄位不適用於 Unicode 地區設定。 若要判斷地區設定所支援的腳本，您的應用程式可以使用地區設定識別碼常數 [地區設定 \_ SSCRIPTS](locale-sscripts.md) 與 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)。

 

> [!Note]  
> 字碼頁位中有位存在，不一定表示地區設定的所有字串都可以在該字碼頁中進行編碼，而不會遺失。 若要保留資料而不遺失，建議使用 Unicode UTF-8 或 UTF-16。

 



| bit          | 字碼頁 | Description                                           |
|--------------|-----------|-------------------------------------------------------|
| ANSI         |           |                                                       |
| 0            | 1252      | 拉丁文1                                               |
| 1            | 1250      | 拉丁文2：歐洲中部                               |
| 2            | 1251      | 古斯拉夫文                                              |
| 3            | 1253      | 希臘文                                                 |
| 4            | 1254      | 土耳其文                                               |
| 5            | 1255      | Hebrew                                                |
| 6            | 1256      | 阿拉伯文                                                |
| 7            | 1257      | 波羅的語系                                                |
| 8            | 1258      | 越南文                                            |
| 9 - 15       |           | 保留給 ANSI                                     |
| ANSI 和 OEM |           |                                                       |
| 16           | 874       | 泰文                                                  |
| 17           | 932       | 日文，Shift-JIS                                   |
| 18           | 936       | 簡體中文 (PRC，新加坡)                    |
| 19           | 949       | 韓文統一的韓文程式碼 (韓文 TongHabHyung 程式碼)  |
| 20           | 950       | 繁體中文 (臺灣;香港特別行政區、PRC)       |
| 21           | 1361      | 韓文 (Johab)                                         |
| 22 - 29      |           | 保留給替代的 ANSI 和 OEM                   |
| 30 - 31      |           | 由系統所保留。                                   |
| OEM          |           |                                                       |
| 32-46      |           | 保留給 OEM                                      |
| 47           | 1258      | 越南文                                            |
| 48           | 869       | 新式希臘文                                          |
| 49           | 866       | 俄文                                               |
| 50           | 865       | 北歐                                                |
| 51           | 864       | 阿拉伯文                                                |
| 52           | 863       | 法文 (加拿大)                                       |
| 53           | 862       |                                                       |
| 54           | 861       | 冰島文                                             |
| 55           | 860       | 葡萄牙文                                            |
| 56           | 857       | 土耳其文                                               |
| 57           | 855       | 克主要是俄文                           |
| 58           | 852       | 拉丁2                                               |
| 59           | 775       | 波羅的語系                                                |
| 60           | 737       | 希臘文先前437G                                  |
| 61           | 708;720  | 帶ASMO 708                                      |
| 62           | 850       | 多語系拉丁1                                  |
| 63           | 437       | US                                                    |



 

 

 



