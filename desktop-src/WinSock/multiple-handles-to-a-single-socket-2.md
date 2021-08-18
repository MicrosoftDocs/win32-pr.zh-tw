---
description: 由於複製的內容是通訊端描述項，而不是基礎通訊端，因此與通訊端相關聯的所有狀態都會保留在所有描述項的通用範圍內。
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: 單一通訊端的多個控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e402d19c3306158a905f2e9ddc263649e52d214a3d9441509e7a277f7d2800
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121398"
---
# <a name="multiple-handles-to-a-single-socket"></a>單一通訊端的多個控制碼

由於複製的內容是通訊端描述項，而不是基礎通訊端，因此與通訊端相關聯的所有狀態都會保留在所有描述項的通用範圍內。 例如，使用一個描述項執行的 [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) 作業，之後會使用來自任何或所有描述項的 [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) 來顯示。

共用通訊端上的通知會受到 [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) 和 [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))的一般限制。 使用任何共用描述項來發出上述其中一項呼叫，就會取消通訊端先前的任何事件註冊，無論使用哪一個描述項進行註冊。 例如，可能無法讓進程收到「接收 FD \_ 讀取事件」和「進程 B 接收 fd」 \_ 寫入事件。 在需要這類緊密協調的情況下，建議開發人員考慮使用執行緒，而不是個別的進程。

 

 
