---
description: Microsoft Windows 軟體開發套件 (SDK) 包含當地語系化的資源字串、當地語系化的錯誤資料表，以及下表所列語言的當地語系化 ActionText 資料表。
ms.assetid: 2e3a6e73-5b06-452d-9f87-18eb6914b961
title: 將錯誤和 ActionText 表當地語系化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1839141b80afd1d28aa9e9317da10d79aea41232f9e7ebde0db7971d22f5141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629463"
---
# <a name="localizing-the-error-and-actiontext-tables"></a>將錯誤和 ActionText 表當地語系化

Microsoft Windows 軟體開發套件 (SDK) 包含當地語系化的資源字串、當地語系化的[錯誤資料表](error-table.md)，以及下表所列語言的當地語系化[ActionText 資料表](actiontext-table.md)。 以星號標示的 Langid 會指出資源字串會儲存為基底語言，因此可搭配該語言的所有方言使用。

您可以使用 Msidb.exe 或 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)，將當地語系化的錯誤和 ActionText 資料表匯入資料庫中。



| LANGID (decimal)  | LANGID (十六進位)  | ASCII 字碼頁 | 縮寫 | 語言                      | Language-Culture |
|------------------|----------------------|-----------------|--------------|-------------------------------|------------------|
| 1025\*           | 0x401                | 1256            | ARA          | 阿拉伯文 - 沙烏地阿拉伯         | ar-SA            |
| 1027             | 0x403                | 1252            | 貓          | 卡達隆尼亞文                       | ca-ES            |
| 1028\*           | 0x404                | 950             | CHT          | 繁體中文 - 台灣              | zh-TW            |
| 2052             | 0x804                | 936             | CHS          | 簡體中文 - 中國               | zh-CN            |
| 1029             | 0x405                | 1250            | CSY          | 捷克文-捷克共和國        | cs-CZ            |
| 1030             | 0x406                | 1252            | DAN          | 丹麥文-丹麥               | da-DK            |
| 1031\*           | 0x407                | 1252            | DEU          | 德文 (德國)              | de-DE            |
| 1032             | 0x408                | 1253            | ELL          | 希臘文-希臘                | el-GR            |
| 1033\*           | 0x409                | 1252            | ENU          | Chinese - Taiwan       | en-US            |
| 3082\*           | 0xC0A                | 1252            | ESN          | 西班牙文-新式排序-西班牙 | es-ES            |
| 1061             | 0x425                | 1257            | ETI          | 愛沙尼亞文                      | et-EE            |
| 1035             | 0x40B                | 1252            | FIN          | 芬蘭文-芬蘭             | fi-FI            |
| 1036\*           | 0x40C                | 1252            | FRA          | 法文 (法國)               | fr-FR            |
| 1037             | 0x40D                | 1255            | HEB          | 希伯來文-以色列               | he-IL            |
| 1038             | 0x40E                | 1250            | HUN          | 匈牙利文-匈牙利           | hu-HU            |
| 1040\*           | 0x410                | 1252            | ITA          | 義大利文 - 義大利               | it-IT            |
| 1041             | 0x411                | 932             | JPN          | 日文 (日本)              | jp-JP            |
| 1042             | 0x412                | 949             | KOR          | 韓文 (韓國)                | ko-KO            |
| 1063             | 0x427                | 1257            | LTH          | 立陶宛文                    | lt-LT            |
| 1062             | 0x426                | 1257            | LVI          | 拉脫維亞文                       | lv-LV            |
| 1043\*           | 0x413                | 1252            | NLD          | 荷蘭文 - 荷蘭           | nl-NL            |
| 1044\*           | 0x414                | 1252            | NOR          | 挪威文 (博克) -挪威    | nb-NO            |
| 1045             | 0x415                | 1250            | PLK          | 波蘭文 - 波蘭                | pl-PL            |
| 1046             | 0x416                | 1252            | PTB          | 葡萄牙文 - 巴西           | pt-BR            |
| 2070             | 0x816                | 1252            | PTG          | 葡萄牙文 - 葡萄牙         | pt-PT            |
| 1048             | 0x418                | 1250            | 羅          | 羅馬尼亞文-羅馬尼亞            | ro-RO            |
| 1049             | 0x419                | 1251            | RUS          | 俄文 - 俄羅斯              | ru-RU            |
| 1050             | 0x41A                | 1250            | HRV          | 克羅地亞語-克羅地亞            | hr-HR            |
| 1051             | 0x41B                | 1250            | 天空          | 斯洛伐克文-斯洛伐克             | sk-SK            |
| 1053\*           | 0x41D                | 1252            | SVE          | 瑞典文-瑞典              | sv-SE            |
| 1054             | 0x41E                | 874             | THA          | 泰文-泰國               | th-TH            |
| 1055             | 0x41F                | 1254            | TRK          | 土耳其文-土耳其              | tr-TR            |
| 1060             | 0x424                | 1250            | SLV          | 斯洛維尼亞文-斯洛維尼亞          | sl-SI            |
| 1066             | 0x42A                | 1258            | 維生素          | 越南文-越南         | vi-VN            |
| 1069             | 0x42D                | 1252            | EUQ          | 巴斯克文 (巴斯克文)               | eu-ES            |



 

**Windows Vista：** 除了上表所列的語言之外，下表中的語言也可以從 Windows Vista 開始使用。



| LANGID (decimal)  | LANGID (十六進位)  | ASCII 字碼頁 | 縮寫 | 語言        | Language-Culture |
|------------------|----------------------|-----------------|--------------|-----------------|------------------|
| 1026             | 0x402                | 1251            | BGR          | 保加利亞文       | bg-BG            |
| 1058             | 0x422                | 1251            | UKR          | 烏克蘭文       | uk-UA            |
| 2074             | 0x81A                | 1250            | SRL          | 塞爾維亞文 (拉丁) | sr-Latn-CS       |



 

 

 



