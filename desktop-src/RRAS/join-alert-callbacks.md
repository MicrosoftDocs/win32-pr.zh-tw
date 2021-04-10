---
title: 加入警示回呼
description: 當多播群組管理員收到介面上群組有新的接收者存在時，多播群組管理員會叫用 PMGM \_ 聯結 \_ 警示 \_ 回呼回呼。
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00dc70160b99c3cfc0e41078a3bd5882d930f31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021664"
---
# <a name="join-alert-callbacks"></a>加入警示回呼

當多播群組管理員收到介面上群組有新的接收者存在時，多播群組管理員會 [**叫用 PMGM \_ 聯結 \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) 回呼。 此回呼會通知路由通訊協定新的主機已加入指定的群組。 因此，路由通訊協定必須要求回呼所指定之群組的多播資料。

多播群組管理員會使用一組預先定義的規則，用來判斷叫用此回呼的時間。 這組規則是根據用戶端傳送的聯結要求類型，以及接收聯結要求的順序。

## <a name="wildcard-join-requests"></a>萬用字元加入要求

當群組的萬用字元聯結 (時 \* ，會從第一個用戶端收到 g) ，多播群組管理員會叫用 [**PMGM \_ 聯結 \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) 回呼給所有其他已註冊的用戶端。 從第二個用戶端收到群組的萬用字元聯結時，多播群組管理員會叫用此回呼給第一個用戶端以加入群組。

## <a name="source-specific-join-requests"></a>Source-Specific 加入要求

多播群組管理員不會對群組的任何後續聯結叫用此回呼。

當收到群組 (s、g) 的來源特定聯結時，多播群組管理員只會針對擁有來源 s 連入介面的用戶端叫用 [**PMGM \_ 聯結 \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) 回呼。

 

 




