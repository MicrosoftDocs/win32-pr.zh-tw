---
description: 允許回呼將專案加入功能表中。
title: 'DFM_MERGECONTEXTMENU 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2fd779ac-7dd6-4b81-86dc-8930db27ae59
api_name:
- DFM_MERGECONTEXTMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ddd071e40d3c017a513eb0e85efb634df530a8686afaf7df59b922602d37f22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455968"
---
# <a name="dfm_mergecontextmenu-message"></a>DFM \_ MERGECONTEXTMENU 訊息

允許回呼將專案加入功能表中。


```C++
DFM_MERGECONTEXTMENU

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

如果專案已新增至內容功能表，則在使用 [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md)叫用其中一個專案時，這些專案必須受到適當回應的常式支援。

這則訊息會傳送至回呼函式或回呼物件（根據預設的內容功能表物件的執行方式而定）。 有兩個 Api 適用于其實 [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)、 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)。

[**DFM \_INVOKECOMMANDEX**](dfm-invokecommandex.md) 是此訊息的擴充版本，可提供更多的回呼資訊。 如果您的實作需要該介面所提供的其他資訊，請使用 **DFM \_ INVOKECOMMANDEX** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 




