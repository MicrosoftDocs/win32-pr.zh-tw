---
title: StringFileInfo BLOCK 語句
description: 描述字串資訊區塊的格式。
ms.assetid: d5edf638-b70a-44d0-a43a-89d4d21e679f
keywords:
- StringFileInfo 區塊語句功能表和其他資源
topic_type:
- apiref
api_name:
- StringFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb0a1c5e7a2fd5e3d2f096c882ca928ce1febf92
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373088"
---
# <a name="stringfileinfo-block-statement"></a>StringFileInfo BLOCK 語句

定義字串資訊區塊。

``` syntax
BLOCK "StringFileInfo" { BLOCK "lang-charset" {VALUE "string-name", "value" . . . }}
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lang-charset"></span><span id="LANG-CHARSET"></span>*lang-字元集*
</dt> <dd>

語言和字元集識別碼組。 它是由 [備註] 區段中指定的語言和字元集識別碼串連所組成的十六進位字串。

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*字串名稱*
</dt> <dd>

區塊中值的名稱，可以是 [備註] 區段中指定的其中一個預先定義名稱。

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*價值*
</dt> <dd>

指定對應字串名稱值的字元字串。 您可以指定一個以上的 **VALUE** 語句。

</dd> </dl>

## <a name="remarks"></a>備註

*Lang-字元集* 參數會指定下列其中一種語言代碼。



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



 

*Lang-字元集* 參數也會指定下列其中一個字元集識別碼。



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



 

*字串名稱* 參數會指定下列其中一個預先定義的名稱。



| Name                 | 描述                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **註解**         | 為了診斷而應顯示的其他資訊。                                                                                                                                                                                                                                    |
| **CompanyName**      | 產生檔案的公司，例如「Microsoft Corporation」或「標準 Microsystems Corporation，Inc.」。 這個字串是必要的。                                                                                                                                                                   |
| **FileDescription**  | 要呈現給使用者的檔案描述。 當使用者選擇要安裝的檔案時，這個字串可能會顯示在清單方塊中，例如「AT-Style 鍵盤的鍵盤驅動程式」。 這個字串是必要的。                                                                                            |
| **FileVersion**      | 檔案的版本號碼，例如 "3.10" 或 "5.00. RC2"。 這個字串是必要的。                                                                                                                                                                                                                      |
| **InternalName**     | 檔案的內部名稱（如果有的話），例如，如果檔案是動態連結程式庫，則為模組名稱。 如果檔案沒有內部名稱，此字串應該是不含副檔名的原始檔案名。 這個字串是必要的。                                                                       |
| **LegalCopyright**   | 適用于檔案的著作權注意事項。 這應該包含所有通知、法律符號、著作權日期等的完整文字。 這個字串是選擇性的。                                                                                                                                             |
| **LegalTrademarks**  | 適用于檔案的商標及注冊商標。 這應包括所有注意事項全文、法律符號、商標登錄編號等等。 這個字串是選擇性的。                                                                                                                        |
| **OriginalFilename** | 檔案的原始名稱，不包含路徑。 這項資訊可讓應用程式判斷使用者是否已重新命名檔案。 名稱的格式取決於建立檔案的檔案系統。 這個字串是必要的。                                                 |
| **PrivateBuild**     | 檔案私用版本的相關資訊，例如「在 TESTBED 上由 TESTER1 建立」 \\ 。 只有當 **VS \_ FF \_ PRI加值稅EBUILD** 是在根區塊的 *fileflags 機碼* 參數中指定時，才會出現這個字串。                                                                                   |
| **ProductName**      | 用來散發檔案的產品名稱。 這個字串是必要的。                                                                                                                                                                                                                            |
| **ProductVersion**   | 散發檔案時所使用的產品版本，例如 "3.10" 或 "5.00. RC2"。 這個字串是必要的。                                                                                                                                                                                       |
| **SpecialBuild**     | 指定這個檔案版本與標準版本之差異的文字（例如「TESTER1 在 M250 和 M250E 電腦上解決滑鼠問題的私用組建」）。 只有當 **VS \_ FF \_ SPECIALBUILD** 是在根區塊的 *fileflags 機碼* 參數中指定時，才會出現這個字串。 |



 

 

 




