---
title: 多播群組管理員回呼
description: 多播群組管理員會使用下列回呼來通知用戶端 (通常是) 事件和狀態變更的路由通訊協定
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ba18f874005e23aef6daca6071362362312e8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842511"
---
# <a name="multicast-group-manager-callbacks"></a>多播群組管理員回呼

多播群組管理員會使用下列回呼來通知用戶端 (通常是) 事件和狀態變更的路由通訊協定：

[**PMGM \_ 建立 \_ 警示 \_ 回呼**](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[**PMGM \_ 聯結 \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[**PMGM \_ 剪除 \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[**PMGM \_ 本機 \_ 聯結 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[**PMGM \_ 本地 \_ 離開 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[**PMGM \_ RPF \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[**回呼的 PMGM \_ 錯誤 \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

多播群組管理員會使用下列回呼來通知 IGMP 事件和狀態變更：

[**PMGM \_ 停用 \_ IGMP \_ 回呼**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[**PMGM \_ 啟用 \_ IGMP \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 