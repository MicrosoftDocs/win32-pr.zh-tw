---
title: VS_VERSIONINFO 結構
description: 代表檔案版本資源中的資料組織。 它是包含所有其他檔案版本資訊結構的根結構。
ms.assetid: 7864510f-1894-4f17-bf7b-fd5bc1ba4aae
keywords:
- VS_VERSIONINFO 結構功能表和其他資源
topic_type:
- apiref
api_name:
- VS_VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2758d5553e192357296868e2dbb62f7a6733ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106163"
---
# <a name="vs_versioninfo-structure"></a>VS \_ VERSIONINFO 結構

代表檔案版本資源中的資料組織。 它是包含所有其他檔案版本資訊結構的根結構。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD             wLength;
  WORD             wValueLength;
  WORD             wType;
  WCHAR            szKey;
  WORD             Padding1;
  VS_FIXEDFILEINFO Value;
  WORD             Padding2;
  WORD             Children;
} VS_VERSIONINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**wLength**
</dt> <dd>

類型： **WORD**

</dd> <dd>

**VS \_ VERSIONINFO** 結構的長度（以位元組為單位）。 此長度不包含在32位界限上對齊任何後續版本資源資料的任何填補。

</dd> <dt>

**wValueLength**
</dt> <dd>

類型： **WORD**

</dd> <dd>

**值** 成員的長度（以位元組為單位）。 如果沒有任何與目前版本結構相關聯的 **值** 成員，則此值為零。

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

Unicode 字串 L 「VS \_ VERSION \_ INFO」。

</dd> <dt>

**Padding1**
</dt> <dd>

類型： **WORD**

</dd> <dd>

包含所需的零個單字，以對齊32位界限上的 **值** 成員。

</dd> <dt>

**值**
</dt> <dd>

類型： **[ **VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**

</dd> <dd>

與這個 **VS \_ VERSIONINFO** 結構相關聯的任意資料。 **WValueLength** 成員會指定這個成員的長度;如果 **wValueLength** 為零，則此成員不存在。

</dd> <dt>

**Padding2**
</dt> <dd>

類型： **WORD**

</dd> <dd>

在32位界限上對齊 **子** 成員所需的任意零個單字。 這些位元組不包含在 **wValueLength** 中。 這個成員是選擇性的。

</dd> <dt>

**子系**
</dt> <dd>

類型： **WORD**

</dd> <dd>

零或一個 [**StringFileInfo**](stringfileinfo.md)結構的陣列，以及屬於目前 **VS \_ VERSIONINFO** 結構子系的零個或一個 [**VarFileInfo**](varfileinfo.md)結構。

</dd> </dl>

## <a name="remarks"></a>備註

此結構不是真正的 C 語言結構，因為它包含可變長度的成員。 此結構是專門用來描述版本資源中的資料組織，而不會出現在隨附于 Windows 軟體開發套件 (SDK) 的任何標頭檔中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

**概念**
</dt> <dt>

[版本資訊](version-information.md)
</dt> </dl>

 

 





