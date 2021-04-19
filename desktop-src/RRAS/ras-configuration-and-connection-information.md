---
title: RAS 設定和連接資訊
description: 在 Windows NT 4.0 和更新版本以及 Windows 95 上執行的應用程式，可以使用 RasEnumConnections 函式來取得本機電腦上現有連接的相關資訊。
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- 設定和連線，RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c4e768f4686a24857a75212e40f2e64bc91109
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966796"
---
# <a name="ras-configuration-and-connection-information"></a><span data-ttu-id="0757a-104">RAS 設定和連接資訊</span><span class="sxs-lookup"><span data-stu-id="0757a-104">RAS Configuration and Connection Information</span></span>

<span data-ttu-id="0757a-105">在 Windows NT 4.0 和更新版本以及 Windows 95 上執行的應用程式，可以使用 [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) 函式來取得本機電腦上現有連接的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0757a-105">Applications running on Windows NT 4.0 and later versions, and Windows 95, can use the [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) function to get information about the existing connections on the local computer.</span></span> <span data-ttu-id="0757a-106">每個連線的資訊包含連接控制碼，以及用來建立連線的電話簿專案名稱。</span><span class="sxs-lookup"><span data-stu-id="0757a-106">The information for each connection includes a connection handle and the name of the phone-book entry used to establish the connection.</span></span> <span data-ttu-id="0757a-107">您可以在 [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) 函數的呼叫中使用連接控制碼取得連接的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0757a-107">You can use the connection handle in a call to the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function get the current status of the connection.</span></span>

<span data-ttu-id="0757a-108">Windows NT Server 4.0 和更新版本提供兩個新功能，可供您用來抓取 RAS 資訊。</span><span class="sxs-lookup"><span data-stu-id="0757a-108">Windows NT Server 4.0 and later versions provide two new functions for retrieving RAS information.</span></span> <span data-ttu-id="0757a-109">Windows 95does 不支援這些功能。</span><span class="sxs-lookup"><span data-stu-id="0757a-109">Windows 95does not support these functions.</span></span>

<span data-ttu-id="0757a-110">[**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa)函式會傳回在本機電腦上設定且支援 RAS 之裝置的名稱和類型。</span><span class="sxs-lookup"><span data-stu-id="0757a-110">The [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) function returns the name and type of the RAS-capable devices that are configured on the local computer.</span></span>

<span data-ttu-id="0757a-111">[**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa)函式會指定事件物件，系統會在建立或終止 RAS 連接時發出通知。</span><span class="sxs-lookup"><span data-stu-id="0757a-111">The [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) function specifies an event object that the system signals when a RAS connection is created or terminated.</span></span>

 

 




