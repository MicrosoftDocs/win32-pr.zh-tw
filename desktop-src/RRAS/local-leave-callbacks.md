---
title: 本地離開回呼
description: 當 IGMP 通知多播群組管理員之後，介面上的群組沒有其他接收者存在時，多播群組管理員會叫用該 \_ \_ 介面上的路由通訊協定的 PMGM 本地離開回呼回呼（如果有的話） \_ 。 此回呼會通知路由通訊協定的變更。
ms.assetid: 47696533-603c-459f-9aa7-3ce42fff3332
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4cd346ac3d84a5c763c7f8f866e21a1bffa2af533e5710c86ec8826ad7db45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790638"
---
# <a name="local-leave-callbacks"></a>本地離開回呼

當 IGMP 通知多播群組管理員之後，介面上的群組沒有其他接收者存在時，多播群組管理員會叫用該介面上的路由通訊協定的 [**PMGM \_ 本地 \_ 離開 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) 回呼（如果有的話）。 此回呼會通知路由通訊協定的變更。

此回呼和 [**PMGM 的 \_ 本機 \_ 聯結 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) 回呼會用來同步處理 IGMP 和路由通訊協定之間的轉送。

 

 




