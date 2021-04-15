---
title: 'EM_SETTOUCHOPTIONS 訊息 (Richedit .h) '
description: 設定與 rich edit 控制項相關聯的觸控選項。
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- EM_SETTOUCHOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7613679a574955ef726da9fa10e8d919c8fe53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465701"
---
# <a name="em_settouchoptions-message"></a>EM \_ SETTOUCHOPTIONS 訊息

設定與 rich edit 控制項相關聯的觸控選項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要設定的觸控選項。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                        | 意義                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO \_ SHOWHANDLES**</dt> </dl>          | 根據 *lParam* 的值，顯示或隱藏觸控控制手柄控點。<br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO \_ DISABLEHANDLES**</dt> </dl> | 根據 *lParam* 的值，啟用或停用觸控控制手柄控點。 當控制碼已停用時，如果已顯示並保持隱藏狀態，直到 **EM \_ SETTOUCHOPTIONS** 訊息變更其狀態時，就會隱藏處理常式。 <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

設定為 **TRUE** 以顯示/啟用觸控選取控點，或設定為 **FALSE** 以隱藏/停用觸控選取控點。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETTOUCHOPTIONS**](em-settouchoptions.md)
</dt> </dl>

 

 





