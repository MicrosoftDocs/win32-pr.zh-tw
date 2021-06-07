---
description: Wmi 服務事件疑難排解類別是由 WMI 服務內的事件所產生，例如建立執行緒集區。
ms.assetid: 1a1251c8-a2f7-47ac-9db1-d780d7d272f0
ms.tgt_platform: multiple
title: WMI 服務事件疑難排解類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e811ac5b276e5562f73b5b432d5f3255af5bab7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443059"
---
# <a name="wmi-service-event-troubleshooting-classes"></a>WMI 服務事件疑難排解類別

Wmi 服務事件疑難排解類別是由 WMI 服務內的事件所產生，例如建立執行緒集區。

您可以訂閱抽象基類的 [**MSFT \_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) 通知，以取得下表所列的所有衍生事件。



|   事件                                                                                        |   描述                                                                                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**MSFT \_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent)                                   | 所有 Windows Management Instrumentation (WMI) 事件子系統 (ESS) 自我事件的父類別。 |
| [**MSFT \_ WmiRegisterNotificationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiregisternotificationevent) | 表示建立事件查詢通知的事件接收。                       |
| [**MSFT \_ WmiCancelNotificationSink**](/previous-versions/windows/desktop/wmisystemprov/msft-wmicancelnotificationsink)       | 在取消事件接收器時產生。                                                           |
| [**MSFT \_ WmiThreadPoolEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolevent)                     | 提供 WMI 事件子系統中的執行緒事件通知 (ESS) 。                           |
| [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated)                 | 提供在 WMI 事件子系統中建立執行緒 (ESS) 時的通知。                   |
| [**MSFT \_ WmiThreadPoolDeleted**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpooldeleted)                 | 提供在 WMI 事件子系統中刪除線程 (ESS) 的通知。                   |
| [**MSFT \_ WmiFilterEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterevent)                             | 所有永久事件取用者篩選事件的父類別。                                        |
| [**MSFT \_ WmiFilterActivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilteractivated)                     | 定義成功啟用永久事件取用者訂用帳戶篩選。                |
| [**MSFT \_ WmiFilterDeactivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterdeactivated)                 | 定義永久取用者訂用帳戶篩選的成功停用。                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)
</dt> <dt>

WMI 疑難排解
</dt> <dt>

[監視事件](monitoring-events.md)
</dt> <dt>

[接收 WMI 事件](receiving-a-wmi-event.md)
</dt> </dl>

 

 
