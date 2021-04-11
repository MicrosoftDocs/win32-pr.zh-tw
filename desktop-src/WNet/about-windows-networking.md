---
title: 關於 Windows 網路
description: 應用程式可以使用 WNet 函式來新增和取消網路連接，以及取得目前網路設定的相關資訊。
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- Windows 網路 WNet，描述
- WNet WNet，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91f7c8f58d4e44439bac18a2b7d7b850b21f955
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022054"
---
# <a name="about-windows-networking"></a><span data-ttu-id="dfde6-105">關於 Windows 網路</span><span class="sxs-lookup"><span data-stu-id="dfde6-105">About Windows Networking</span></span>

<span data-ttu-id="dfde6-106">應用程式可以使用 WNet 函式來新增和取消網路連接，以及取得目前網路設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dfde6-106">Applications can use the WNet functions to add and cancel network connections and to retrieve information about the current configuration of the network.</span></span>

<span data-ttu-id="dfde6-107">下圖顯示一般網路的結構。</span><span class="sxs-lookup"><span data-stu-id="dfde6-107">The following figure shows the structure of a typical network.</span></span>

![一般網路結構](images/csnet-01.png)

<span data-ttu-id="dfde6-109">在上圖中，Windows NT Server/Windows 2000 伺服器資源的階層會詳細提供為網路提供者 \# 1。</span><span class="sxs-lookup"><span data-stu-id="dfde6-109">In the preceding figure, the hierarchy for Windows NT Server/Windows 2000 Server resources is given in detail as Network provider \#1.</span></span> <span data-ttu-id="dfde6-110">來自其他提供者的網路資源具有不同的階層式系統。</span><span class="sxs-lookup"><span data-stu-id="dfde6-110">Network resources from other providers have different hierarchical systems.</span></span> <span data-ttu-id="dfde6-111">應用程式開始使用網路之前，不需要階層的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dfde6-111">An application does not need information about the hierarchy before it begins to work with a network.</span></span> <span data-ttu-id="dfde6-112">它可以從網路根目錄進行 (也就是最上層的容器資源) ，並在需要資訊時取得網路資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dfde6-112">It can proceed from the network root (that is, the topmost container resource) and retrieve information about the network's resources as the information is required.</span></span>

<span data-ttu-id="dfde6-113">包含其他資源的網路資源稱為「 *容器*」（container）。</span><span class="sxs-lookup"><span data-stu-id="dfde6-113">Network resources that contain other resources are called *containers*.</span></span> <span data-ttu-id="dfde6-114">容器資源是上圖中的方塊。</span><span class="sxs-lookup"><span data-stu-id="dfde6-114">Container resources are in boxes in the preceding figure.</span></span>

<span data-ttu-id="dfde6-115">不包含其他資源的資源稱為 *物件*。</span><span class="sxs-lookup"><span data-stu-id="dfde6-115">Resources that do not contain other resources are called *objects*.</span></span> <span data-ttu-id="dfde6-116">在上圖中，Sharepoint \# 1 和 sharepoint \# 2 是物件。</span><span class="sxs-lookup"><span data-stu-id="dfde6-116">In the preceding figure, Sharepoint \#1 and Sharepoint \#2 are objects.</span></span> <span data-ttu-id="dfde6-117">*Sharepoint* 是可在網路上存取的物件。</span><span class="sxs-lookup"><span data-stu-id="dfde6-117">A *sharepoint* is an object that is accessible across the network.</span></span> <span data-ttu-id="dfde6-118">Sharepoints 的範例包括印表機和共用目錄。</span><span class="sxs-lookup"><span data-stu-id="dfde6-118">Examples of sharepoints include printers and shared directories.</span></span>

 

 




