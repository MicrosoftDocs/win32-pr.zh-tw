---
description: 網路監視器使用三種類型的二進位大型物件 (Blob) 選取並連接網路介面卡 (Nic) 、捕捉資料和操作 NPP 資料。
ms.assetid: f7cbceb1-1a85-4a05-8420-90b32c9c9b61
title: BLOB 類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029c375c446d53074cc0c9797dfa2992b2b2d933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195078"
---
# <a name="blob-types"></a><span data-ttu-id="60a4f-103">BLOB 類型</span><span class="sxs-lookup"><span data-stu-id="60a4f-103">BLOB Types</span></span>

<span data-ttu-id="60a4f-104">網路監視器使用三種類型的二進位大型物件 (Blob) 選取並連接網路介面卡 (Nic) 、捕捉資料和操作 NPP 資料。</span><span class="sxs-lookup"><span data-stu-id="60a4f-104">Network Monitor uses three types of binary large objects (BLOBs) to select and connect network interface cards (NICs), capture data, and manipulate NPP data.</span></span>

## <a name="npp-blob"></a><span data-ttu-id="60a4f-105">NPP BLOB</span><span class="sxs-lookup"><span data-stu-id="60a4f-105">NPP BLOB</span></span>

<span data-ttu-id="60a4f-106">應用程式會使用 NPP Blob 透過 NPP 連接到特定的 NIC。</span><span class="sxs-lookup"><span data-stu-id="60a4f-106">Applications use NPP BLOBs to connect to a specific NIC through an NPP.</span></span> <span data-ttu-id="60a4f-107"> (應用程式會對 NPP BLOB 中 **CreateNPPInterface** 和位置資料的呼叫進行連線。應用程式 ) 應用程式也可以將其設定資料儲存在 NPP BLOB 中，以設定 NPP。</span><span class="sxs-lookup"><span data-stu-id="60a4f-107">(The application makes the connection with a call to **CreateNPPInterface** and location data in the NPP BLOB.) An application can also store its configuration data in the NPP BLOB to configure the NPP.</span></span> <span data-ttu-id="60a4f-108">此外，儲存其 NPP BLOB 的應用程式不需要經過搜尋工具即可重複使用該 BLOB。</span><span class="sxs-lookup"><span data-stu-id="60a4f-108">Also, an application that saves its NPP BLOB is not required to go through the Finder to reuse that BLOB.</span></span>

## <a name="filter-blob"></a><span data-ttu-id="60a4f-109">篩選 BLOB</span><span class="sxs-lookup"><span data-stu-id="60a4f-109">Filter BLOB</span></span>

<span data-ttu-id="60a4f-110">篩選 BLOB 包含應用程式定義的準則，您可以用來選取 NPP 和 NIC。</span><span class="sxs-lookup"><span data-stu-id="60a4f-110">A filter BLOB contains application-defined criteria that you can use to select an NPP and a NIC.</span></span> <span data-ttu-id="60a4f-111">例如，應用程式可以要求特定的 NIC、只有乙太網路卡，或支援特定畫面格捕獲速率的卡片。</span><span class="sxs-lookup"><span data-stu-id="60a4f-111">For example, an application can request a specific NIC, only Ethernet cards, or cards that support a specific frame capture rate.</span></span>

## <a name="special-blob"></a><span data-ttu-id="60a4f-112">特殊 BLOB</span><span class="sxs-lookup"><span data-stu-id="60a4f-112">Special BLOB</span></span>

<span data-ttu-id="60a4f-113">當 NPP 需要額外的資料才能將 NPP BLOB 傳回給應用程式時，NPP 會使用特殊的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="60a4f-113">When an NPP requires additional data before it can return an NPP BLOB to an application, the NPP uses a special BLOB.</span></span> <span data-ttu-id="60a4f-114">最常見的情況是，應用程式不需要或使用特殊的 Blob，除非在一個函式呼叫中設定特定的旗標，否則不會將它們傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="60a4f-114">Most often, the application will not need or use special BLOBs so they are not returned to an application unless a specific flag is set in one function call.</span></span> <span data-ttu-id="60a4f-115">例如，遠端 NPP 會使用特殊的 BLOB，因為需要路徑名稱才能建立連接。</span><span class="sxs-lookup"><span data-stu-id="60a4f-115">For example, a remote NPP uses a special BLOB because a path name is required to make a connection.</span></span> <span data-ttu-id="60a4f-116">接收遠端 NPP 特殊 BLOB 的應用程式可以將字串加回搜尋工具，以取得 NPP BLOB 資料表。</span><span class="sxs-lookup"><span data-stu-id="60a4f-116">An application that receives a remote NPP special BLOB could add the string and call back into the Finder to get an NPP BLOB table.</span></span> <span data-ttu-id="60a4f-117">如需詳細資訊，請參閱 [特殊 BLOB 專案](special-blob-entries.md)。</span><span class="sxs-lookup"><span data-stu-id="60a4f-117">For more information, see [Special BLOB Entries](special-blob-entries.md).</span></span>

 

 



