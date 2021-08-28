---
title: 'SBM_ENABLE_ARROWS 訊息 (Winuser .h) '
description: 應用程式會傳送 SBM \_ 啟用 \_ 箭號訊息，以啟用或停用捲軸控制項的一個或兩個箭號。
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- SBM_ENABLE_ARROWS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SBM_ENABLE_ARROWS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e7f3ef8728befe72ec4f2c4afe39caeb10bc0b58984612a5db2445963dc549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770018"
---
# <a name="sbm_enable_arrows-message"></a>SBM \_ 啟用 \_ 箭號訊息

應用程式會傳送 **SBM \_ 啟用 \_ 箭** 號訊息，以啟用或停用捲軸控制項的一個或兩個箭號。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定捲軸箭號是否為啟用或停用，以及表示已啟用或停用的箭號。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                   | 意義                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <dt>**ESB \_ 停用 \_ 兩者**</dt> </dl> | 停用捲軸上的兩個箭號。<br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <dt>**ESB \_ 停 \_ 用**</dt> </dl> | 停用垂直捲動條上的向下箭號。<br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <dt>**ESB \_ 停用 \_ LTUP**</dt> </dl> | 停用水準捲軸上的向左箭號或垂直捲動條上的向上箭號。<br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <dt>**ESB \_ 停用 \_ 左**</dt> </dl> | 停用水準捲軸上的向左鍵。<br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <dt>**ESB \_ 停用 \_ RTDN**</dt> </dl> | 停用水準捲軸上的向右箭號或垂直捲動條上的向下箭號。<br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <dt>**ESB \_ 停 \_ 用**</dt> </dl>       | 停用垂直捲動條上的向上箭號。<br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <dt>**ESB \_ 啟用 \_ 兩者**</dt> </dl>    | 在捲軸上啟用這兩個箭號。<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值為 **TRUE**;否則為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



 

 





