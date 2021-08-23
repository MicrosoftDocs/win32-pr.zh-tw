---
description: 允許回呼將專案加入至擴充功能表的頂端。
title: 'DFM_MERGECONTEXTMENU_TOP 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: eed6aec6-11a0-4738-b5b9-a455d0e35eac
api_name:
- DFM_MERGECONTEXTMENU_TOP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4cafbbe7331242e65e27137a1b5b78da6b8c6086c8326f96bbc32520366d10a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351118"
---
# <a name="dfm_mergecontextmenu_top-message"></a>DFM \_ MERGECONTEXTMENU \_ TOP message

允許回呼將專案加入至擴充功能表的頂端。


```C++
DFM_MERGECONTEXTMENU_TOP

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*pqcminfo* \[在\]
</dt> <dd>

[**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo)結構的指標，其中包含合併中使用的資訊。

</dd> <dt>

*uFlags* \[在\]
</dt> <dd>

指定如何變更內容功能表的旗標。 此參數會使用 \_ \* [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)中所述的 CM光圈值。

</dd> </dl>

## <a name="remarks"></a>備註

如果專案加入至擴充的內容功能表中，則在使用 [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md)叫用其中一個專案時，這些專案必須受到適當回應的常式支援。

這則訊息會傳送至回呼函式或回呼物件（根據預設的內容功能表物件的執行方式而定）。 有兩個 Api 適用于其實 [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)、 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)。

[**DFM \_INVOKECOMMANDEX**](dfm-invokecommandex.md) 是此訊息的擴充版本，可提供更多的回呼資訊。 如果您的實作需要該介面所提供的其他資訊，請使用 **DFM \_ INVOKECOMMANDEX** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 




