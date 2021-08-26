---
title: 本機聯結回呼
description: 在 IGMP 通知多播群組管理員之後，介面上的群組有新的接收者存在時，多播群組管理員會叫用 PMGM \_ 本機 \_ 聯結 \_ 回呼回呼給擁有介面的路由通訊協定（如果有的話）。
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b3464aa645a6ab110acef09f238ffca97f781a38cc6c2602a39e7c66316490
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074068"
---
# <a name="local-join-callbacks"></a>本機聯結回呼

在 IGMP 通知多播群組管理員之後，介面上的群組有新的接收者存在時，多播群組管理員會叫用 [**PMGM \_ 本機 \_ 聯結 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) 回呼給擁有介面的路由通訊協定（如果有的話）。 此回呼會通知路由通訊協定的變更。

此回呼和 [**PMGM \_ 本地 \_ 離開 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) 回呼會用來同步處理 IGMP 和路由通訊協定之間的轉送。

 

 




