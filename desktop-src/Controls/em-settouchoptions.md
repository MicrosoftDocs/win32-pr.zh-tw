---
title: 'EM_SETTOUCHOPTIONS 訊息 (Richedit .h) '
description: 設定與 rich edit 控制項相關聯的觸控選項。
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- EM_SETTOUCHOPTIONS 訊息 Windows 控制項
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
ms.openlocfilehash: 4ea2f372d1e59a76ea13667e994534df1088fe1c78c51c30ac54db1b4dfeed2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048008"
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
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETTOUCHOPTIONS**](em-settouchoptions.md)
</dt> </dl>

 

 





