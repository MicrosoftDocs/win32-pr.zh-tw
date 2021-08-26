---
title: 剪除警示回呼
description: 當多播群組管理員收到通知接收者將群組留在介面上時，多播群組管理員會叫用 PMGM 剪除 \_ \_ 警示 \_ 回呼回呼。
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5aa4d95742a2976ea46367b0f1af9442528c2821dc9d27b09b9e1c29eee6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036397"
---
# <a name="prune-alert-callbacks"></a>剪除警示回呼

當多播群組管理員收到通知接收者將群組留在介面上時，多播群組管理員會叫用 PMGM 剪除 [**\_ \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) 回呼。 此回呼會通知路由通訊協定，用戶端不再屬於指定的群組。 因此，路由通訊協定必須停止要求指定群組的多播資料。

多播群組管理員有一組預先定義的規則，用來判斷叫用此回呼的時間。 這些規則是根據用戶端所傳送的剪除要求類型，以及在中收到剪除要求的順序。

## <a name="wildcard-prune-requests"></a>萬用字元剪除要求

當針對群組 (的萬用字元剪除時 \* ，會收到 g) ，而且會為第二個用戶端移除最後一個介面 (也就是說，當只有單一用戶端的介面保持) 時，多播群組管理員會叫用 PMGM 剪除 [**\_ \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) 回呼至剩餘的用戶端。 移除最後一個用戶端的最終介面之後 (也就是，當沒有其他介面仍) 時，就會針對已向多播群組管理員註冊的所有其他用戶端叫用此回呼。

## <a name="source-specific-prune-requests"></a>Source-Specific 剪除要求

當群組的來源特定剪除 (s，會收到 g) ，多播群組管理員只會針對擁有來源 s 傳入介面的用戶端叫用 [**PMGM 剪除 \_ \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) 回呼。

 

 




