---
title: MENUEX_TEMPLATE_ITEM 結構
description: 定義擴充功能表範本中的功能表項目。 此結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- MENUEX_TEMPLATE_ITEM 結構功能表和其他資源
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca1f73d1174590db5948f54f5c51c91a8c65a8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509188"
---
# <a name="menuex_template_item-structure"></a>MENUEX \_ 範本 \_ 專案結構

定義擴充功能表範本中的功能表項目。 此結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法

```C++
typedef struct {
  DWORD dwType;
  DWORD dwState;
  UINT  uId;
  WORD  wFlags;
  WCHAR szText[1];
} MENUEX_TEMPLATE_ITEM;
```

## <a name="members"></a>成員

<dl> <dt>

**dwType**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

功能表項目類型。 這個成員可以是類型 (開頭是與 [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) 結構一起列出的 MFT) 值的組合。

</dd> <dt>

**dwState**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

功能表項目的狀態。 這個成員可以是狀態 (的組合，其開頭為 MFS) 與 [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) 結構一起列出的值。

</dd> <dt>

**Uid**
</dt> <dd>

類型： **UINT**

</dd> <dd>

功能表項目識別碼。 這是用來識別功能表項目的應用程式定義值。 在擴充功能表資源中，開啟下拉式功能表或子功能表，以及命令專案的專案都可以有識別碼。

</dd> <dt>

**wFlags**
</dt> <dd>

類型： **WORD**

</dd> <dd>

指定功能表項目是功能表列、下拉式功能表、子功能表或快捷方式功能表中的最後一個專案，以及是否為開啟下拉式功能表或子功能表的專案。 這個成員可以是零或多個這些值。 若為32位應用程式，這個成員是一個字;若是16位應用程式，則是位元組。

<dt>

0x80
</dt> <dd>

結構會定義功能表列、下拉式功能表、子功能表或快捷方式功能表中的最後一個功能表項目。

</dd> <dt>

0x01
</dt> <dd>

結構會定義開啟下拉式功能表或子功能表的專案。 後續的結構會在對應的下拉式功能表或子功能表中定義功能表項目。

</dd> </dl> </dd> <dt>

**szText**
</dt> <dd>

類型： **WCHAR**

</dd> <dd>

功能表項目文字。 這個成員是以 null 結束的 Unicode 字串，在字邊界上對齊。 功能表項目定義的大小會根據此字串的長度而有所不同。

</dd> </dl>

## <a name="remarks"></a>備註

擴充功能表範本包含 [**MENUEX \_ 範本 \_ 標頭**](menuex-template-header.md) 結構，後面接著一個或多個連續的 **MENUEX \_ 範本 \_ 專案** 結構。 **MENUEX \_ 範本 \_ 專案** 結構（長度為變數）會對齊 **DWORD** 界限。 若要從記憶體中的擴充功能表範本建立功能表，請使用 [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[**MENUEX \_ 範本 \_ 標頭**](menuex-template-header.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

**概念**
</dt> <dt>

[功能表](menus.md)
</dt> </dl>

 

 





