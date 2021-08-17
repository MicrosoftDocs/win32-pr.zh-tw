---
description: 全域旗標常數可用來啟用或停用使用者電源原則選項。
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: '全域旗標常數 (PowrProf .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2dfd23559959bee72e8572cc700a948df1e92dcdb37a03c41b52cdca4d578c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143525"
---
# <a name="global-flags-constants"></a>全域旗標常數

全域旗標常數可用來啟用或停用使用者電源原則選項。



| 常數/值                                                                                                                                                                                                                                                                                         | 描述                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt> </dl> | 啟用或停用系統電源計量表中的多個電池顯示器。<br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <dt>**EnablePasswordLogon**</dt> <dt>0x04</dt> </dl>                         | 當系統從待命或休眠狀態恢復時，啟用或停用需要密碼登入。<br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt> </dl> | 啟用或停用系統匣中的電池計量表圖示。 清除此旗標時，不會顯示電池計量表圖示。<br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt> </dl>                 | 啟用或停用在系統從 AC 電源上執行變更為以電池電源執行時，讓影片顯示變暗的支援。<br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <dt>**EnableWakeOnRing**</dt> <dt>0x08</dt> </dl>                                     | 啟用或停用喚醒功能支援。<br/>                                                                                               |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>PowrProf。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**全域 \_ 使用者 \_ 電源 \_ 原則**](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




