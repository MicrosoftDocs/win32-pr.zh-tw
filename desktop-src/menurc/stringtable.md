---
title: StringTable 結構
description: 代表檔案版本資源中的資料組織。 它包含子系成員所指定之字串的語言和字碼頁格式資訊。 字碼頁是一組已排序的字元集。
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- StringTable 結構功能表和其他資源
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc790baa6484c5b1a8a7d96a0a7bc8e8ad12b0e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384141"
---
# <a name="stringtable-structure"></a>StringTable 結構

代表檔案版本資源中的資料組織。 它包含 **子** 系成員所指定之字串的語言和字碼頁格式資訊。 字碼頁是一組已排序的字元集。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD   wLength;
  WORD   wValueLength;
  WORD   wType;
  WCHAR  szKey;
  WORD   Padding;
  String Children;
} StringTable;
```



## <a name="members"></a>成員

<dl> <dt>

**wLength**
</dt> <dd>

類型： **WORD**

</dd> <dd>

這個 **StringTable** 結構的長度（以位元組為單位），包括 **子** 成員所指示的所有結構。

</dd> <dt>

**wValueLength**
</dt> <dd>

類型： **WORD**

</dd> <dd>

這個成員永遠等於零。

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

儲存為 Unicode 字串的8位數十六進位數位。 四個最有效的數位代表語言識別項。 四個最不重要的數位代表要格式化資料的字碼頁。 每個 Microsoft 標準語言識別項都包含兩個部分：低序位10位會指定主要語言，而高序位6位則會指定語言。 如需有效識別碼的表格，請參閱。

</dd> <dt>

**填補**
</dt> <dd>

類型： **WORD**

</dd> <dd>

在32位界限上對齊 **子** 成員所需的任意零個單字。

</dd> <dt>

**子系**
</dt> <dd>

類型： **[**字串**](string-str.md)**

</dd> <dd>

一或多個 [**字串**](string-str.md) 結構的陣列。

</dd> </dl>

## <a name="remarks"></a>備註

此結構不是真正的 C 語言結構，因為它包含可變長度的成員。 此結構是專門用來描述版本資源中的資料組織，而不會出現在隨附于 Windows 軟體開發套件 (SDK) 的任何標頭檔中。

[**StringFileInfo**](stringfileinfo.md)結構的 **子** 系成員至少包含一個 **StringTable** 結構。

將 **szKey** 成員的字碼頁部分設定為十六進位值0x04b0，以指出 Unicode 字碼頁或適用于語言元件之字碼頁的十六進位值。 選擇 [字碼頁] 的值之後，您應該會在稍後的檔案修訂中繼續使用相同的值。

支援多種語言的可執行檔或 DLL 應該具有每個語言的版本資源，而不是包含數種語言之字串的單一版本資源。 但是，如果您使用 [**var**](var-str.md)結構來列出您的應用程式支援的語言，則版本資源中的 **StringTable** 結構數目會與 **Var** 結構的 **Value** 成員中的語言/字碼頁識別碼組數目直接相關。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**字串**](string-str.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**無 功**](var-str.md)
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**概念**
</dt> <dt>

[版本資訊](version-information.md)
</dt> </dl>

 

 





