---
title: 'SB_GETPARTS 訊息 (Commctrl .h) '
description: 捕獲狀態視窗中的部分計數。 此訊息也會抓取指定之部分數目的右邊緣座標。
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- SB_GETPARTS message Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee0f33331c579490cf66a38b9ce6655215ae673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509020"
---
# <a name="sb_getparts-message"></a>SB \_ GETPARTS 訊息

捕獲狀態視窗中的部分計數。 此訊息也會抓取指定之部分數目的右邊緣座標。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要抓取座標的部分數目。 如果此參數大於視窗中的部分數目，則訊息只會抓取現有元件的座標。

</dd> <dt>

*lParam* 
</dt> <dd>

整數陣列的指標，該陣列與 *wParam* 所指定的元件具有相同的專案數。 陣列中的每個元素都會接收相對應元件右邊緣的用戶端座標。 如果元素設定為-1，則該部分的右邊緣位置會延伸至視窗的右邊緣。 若要取出目前的部分數目，請將此參數設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回視窗中的部分數目。

## <a name="remarks"></a>備註

此訊息一律會傳回狀態列中的部分數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





