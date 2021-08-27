---
title: 'LVM_SETGROUPMETRICS 訊息 (Commctrl .h) '
description: 設定群組顯示的相關資訊。
ms.assetid: 268b478d-da1f-4efe-9ee9-af3f12e089ee
keywords:
- LVM_SETGROUPMETRICS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32f978c763fd1602d06f921a5da38a895fb1d3c76573341d9ca4f2987a0d3c7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077258"
---
# <a name="lvm_setgroupmetrics-message"></a>LVM \_ SETGROUPMETRICS 訊息

設定群組顯示的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須是 **Null**。</dd> <dt>

*lParam* 
</dt> <dd><a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a>結構的指標，其中包含要設定的度量。</dd> </dl>

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



 

 





