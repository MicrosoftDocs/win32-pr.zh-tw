---
description: 下列清單描述放電原則常數。
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: " (WinNT. h) 釋出原則常數"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a05237b7555cc7281f132f02110a10cb5b58cd342d6872b16c1a6319773ea8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961868"
---
# <a name="discharge-policy-constants"></a>放電原則常數

下列清單描述放電原則常數。



| 常數/值                                                                                                                                                                                                                                            | 描述                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <dt>**放電 \_原則 \_ 關鍵性**</dt> <dt>0</dt> </dl> | 當電池出院低於 [重大臨界值] 時，會使用哪一個電池放電原則設定 ([**系統 \_ 電源 \_ 等級**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) 結構) 。<br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <dt>**放電 \_原則 \_ 低**</dt> <dt>1</dt> </dl>                | 當電池出院低於低閾值時，會使用) 的電池放電原則設定 ([**系統 \_ 電源 \_ 等級**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) 結構。<br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <dt>**NUM \_放電 \_ 原則**</dt> <dt>4</dt> </dl>          | ) 指定 ([**系統 \_ 電源 \_ 等級**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) 結構的電池放電原則設定數目。<br/>                                                           |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>WinNT (包含 Windows .h) </dt> </dl> |



 

 




