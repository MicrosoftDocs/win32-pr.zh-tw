---
description: 裝置重新導向功能會重新導向標準 MS-DOS 裝置、磁碟機號和 LPT 埠。 這可讓在系統上執行的應用程式使用裝置，並以完全透明的方式存取網路。
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Device-Redirecting 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577f8d108b6bfdeb01f786478cd736e6c84cc83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191154"
---
# <a name="device-redirecting-functions"></a><span data-ttu-id="5ad22-104">Device-Redirecting 函式</span><span class="sxs-lookup"><span data-stu-id="5ad22-104">Device-Redirecting Functions</span></span>

<span data-ttu-id="5ad22-105">裝置重新導向功能會重新導向標準 MS-DOS 裝置、磁碟機號和 LPT 埠。</span><span class="sxs-lookup"><span data-stu-id="5ad22-105">The device-redirecting functions redirect standard MS-DOS devices, drive letters and LPT ports.</span></span> <span data-ttu-id="5ad22-106">這可讓在系統上執行的應用程式使用裝置，並以完全透明的方式存取網路。</span><span class="sxs-lookup"><span data-stu-id="5ad22-106">This enables applications running on the system to use the devices and access the network in a totally transparent manner.</span></span>



| <span data-ttu-id="5ad22-107">函式</span><span class="sxs-lookup"><span data-stu-id="5ad22-107">Function</span></span>                                                         | <span data-ttu-id="5ad22-108">描述</span><span class="sxs-lookup"><span data-stu-id="5ad22-108">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ad22-109">**NPAddConnection**</span><span class="sxs-lookup"><span data-stu-id="5ad22-109">**NPAddConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | <span data-ttu-id="5ad22-110">將本機裝置重新導向或連接到網路資源。</span><span class="sxs-lookup"><span data-stu-id="5ad22-110">Redirects or connects a local device to a network resource.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="5ad22-111">**NPAddConnection3**</span><span class="sxs-lookup"><span data-stu-id="5ad22-111">**NPAddConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | <span data-ttu-id="5ad22-112">執行與 [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)相同的動作，但讓使用者指定應擁有任何對話方塊的視窗，以及應如何建立連接。</span><span class="sxs-lookup"><span data-stu-id="5ad22-112">Performs the same action as [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), but lets the user specify which window should own any dialog boxes and how the connection should be established.</span></span><br/> |
| [<span data-ttu-id="5ad22-113">**NPCancelConnection**</span><span class="sxs-lookup"><span data-stu-id="5ad22-113">**NPCancelConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | <span data-ttu-id="5ad22-114">中斷網路連接。</span><span class="sxs-lookup"><span data-stu-id="5ad22-114">Breaks a network connection.</span></span> <span data-ttu-id="5ad22-115">如果裝置已中斷連線，則會記住變更，除非連接是 deviceless 連線。</span><span class="sxs-lookup"><span data-stu-id="5ad22-115">The changes are remembered if a device is disconnected unless the connection is a deviceless connection.</span></span><br/>                                                    |
| [<span data-ttu-id="5ad22-116">**NPGetConnection**</span><span class="sxs-lookup"><span data-stu-id="5ad22-116">**NPGetConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | <span data-ttu-id="5ad22-117">傳回連接的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5ad22-117">Returns information about a connection.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="5ad22-118">**NPGetConnection3**</span><span class="sxs-lookup"><span data-stu-id="5ad22-118">**NPGetConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | <span data-ttu-id="5ad22-119">傳回連接的相關資訊，即使連接目前已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="5ad22-119">Returns information about a connection, even if the connection is currently disconnected.</span></span><br/>                                                                                                |
| [<span data-ttu-id="5ad22-120">**NPGetConnectionPerformance**</span><span class="sxs-lookup"><span data-stu-id="5ad22-120">**NPGetConnectionPerformance**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | <span data-ttu-id="5ad22-121">傳回連接的相關效能資訊。</span><span class="sxs-lookup"><span data-stu-id="5ad22-121">Returns performance information about a connection.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="5ad22-122">**NPGetUniversalName**</span><span class="sxs-lookup"><span data-stu-id="5ad22-122">**NPGetUniversalName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | <span data-ttu-id="5ad22-123">以函式呼叫期間指定的格式，傳回遠端或區域通用名稱。</span><span class="sxs-lookup"><span data-stu-id="5ad22-123">Returns the remote or local universal name, in the format specified during the function call.</span></span><br/>                                                                                            |



 

 

 




