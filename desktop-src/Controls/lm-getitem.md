---
title: 'LM_GETITEM 訊息 (Commctrl .h) '
description: 抓取專案的狀態和屬性。
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- LM_GETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LM_GETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb0e05f896df00f3762c53e6f5f62119cb3645f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093868"
---
# <a name="lm_getitem-message"></a>LM \_ GETITEM 訊息

抓取專案的狀態和屬性。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須是 **Null**。 </dd> <dt>

*lParam* 
</dt> <dd>要填入專案相關資訊之 <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> 結構的指標。 </dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功取得指定的值和屬性，則傳回 **TRUE** 。

## <a name="remarks"></a>備註

使用 **LM \_ GETITEM** 訊息時，只能透過 [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem)的 **ashraf** 成員所傳回的數值索引來存取連結。 不支援透過 **szID** 中傳回的識別碼名稱來存取連結。

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





