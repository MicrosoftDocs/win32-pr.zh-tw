---
title: VERSIONINFO 資源
description: 定義版本資訊資源。 資源包含檔案的相關資訊，例如其版本號碼、其預定的作業系統，以及其原始檔案名。 此資源適用于版本資訊功能。
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- VERSIONINFO 資源功能表與其他資源
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9248abe18d07820ebefaa6d939f36f617f6cd07f
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "104316717"
---
# <a name="versioninfo-resource"></a>VERSIONINFO 資源

定義版本資訊資源。 資源包含檔案的相關資訊，例如其版本號碼、其預定的作業系統，以及其原始檔案名。 此資源適用于 [版本資訊](./version-information.md) 功能。

有兩種方式可將 **VERSIONINFO** 語句格式化：

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

\- 或 -

``` syntax
versionID VERSIONINFO 
fixed-info
BEGIN
block-statement
. . .
END
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*
</dt> <dd>

版本資訊資源識別碼。 此值必須是1。

</dd> <dt>

<span id="fixed-info"></span><span id="FIXED-INFO"></span>*固定資訊*
</dt> <dd>

版本資訊，例如檔案版本和預定的作業系統。 這個參數是由下列語句所組成。



| 陳述式                         | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FILEVERSION** *版本*         | 檔案的二進位版本號碼。 *版本* 是由 4 16 位整數所定義的 2 32 位整數所組成。 例如，"FILEVERSION 3，10，0，61" 會以該順序轉譯成兩個雙字：0x0003000a 和0x0000003d。 因此，如果 *version* 是由 **DWORD** 值 *dw1* 和 *dw2* 所定義，則它們必須出現在 **FILEVERSION** 語句中，如下所示：、 `HIWORD(dw1)` `LOWORD(dw1)` 、 `HIWORD(dw2)` 、 `LOWORD(dw2)` 。 |
| **PRODUCTVERSION** *版本*      | 用來散發檔案的產品二進位版本號碼。 *Version* 參數是 2 32 位整數，由 4 16 位整數所定義。 如需 *版本* 的詳細資訊，請參閱 **FILEVERSION** 描述。                                                                                                                                                                                                           |
| **FILEFLAGSMASK** *FILEFLAGSMASK* | 指出 **fileflags 機碼** 語句中的位有效。 若為16位 Windows，則此值為0x3f。                                                                                                                                                                                                                                                                                                                                          |
| **Fileflags 機碼** *fileflags 機碼*         | 檔案的屬性。                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **FILEOS** *FILEOS*               | 專為其設計此檔案的作業系統。 *Fileos* 參數可以是 [備註] 區段中提供的其中一個作業系統值。                                                                                                                                                                                                                                                                                               |
| **類型** 類型 *類型*           | 一般檔案類型。 內容 *類型參數可以* 是 [備註] 區段中所列的其中一種檔案類型值。                                                                                                                                                                                                                                                                                                                                |
| **FILESUBTYPE** *子類型*         | 檔案的功能。 除非 **類型類型語句中** 的 *類型* 參數是 VFT winspool.drv、VFT  \_ \_ font-family 或 VFT VXD，否則子類型參數為零 \_ 。 如需檔案子類型值的清單，請參閱「備註」一節。                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*block 語句*
</dt> <dd>

指定一或多個版本資訊區塊。 區塊可以包含字串資訊或變數資訊。 如需詳細資訊，請參閱 [**StringFileInfo block**](stringfileinfo-block.md) 或 [**VarFileInfo block**](varfileinfo-block.md)。

</dd> </dl>

## <a name="remarks"></a>備註

若要使用以 **VERSIONINFO** 語句指定的常數，您必須在資源定義檔中包含 Winver .H 或 Windows .h 標頭檔。

下列清單描述 **VERSIONINFO** 語句中使用的參數：

<dl> <dt>

<span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags 機碼*
</dt> <dd>

下列值的組合。



| 值                      | 描述                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VS \_ FF \_ DEBUG**          | 檔案包含偵錯工具資訊，或是已啟用偵錯工具的編譯功能。                                                                                                                                                                                         |
| **VS \_ FF \_ 修補**        | 檔案已修改，而且與相同版本號碼的原始運送檔案不相同。                                                                                                                                                                       |
| **VS \_ FF \_ 發行前版本**     | 檔案是開發版本，而不是商業發行的產品。                                                                                                                                                                                                         |
| **VS \_ FF \_ PRI加值稅EBUILD**   | 檔案不是使用標準發行程式所建立。 如果指定此值， [**StringFileInfo 區塊**](stringfileinfo-block.md) 必須包含 **PrivateBuild** 字串。                                                                                              |
| **VS \_ FF \_ SPECIALBUILD**   | 檔案是由使用標準發行程式的原始公司所建立，但是相同版本號碼之標準檔案的變化。 如果指定了這個值， [ **StringFileInfo** 區塊](stringfileinfo-block.md)區塊就必須包含 **SpecialBuild** 字串。 |
| **VS \_ FFI \_ FILEFLAGSMASK** | 所有上述值的組合。                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="fileos"></span><span id="FILEOS"></span>*fileos*
</dt> <dd>

下列其中一個值。



| 值                   | 描述                                                      |
|-------------------------|------------------------------------------------------------------|
| **VOS \_ 不明**        | 設計檔案的作業系統不明。 |
| **VOS \_ DOS**            | 檔案是針對 MS-DOS 所設計。                                    |
| **VOS \_ NT**             | 檔案是針對32位 Windows 所設計。                            |
| **VOS \_ \_ WINDOWS16**    | 檔案是針對16位 Windows 所設計。                            |
| **VOS \_ \_ WINDOWS32**    | 檔案是針對32位 Windows 所設計。                            |
| **VOS \_ DOS \_ WINDOWS16** | 檔案是針對以 MS-DOS 執行的16位 Windows 所設計。        |
| **VOS \_ DOS \_ WINDOWS32** | 檔案是針對使用 MS-DOS 執行的32位 Windows 所設計。        |
| **VOS \_ NT \_ WINDOWS32**  | 檔案是針對32位 Windows 所設計。                            |



 

0x00002L、0x00003L、0x20000L 和0x30000L 的值是保留的。

</dd> <dt>

<span id="filetype"></span><span id="FILETYPE"></span>*filetype*
</dt> <dd>

下列其中一個值。



| 值                | 描述                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **VFT \_ 不明**     | 檔案類型未知。                                                                                                       |
| **VFT \_ 應用程式**         | 檔案包含應用程式。                                                                                               |
| **VFT \_ DLL**         | 檔案包含動態連結程式庫 (DLL) 。                                                                                 |
| **VFT \_ WINSPOOL.DRV**         | 檔案包含設備磁碟機。 如果 *類型* 為 **VFT \_ winspool.drv**，則 *子類型* 會包含更具體的驅動程式描述。 |
| **VFT \_ 字型**        | 檔案包含字型。 如果 [ *類型* ] 為 [VFT] \_ 字型，則 *子類型* 會包含更明確的字型描述。               |
| **VFT \_ VXD**         | 檔案包含虛擬裝置。                                                                                             |
| **VFT \_ 靜態 \_ LIB** | 檔案包含靜態程式庫。                                                                                        |



 

所有其他值都會保留給 Microsoft 使用。

</dd> <dt>

<span id="subtype"></span><span id="SUBTYPE"></span>*亞*
</dt> <dd>

有關檔案類型的其他資訊。

如果資料 *類型* 指定 **VFT \_ winspool.drv**，則此參數可以是下列其中一個值。



| 值                             | 描述                               |
|-----------------------------------|-------------------------------------------|
| **VFT2 \_ 不明**                 | 驅動程式類型未知。                   |
| **VFT2 \_ Winspool.drv \_ 通訊**               | 檔案包含通訊驅動程式。    |
| **VFT2 \_ Winspool.drv \_ 印表機**            | 檔案包含印表機驅動程式。           |
| **VFT2 \_ Winspool.drv \_ 鍵盤**           | 檔案包含鍵盤驅動程式。          |
| **VFT2 \_ Winspool.drv \_ 語言**           | 檔案包含語言驅動程式。          |
| **VFT2 \_ Winspool.drv \_ 顯示**            | 檔案包含顯示驅動程式。           |
| **VFT2 \_ Winspool.drv \_ 滑鼠**              | 檔案包含滑鼠驅動程式。             |
| **VFT2 \_ Winspool.drv \_ 網路**            | 檔案包含網路驅動程式。           |
| **VFT2 \_ Winspool.drv \_ 系統**             | 檔案包含系統驅動程式。            |
| **VFT2 \_ winspool.drv 可 \_ 安裝**        | 檔案包含可安裝的驅動程式。      |
| **VFT2 \_ Winspool.drv \_ 音效**              | 檔案包含音效驅動程式。             |
| **VFT2 \_ Winspool.drv \_ 版本的 \_ 印表機** | 檔案包含已建立版本的印表機驅動程式。 |



 

如果資料 *類型* 指定 **VFT \_ 字型**，則此參數可以是下列其中一個值。



| 值                    | 描述                    |
|--------------------------|--------------------------------|
| **VFT2 \_ 不明**        | 字型類型未知。          |
| **VFT2 \_ 字型 \_ 點陣**   | 檔案包含點陣字型。   |
| **VFT2 \_ 字型 \_ 向量**   | 檔案包含向量字型。   |
| **VFT2 \_ 字型 \_ TRUETYPE** | 檔案包含 TrueType 字型。 |



 

如果資料 *類型* 指定 VFT \_ VXD，則此參數必須是虛擬裝置控制區塊中包含的虛擬裝置識別碼。

此處未列出的所有 *子類型* 值都是保留給 Microsoft 使用。

</dd> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

下列其中一種語言代碼。



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
| 0x0414 | 挪威語？ 博克  | 0x100C | 瑞士法文              |
| 0x0810 | 瑞士義大利文       | 0x0816 | 葡萄牙文 (葡萄牙)     |
| 0x0813 | 比利時荷蘭文       | 0x081A | Serbo-Croatian (斯拉夫)  |
| 0x0814 | 挪威語？ 耐諾斯克 |        |                           |



 

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

下列其中一個字元集識別碼。



| Decimal | 十六進位 | 字元集              |
|---------|-------------|----------------------------|
| 0       | 0000        | 7位 ASCII                |
| 932     | 03A4        | 日本 (Shift？ JIS X-0208)  |
| 949     | 03B5        | 韓國 (Shift？ KSC 5601)    |
| 950     | 03B6        | 臺灣 (Big5)               |
| 1200    | 04B0        | Unicode                    |
| 1250    | 04E2        | 拉丁美洲 (東部歐洲)  |
| 1251    | 04E3        | 古斯拉夫文                   |
| 1252    | 04E4        | 多 語種               |
| 1253    | 04E5        | 希臘文                      |
| 1254    | 04E6        | 土耳其文                    |
| 1255    | 04E7        | Hebrew                     |
| 1256    | 04E8        | 阿拉伯文                     |



 

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*字串名稱*
</dt> <dd>

下列其中一個預先定義的名稱。



| Name                 | 描述                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **註解**         | 為了診斷而應顯示的其他資訊。                                                                                                                                                                                                                                    |
| **CompanyName**      | 產生檔案的公司，例如「Microsoft Corporation」或「標準 Microsystems Corporation，Inc.」。 這個字串是必要的。                                                                                                                                                                   |
| **FileDescription**  | 要呈現給使用者的檔案描述。 當使用者選擇要安裝的檔案時，此字串可能會顯示在清單方塊中（例如，「AT-Style 鍵盤的鍵盤驅動程式」）。 這個字串是必要的。                                                                                            |
| **FileVersion**      | 檔案的版本號碼，例如 "3.10" 或 "5.00. RC2"。 這個字串是必要的。                                                                                                                                                                                                                      |
| **InternalName**     | 檔案的內部名稱（如果有的話）？例如，如果檔案是動態連結程式庫，則為模組名稱。 如果檔案沒有內部名稱，此字串應該是不含副檔名的原始檔案名。 這個字串是必要的。                                                                       |
| **LegalCopyright**   | 適用于檔案的著作權注意事項。 這應該包含所有通知、法律符號、著作權日期等的完整文字。 這個字串是選擇性的。                                                                                                                                             |
| **LegalTrademarks**  | 適用于檔案的商標及注冊商標。 這應包括所有注意事項全文、法律符號、商標登錄編號等等。 這個字串是選擇性的。                                                                                                                        |
| **OriginalFilename** | 檔案的原始名稱，不包含路徑。 這項資訊可讓應用程式判斷使用者是否已重新命名檔案。 名稱的格式取決於建立檔案的檔案系統。 這個字串是必要的。                                                 |
| **PrivateBuild**     | 檔案私用版本的相關資訊，例如「在 TESTBED 上由 TESTER1 建立」 \\ 。 只有當 **VS \_ FF \_ PRI加值稅EBUILD** 是在根區塊的 *fileflags 機碼* 參數中指定時，才會出現這個字串。                                                                                   |
| **ProductName**      | 用來散發檔案的產品名稱。 這個字串是必要的。                                                                                                                                                                                                                            |
| **ProductVersion**   | 散發檔案時所使用的產品版本（例如 "3.10" 或 "5.00. RC2"）。 這個字串是必要的。                                                                                                                                                                                       |
| **SpecialBuild**     | 指出此檔案版本與標準版本有何差異的文字（例如「TESTER1 在 M250 和 M250E 電腦上解決滑鼠問題的私用組建」）。 只有當 **VS \_ FF \_ SPECIALBUILD** 是在根區塊的 *fileflags 機碼* 參數中指定時，才會出現這個字串。 |



 

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="examples"></a>範例

下列範例會定義 **VERSIONINFO** 資源：

``` syntax
#define VER_FILEVERSION             3,10,349,0
#define VER_FILEVERSION_STR         "3.10.349.0\0"

#define VER_PRODUCTVERSION          3,10,0,0
#define VER_PRODUCTVERSION_STR      "3.10\0"

#ifndef DEBUG
#define VER_DEBUG                   0
#else
#define VER_DEBUG                   VS_FF_DEBUG
#endif

VS_VERSION_INFO VERSIONINFO
FILEVERSION     VER_FILEVERSION
PRODUCTVERSION  VER_PRODUCTVERSION
FILEFLAGSMASK   VS_FFI_FILEFLAGSMASK
FILEFLAGS       (VER_PRIVATEBUILD|VER_PRERELEASE|VER_DEBUG)
FILEOS          VOS__WINDOWS32
FILETYPE        VFT_DLL
FILESUBTYPE     VFT2_UNKNOWN
BEGIN
    BLOCK "StringFileInfo"
    BEGIN
        BLOCK "040904E4"
        BEGIN
            VALUE "CompanyName",      VER_COMPANYNAME_STR
            VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
            VALUE "FileVersion",      VER_FILEVERSION_STR
            VALUE "InternalName",     VER_INTERNALNAME_STR
            VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
            VALUE "LegalTrademarks1", VER_LEGALTRADEMARKS1_STR
            VALUE "LegalTrademarks2", VER_LEGALTRADEMARKS2_STR
            VALUE "OriginalFilename", VER_ORIGINALFILENAME_STR
            VALUE "ProductName",      VER_PRODUCTNAME_STR
            VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
        END
    END

    BLOCK "VarFileInfo"
    BEGIN
        /* The following line should only be modified for localized versions.     */
        /* It consists of any number of WORD,WORD pairs, with each pair           */
        /* describing a language,codepage combination supported by the file.      */
        /*                                                                        */
        /* For example, a file might have values "0x409,1252" indicating that it  */
        /* supports English language (0x409) in the Windows ANSI codepage (1252). */

        VALUE "Translation", 0x409, 1252

    END
END
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用版本資訊](./using-version-information.md)
</dt> <dt>

[版本資訊](./version-information.md)
</dt> </dl>

 

 