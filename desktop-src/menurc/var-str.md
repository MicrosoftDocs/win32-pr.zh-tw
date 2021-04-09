---
title: Var 結構
description: 代表檔案版本資源中的資料組織。 它通常會包含應用程式或 DLL 版本所支援的語言和字碼頁識別碼組清單。
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Var 結構功能表和其他資源
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 151103366e85537368cacb7063f199f1f91bf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844299"
---
# <a name="var-structure"></a>Var 結構

代表檔案版本資源中的資料組織。 它通常會包含應用程式或 DLL 版本所支援的語言和字碼頁識別碼組清單。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  DWORD Value;
} Var;
```



## <a name="members"></a>成員

<dl> <dt>

**wLength**
</dt> <dd>

類型： **WORD**

</dd> <dd>

**Var** 結構的長度（以位元組為單位）。

</dd> <dt>

**wValueLength**
</dt> <dd>

類型： **WORD**

</dd> <dd>

**值** 成員的長度（以位元組為單位）。

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

Unicode 字串 L 「轉譯」。

</dd> <dt>

**填補**
</dt> <dd>

類型： **WORD**

</dd> <dd>

在32位界限上對齊 **值** 成員所需的任意零個單字。

</dd> <dt>

**值**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

一或多個值為語言和字碼頁識別碼組的陣列。 如需詳細資訊，請參閱下列備註一節。

</dd> </dl>

## <a name="remarks"></a>備註

此結構不是真正的 C 語言結構，因為它包含可變長度的成員。 此結構是專門用來描述版本資源中的資料組織，而不會出現在隨附于 Windows 軟體開發套件 (SDK) 的任何標頭檔中。

如果您使用 **Var** 結構來列出您的應用程式或 DLL 所支援的語言，而不是使用多個版本的資源，請使用 **Value** 成員來包含 **DWORD** 值陣列，指出此檔案所支援的語言和字碼頁組合。 每個 **DWORD** 的低序位字必須包含 Microsoft 語言識別項，而高序位單字必須包含 IBM 字碼頁編號。 高序位或低序位的單字可以是零，表示檔案與語言或字碼頁無關。 如果省略了 **Var** 結構，檔案將會被視為與語言和字碼頁無關。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**StringTable**](stringtable.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**概念**
</dt> <dt>

[版本資訊](version-information.md)
</dt> </dl>

 

 





