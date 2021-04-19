---
description: 地區設定 \_ SSCRIPTS
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970841"
---
# <a name="locale_sscripts"></a>地區設定 \_ SSCRIPTS

**Windows Vista 和更新版本：** 字串，代表腳本清單（使用 [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html)中使用的4個字元標記法）。 每個腳本名稱都是由四個拉丁字元所組成，且清單會依字母順序排列，並以每個名稱（包括最後）和分號。

您可以呼叫 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)或 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) ，並將 *LCType* 設定為 LOCALE \_ SSCRIPTS，作為策略的一部分，以降低 (IDNs) 的國際化功能變數名稱相關的安全性問題。 以下是一些範例值：



| Locale                  | 地區設定/語言名稱 | 值                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| 英文 (美國) | zh-TW                | Latn;                                                                                                  |
| 印度文 (印度)           | hi-IN                | Deva;                                                                                                  |
| 日文 (日本)        | ja-JP                | **Windows 7 和更新版本：** Hani;Hira;Jpan;區分<br/> **Windows Vista：** Hani;Hira;區分<br/> |



 

複合腳本值不包含拉丁腳本，除非它是用於特定地區設定之書寫系統的必要部分。 拉丁字元通常用於不是原生的地區設定內容，例如外部商務名稱。 在上述範例中，印度文的印度文中，唯一的腳本值為 "Deva" ("梵文" ) ，不過拉丁字元也可以出現在印度文文字中。 [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)函式具有特殊旗標，可解決此案例。

 

 




