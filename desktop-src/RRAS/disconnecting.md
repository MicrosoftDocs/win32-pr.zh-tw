---
title: 正在中斷連線
description: 當 RAS 用戶端應用程式啟動連接作業時，RasDial 呼叫會收到 HRASCONN 連接控制碼來識別連接。
ms.assetid: a0fddc69-44bb-4bb0-ae57-ebecbe85cbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fde205dfeb838639447c9f9359ee5b1258b2426eb55dbdd592291aea002fad6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101858"
---
# <a name="disconnecting"></a>正在中斷連線

當 RAS 用戶端應用程式啟動連接作業時， [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫會收到 **HRASCONN** 連接控制碼來識別連接。 如果傳回的控制碼不是 **Null**，用戶端最後必須呼叫 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) 函數來結束連接。 如果連接作業期間發生錯誤，用戶端必須呼叫 **RasHangUp** ，即使從未建立連接也是一樣。

呼叫 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) 的應用程式應該不會立即結束，因為遠端存取連線管理員需要時間才能正確地終止連接。 相反地，應用程式應該等候，直到 [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) 函式傳回錯誤 \_ \_ 的無效控制碼，指出已刪除連接。

RAS 用戶端應用程式可能需要結束連接，即使它沒有 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)傳回的控制碼也一樣。 例如，在成功建立連接之後，呼叫 **RasDial** 的應用程式可能已經結束。 在此情況下，中斷連接的應用程式可以使用 [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) 函式來取得所有目前的連接。 針對每個連線， **RasEnumConnections** 會傳回 [**RASCONN**](/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)) 結構，其中包含 **HRASCONN** 連接控制碼，以及啟動連接作業時指定的電話簿專案名稱或電話號碼。 這項資訊可以用來顯示連接清單，使用者可以從中選取連線以結束。

 

 