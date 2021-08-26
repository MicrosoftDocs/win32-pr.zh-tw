---
title: 'LVM_GETGROUPMETRICS 訊息 (Commctrl .h) '
description: 取得群組顯示的相關資訊。
ms.assetid: 75e7da66-50c6-4834-ae66-e43b8f9b0b34
keywords:
- LVM_GETGROUPMETRICS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b99996adfe7f26342dde8967c95973fdb972290367328875257f5615f0a43c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062608"
---
# <a name="lvm_getgroupmetrics-message"></a>LVM \_ GETGROUPMETRICS 訊息

取得群組顯示的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須是 **Null**。</dd> <dt>

*lParam* 
</dt> <dd><a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a>結構的指標，此結構會接收已抓取的度量。</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





