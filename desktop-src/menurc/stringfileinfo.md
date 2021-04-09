---
title: StringFileInfo 結構
description: 代表檔案版本資源中的資料組織。 它包含可以針對特定語言和字碼頁顯示的版本資訊。
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- StringFileInfo 結構功能表和其他資源
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f252077a5536194e635281d4b4178a457f7a82cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934049"
---
# <a name="stringfileinfo-structure"></a>StringFileInfo 結構

代表檔案版本資源中的資料組織。 它包含可以針對特定語言和字碼頁顯示的版本資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a>成員

<dl> <dt>

**wLength**
</dt> <dd>

類型： **WORD**

</dd> <dd>

整個 **StringFileInfo** 區塊的長度（以位元組為單位），包括 **子** 成員所指示的所有結構。

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

Unicode 字串 L "StringFileInfo"。

</dd> <dt>

**填補**
</dt> <dd>

類型： **WORD**

</dd> <dd>

在32位界限上對齊 **子** 成員所需的任意零個單字。

</dd> <dt>

**子系**
</dt> <dd>

類型： **[ **StringTable**](stringtable.md)**

</dd> <dd>

一或多個 [**StringTable**](stringtable.md) 結構的陣列。 每個 **StringTable** 結構的 **szKey** 成員都會指出適當的語言和字碼頁，以顯示該 **StringTable** 結構中的文字。

</dd> </dl>

## <a name="remarks"></a>備註

此結構不是真正的 C 語言結構，因為它包含可變長度的成員。 此結構是專門用來描述版本資源中的資料組織，而不會出現在隨附于 Windows 軟體開發套件 (SDK) 的任何標頭檔中。

[**VS \_ VERSIONINFO**](vs-versioninfo.md)結構的 **子** 成員可以包含零或多個 **StringFileInfo** 結構。

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

[**字串**](string-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**概念**
</dt> <dt>

[版本資訊](version-information.md)
</dt> </dl>

 

 





