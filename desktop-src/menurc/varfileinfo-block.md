---
title: VarFileInfo BLOCK 語句
description: 描述變數資訊區塊的格式。
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- VarFileInfo 區塊語句功能表和其他資源
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15b4bf57a14d6bae6dd5b83c8ea86e38830113fbcfbbaa27b143bf02bb130e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846968"
---
# <a name="varfileinfo-block-statement"></a>VarFileInfo BLOCK 語句

定義變數資訊區塊。

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

[備註] 區段中指定的其中一個語言識別項。

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

在 [備註] 區段中指定的其中一個字元組識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

您可以指定一個以上的識別碼組，但每一組都必須以逗號分隔。

*LangID* 參數會指定下列其中一種語言代碼。



| 程式碼   | 語言            | 程式碼   | 語言                  |
|--------|---------------------|--------|---------------------------|
| 0x0401 | 阿拉伯文              | 0x0415 | 波蘭文                    |
| 0x0402 | 保加利亞文           | 0x0416 | 葡萄牙文 (巴西)       |
| 0x0403 | 卡達隆尼亞文             | 0x0417 | Rhaeto-Romanic            |
| 0x0404 | 繁體中文 | 0x0418 | 羅馬尼亞文                  |
| 0x0405 | 捷克文               | 0x0419 | 俄文                   |
| 0x0406 | 丹麥文              | 0x041A | Croato-Serbian (拉丁)     |
| 0x0407 | 德文              | 0x041B | 斯洛伐克文                    |
| 0x0408 | 希臘文               | 0x041C | 阿爾巴尼亞文                  |
| 0x0409 | 美式英文        | 0x041D | 瑞典文                   |
| 0x040A | 標準西班牙文   | 0x041E | 泰文                      |
| 0x040B | 芬蘭文             | 0x041F | 土耳其文                   |
| 0x040C | 法文              | 0x0420 | 烏都文                      |
| 0x040D | Hebrew              | 0x0421 | Bahasa                    |
| 0x040E | 匈牙利文           | 0x0804 | 簡體中文        |
| 0x040F | 冰島文           | 0x0807 | 瑞士德文              |
| 0x0410 | 義大利文             | 0x0809 | 英國。 英文              |
| 0x0411 | 日文            | 0x080A | 西班牙文 (墨西哥)          |
| 0x0412 | 韓文              | 0x080C | 比利時法文            |
| 0x0413 | 荷蘭文               | 0x0C0C | 法文 (加拿大)           |
| 0x0414 | 挪威文–博克瑪律  | 0x100C | 瑞士法文              |
| 0x0810 | 瑞士義大利文       | 0x0816 | 葡萄牙文 (葡萄牙)     |
| 0x0813 | 比利時荷蘭文       | 0x081A | Serbo-Croatian (斯拉夫)  |
| 0x0814 | 挪威文–挪威文 | ?      | ?                         |



 

*CharsetID* 參數會指定下列其中一個字元集識別碼：



| 識別碼 | 字元集              |
|------------|----------------------------|
| 0          | 7位 ASCII                |
| 932        | 日本 (Shift – JIS X-0208)  |
| 949        | 韓國 (Shift – KSC 5601)    |
| 950        | 臺灣 (Big5)               |
| 1200       | Unicode                    |
| 1250       | 拉丁美洲 (東部歐洲)  |
| 1251       | 古斯拉夫文                   |
| 1252       | 多 語種               |
| 1253       | 希臘文                      |
| 1254       | 土耳其文                    |
| 1255       | Hebrew                     |
| 1256       | 阿拉伯文                     |



 

 

 




