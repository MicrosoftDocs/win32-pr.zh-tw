---
title: 本機聯結回呼
description: 在 IGMP 通知多播群組管理員之後，介面上的群組有新的接收者存在時，多播群組管理員會叫用 PMGM \_ 本機 \_ 聯結 \_ 回呼回呼給擁有介面的路由通訊協定（如果有的話）。
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c97f0e16e08bc3781b946a51f69d2b0d65b3272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462361"
---
# <a name="local-join-callbacks"></a>本機聯結回呼

在 IGMP 通知多播群組管理員之後，介面上的群組有新的接收者存在時，多播群組管理員會叫用 [**PMGM \_ 本機 \_ 聯結 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) 回呼給擁有介面的路由通訊協定（如果有的話）。 此回呼會通知路由通訊協定的變更。

此回呼和 [**PMGM \_ 本地 \_ 離開 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) 回呼會用來同步處理 IGMP 和路由通訊協定之間的轉送。

 

 




