---
title: 正在中斷連線
description: 當 RAS 用戶端應用程式啟動連接作業時，RasDial 呼叫會收到 HRASCONN 連接控制碼來識別連接。
ms.assetid: a0fddc69-44bb-4bb0-ae57-ebecbe85cbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859a3751bcbaf7d95927cdf6d14de859ddcc731e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024013"
---
# <a name="disconnecting"></a><span data-ttu-id="6e241-103">正在中斷連線</span><span class="sxs-lookup"><span data-stu-id="6e241-103">Disconnecting</span></span>

<span data-ttu-id="6e241-104">當 RAS 用戶端應用程式啟動連接作業時， [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫會收到 **HRASCONN** 連接控制碼來識別連接。</span><span class="sxs-lookup"><span data-stu-id="6e241-104">When a RAS client application starts a connection operation, the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call receives an **HRASCONN** connection handle to identify the connection.</span></span> <span data-ttu-id="6e241-105">如果傳回的控制碼不是 **Null**，用戶端最後必須呼叫 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) 函數來結束連接。</span><span class="sxs-lookup"><span data-stu-id="6e241-105">If the returned handle is not **NULL**, the client must eventually call the [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) function to end the connection.</span></span> <span data-ttu-id="6e241-106">如果連接作業期間發生錯誤，用戶端必須呼叫 **RasHangUp** ，即使從未建立連接也是一樣。</span><span class="sxs-lookup"><span data-stu-id="6e241-106">If an error occurs during the connection operation, the client must call **RasHangUp** even though the connection was never established.</span></span>

<span data-ttu-id="6e241-107">呼叫 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) 的應用程式應該不會立即結束，因為遠端存取連線管理員需要時間才能正確地終止連接。</span><span class="sxs-lookup"><span data-stu-id="6e241-107">The application that calls [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) should not exit immediately because the Remote Access Connection Manager needs time to properly terminate the connection.</span></span> <span data-ttu-id="6e241-108">相反地，應用程式應該等候，直到 [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) 函式傳回錯誤 \_ \_ 的無效控制碼，指出已刪除連接。</span><span class="sxs-lookup"><span data-stu-id="6e241-108">Instead, the application should wait until the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function returns ERROR\_INVALID\_HANDLE, indicating that the connection has been deleted.</span></span>

<span data-ttu-id="6e241-109">RAS 用戶端應用程式可能需要結束連接，即使它沒有 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)傳回的控制碼也一樣。</span><span class="sxs-lookup"><span data-stu-id="6e241-109">A RAS client application might need to end a connection even though it does not have the handle returned by [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span></span> <span data-ttu-id="6e241-110">例如，在成功建立連接之後，呼叫 **RasDial** 的應用程式可能已經結束。</span><span class="sxs-lookup"><span data-stu-id="6e241-110">For example, the application that called **RasDial** might have exited after the connection was successfully established.</span></span> <span data-ttu-id="6e241-111">在此情況下，中斷連接的應用程式可以使用 [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) 函式來取得所有目前的連接。</span><span class="sxs-lookup"><span data-stu-id="6e241-111">In this case, the disconnecting application can use the [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) function to get all the current connections.</span></span> <span data-ttu-id="6e241-112">針對每個連線， **RasEnumConnections** 會傳回 [**RASCONN**](/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)) 結構，其中包含 **HRASCONN** 連接控制碼，以及啟動連接作業時指定的電話簿專案名稱或電話號碼。</span><span class="sxs-lookup"><span data-stu-id="6e241-112">For each connection, **RasEnumConnections** returns a [**RASCONN**](/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)) structure that contains the **HRASCONN** connection handle and the phone-book entry name or phone number specified when the connection operation was started.</span></span> <span data-ttu-id="6e241-113">這項資訊可以用來顯示連接清單，使用者可以從中選取連線以結束。</span><span class="sxs-lookup"><span data-stu-id="6e241-113">This information can be used to display a list of connections from which the user can select the connection to end.</span></span>

 

 