---
title: 'LVM_GETVIEW 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項的目前視圖。
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- LVM_GETVIEW 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431b0a7b3fba9a45370c372347285489a56082c4a04396c273a45c4da41b05b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915508"
---
# <a name="lvm_getview-message"></a>LVM \_ GETVIEW 訊息

抓取清單視圖控制項的目前視圖。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回指定目前視圖的 **DWORD** 。

## <a name="remarks"></a>備註

以下是 views 的值。

-   LV \_ 視圖 \_ 詳細資料
-   LV \_ 視圖 \_ 圖示
-   LV \_ 視圖 \_ 清單
-   LV \_ 視圖 \_ SMALLICON
-   LV \_ 視圖 \_ 磚

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





