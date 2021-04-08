---
title: 連線管理員
description: 如果客戶想要使用遠端存取服務 API 開發自訂的撥號，可能會想要調查 Microsoft 連線管理員和連線管理員系統管理組件。
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7959482542630b6dc90149971df08f7944f83fc
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104023106"
---
# <a name="connection-manager"></a><span data-ttu-id="a7a95-103">連線管理員</span><span class="sxs-lookup"><span data-stu-id="a7a95-103">Connection Manager</span></span>

<span data-ttu-id="a7a95-104">如果客戶想要使用遠端存取服務 API 開發自訂的撥號，可能會想要調查 Microsoft 連線管理員和連線管理員系統管理組件。</span><span class="sxs-lookup"><span data-stu-id="a7a95-104">Customers who intend to develop custom dialers using the Remote Access Service API may want to investigate Microsoft Connection Manager and the Connection Manager Administration Kit.</span></span> <span data-ttu-id="a7a95-105">連線管理員是 Microsoft 的受控遠端存取用戶端。</span><span class="sxs-lookup"><span data-stu-id="a7a95-105">Connection Manager is Microsoft's managed remote access client.</span></span> <span data-ttu-id="a7a95-106">它可讓系統管理員建立遠端存取設定套件，以散發給系統管理員的遠端使用者。</span><span class="sxs-lookup"><span data-stu-id="a7a95-106">It allows an administrator to build a remote access configuration package to be distributed to the administrator's remote users.</span></span> <span data-ttu-id="a7a95-107">如需有關連線管理員和連線管理員系統管理組件的詳細資訊，請參閱 Microsoft Windows 2000 Server 和更新版本作業系統的線上說明。</span><span class="sxs-lookup"><span data-stu-id="a7a95-107">For more information on Connection Manager and the Connection Manager Administration Kit, see the online help for Microsoft Windows 2000 Server and later operating systems.</span></span>

<span data-ttu-id="a7a95-108">您可以在完整的平臺軟體發展工具組 (SDK) 中找到範例連線管理員自訂動作的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="a7a95-108">You can find the source code for a sample Connection Manager custom action in the complete Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="a7a95-109">您可以從 [Microsoft 網站](https://msdn.microsoft.com/windowsserver/bb980924.aspx)下載 Platform SDK。</span><span class="sxs-lookup"><span data-stu-id="a7a95-109">The Platform SDK can be downloaded at the [Microsoft Web site](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="a7a95-110">安裝之後，範例程式碼的路徑為% Install Path% \\ MICROSOFT SDK \\ sample \\ netds \\ Ras \\ ConnectionManager，其中% INSTALL path% 指定 Platform SDK 的基底安裝目錄 (例如 C： \\ Program Files) 。</span><span class="sxs-lookup"><span data-stu-id="a7a95-110">After installation, the path to the sample code is %Install Path%\\Microsoft SDK\\Samples\\netds\\Ras\\ConnectionManager, where %Install Path% designates the base installation directory of the Platform SDK (for example, C:\\Program Files).</span></span>

<span data-ttu-id="a7a95-111">自訂動作可讓遠端存取用戶端在連線程式的不同點上採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="a7a95-111">Custom actions make it possible for the remote access client to take specific actions at various points in the connection process.</span></span> <span data-ttu-id="a7a95-112">範例中示範的自訂動作會根據連接的伺服器位址，自動調整連線的 proxy 伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="a7a95-112">The custom action demonstrated in the sample automatically adjusts the proxy server configuration for a connection based on the connection's server address.</span></span> <span data-ttu-id="a7a95-113">客戶可以使用此範例作為開始建立自己自訂動作的起點。</span><span class="sxs-lookup"><span data-stu-id="a7a95-113">Customers can use this sample as a starting point for creating their own custom actions.</span></span>

 

 




