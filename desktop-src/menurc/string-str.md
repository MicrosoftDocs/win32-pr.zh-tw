---
title: 字串結構
description: 代表檔案版本資源中的資料組織。 它包含的字串會描述檔案的特定層面，例如檔案的版本、其著作權聲明或其商標。
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- 字串結構功能表和其他資源
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7035223082a9e446caebd6e07d3d55c84536d09f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967526"
---
# <a name="string-structure"></a>字串結構

代表檔案版本資源中的資料組織。 它包含的字串會描述檔案的特定層面，例如檔案的版本、其著作權聲明或其商標。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a>成員

<dl> <dt>

**wLength**
</dt> <dd>

類型： **WORD**

</dd> <dd>

這個 **字串** 結構的長度（以位元組為單位）。

</dd> <dt>

**wValueLength**
</dt> <dd>

類型： **WORD**

</dd> <dd>

**值** 成員的大小，以單字為限。

</dd> <dt>

**wType**
</dt> <dd>

類型： **WORD**

</dd> <dd>

版本資源中的資料類型。 如果版本資源包含文字資料，則此成員為1，如果版本資源包含二進位資料，則為0。

</dd> <dt>

**szKey**
</dt> <dd>

類型： **WCHAR**

</dd> <dd>

任意的 Unicode 字串。 **SzKey** 成員可以是下列一或多個值。 這些值只是指導方針。

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**評論**


</dt> <dd>

**值** 成員包含應針對診斷目的顯示的任何其他資訊。 這個字串可以是任意長度。

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**名稱**


</dt> <dd>

**值** 成員會識別產生檔案的公司。 例如，"Microsoft Corporation" 或 "Standard Microsystems Corporation，Inc."

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**


</dt> <dd>

**值** 成員會以提供給使用者的方式來描述檔案。 當使用者選擇要安裝的檔案時，此字串可能會顯示在清單方塊中。 例如，「適用于樣式鍵盤的鍵盤驅動程式」或「適用于 Windows 的 Microsoft Word」。

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**


</dt> <dd>

**值** 成員會識別此檔案的版本。 例如， **值** 可以是 "3.00 a" 或 "5.00. RC2"。

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**


</dt> <dd>

**值** 成員會識別檔案的內部名稱（如果有的話）。 例如，此字串可能包含 DLL 的模組名稱、Windows 虛擬裝置的虛擬裝置名稱，或 MS-DOS 設備磁碟機的裝置名稱。

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**


</dt> <dd>

**值** 成員描述適用于檔案的所有著作權聲明、商標和注冊商標。 這應包括所有注意事項全文、法律符號、版權日期、商標登錄編號等等。 在英文中，此字串的格式應為 "著作權 Microsoft Corp. 1990 1994"。

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**


</dt> <dd>

**值** 成員描述適用于檔案的所有商標和注冊商標。 這應包括所有注意事項全文、法律符號、商標登錄編號等等。 此段文字的英文格式應為 "Windows is a trademark of Microsoft Corporation"。

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**


</dt> <dd>

**值** 成員會識別檔案的原始名稱，而不包含路徑。 這可讓應用程式判斷使用者是否已重新命名檔案。 如果檔案是非 FAT 檔案系統的特定名稱，則此名稱不可以是 MS-DOS 8.3 格式。

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**


</dt> <dd>

**值** 成員會根據其建立檔案私用版本的位置和原因來描述。 只有當 vs **\_ FF \_ PRI加值稅EBUILD** 旗標設定于 [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)結構的 **dwFileFlags** 成員時，才會出現這個字串。 例如， **值** 可能是「OSCAR2 上的 OSCAR 建立」 \\ 。

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**名稱**


</dt> <dd>

**值** 成員會識別這個檔案所散發的產品名稱。 例如，這個字串可能是「Microsoft Windows」。

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**


</dt> <dd>

**值** 成員會識別這個檔案所散發的產品版本。 例如， **值** 可以是 "3.00 a" 或 "5.00. RC2"。

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**


</dt> <dd>

**值** 成員描述此檔案版本與一般版本的差異。 只有當 vs **\_ FF \_ SPECIALBUILD** 旗標設定于 [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)結構的 **dwFileFlags** 成員時，此專案才會存在。 例如， **值** 可能是「Olivetti 在 M250 和 M250E 電腦上解決滑鼠問題的私用組建」。

</dd> </dl> </dd> <dt>

**填補**
</dt> <dd>

類型： **WORD**

</dd> <dd>

在32位界限上對齊 **值** 成員所需的任意零個單字。

</dd> <dt>

**值**
</dt> <dd>

類型： **WORD**

</dd> <dd>

以零結尾的字串。 如需詳細資訊，請參閱 **szKey** 成員描述。

</dd> </dl>

## <a name="remarks"></a>備註

此結構不是真正的 C 語言結構，因為它包含可變長度的成員。 此結構是專門用來描述版本資源中的資料組織，而不會出現在隨附于 Windows 軟體開發套件 (SDK) 的任何標頭檔中。

**字串** 結構可能具有 szKey 值，例如 "  " 和 "Microsoft Corporation" 的 **值**。 另一個具有相同 **szKey** 值的 **字串** 結構可能包含 "Microsoft GmbH" 的 **值**。 如果第二個 **字串** 結構與 [**StringTable**](stringtable.md) 結構相關聯，而其 **szKey** 值是040704b0，也就是德文/Unicode，則可能會發生這種情況。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**StringTable**](stringtable.md)
</dt> <dt>

[**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**概念**
</dt> <dt>

[版本資訊](version-information.md)
</dt> </dl>

 

 





