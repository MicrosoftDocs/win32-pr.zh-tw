---
description: 您可以使用 COM + 分割服務，在電腦上安裝不同版本的 COM + 應用程式，並同時執行它們。
ms.assetid: fd22a64c-f2d8-48af-86e1-985e21b0f8fa
title: COM + 磁碟分割
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd4e1efdd42ac407d8937c4090c59e65472ed69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847162"
---
# <a name="com-partitions"></a><span data-ttu-id="949ba-103">COM + 磁碟分割</span><span class="sxs-lookup"><span data-stu-id="949ba-103">COM+ Partitions</span></span>

<span data-ttu-id="949ba-104">您可以使用 COM + 分割服務，在電腦上安裝不同版本的 COM + 應用程式，並同時執行它們。</span><span class="sxs-lookup"><span data-stu-id="949ba-104">You can use the COM+ partitions service to install different versions of a COM+ application on a computer and run them simultaneously.</span></span>

<span data-ttu-id="949ba-105">**WINDOWS XP：** 無法使用建立、設定或委派 COM + 分割的能力。</span><span class="sxs-lookup"><span data-stu-id="949ba-105">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="949ba-106">全域分割區是唯一可用的 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="949ba-106">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="949ba-107">\* \* Windows 2000： \* \* COM + 分割服務無法在 Windows 2000 中使用。</span><span class="sxs-lookup"><span data-stu-id="949ba-107">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>

<span data-ttu-id="949ba-108">下列主題提供 COM + 磁碟分割服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="949ba-108">The following topics provide information about the COM+ partitions service.</span></span>



| <span data-ttu-id="949ba-109">主題</span><span class="sxs-lookup"><span data-stu-id="949ba-109">Topic</span></span>                                                               | <span data-ttu-id="949ba-110">描述</span><span class="sxs-lookup"><span data-stu-id="949ba-110">Description</span></span>                                                                 |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="949ba-111">COM + 磁碟分割概念</span><span class="sxs-lookup"><span data-stu-id="949ba-111">COM+ Partitions Concepts</span></span>](com--partitions-concepts.md)<br/> | <span data-ttu-id="949ba-112">提供使用 COM + 磁碟分割的總覽。</span><span class="sxs-lookup"><span data-stu-id="949ba-112">Provides an overview of using COM+ partitions.</span></span><br/>                   |
| [<span data-ttu-id="949ba-113">COM + 分割工作</span><span class="sxs-lookup"><span data-stu-id="949ba-113">COM+ Partitions Tasks</span></span>](com--partitions-tasks.md)<br/>       | <span data-ttu-id="949ba-114">提供建立和管理 COM + 磁碟分割的指示。</span><span class="sxs-lookup"><span data-stu-id="949ba-114">Provides instructions for creating and managing COM+ partitions.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="949ba-115">預設不會啟用 COM + 分割服務。</span><span class="sxs-lookup"><span data-stu-id="949ba-115">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="949ba-116">若要使用 COM + 分割服務，您必須透過 [元件服務] 系統管理工具啟用它，或將 [**LocalComputer**](localcomputer.md) 集合上的 PartitionsEnabled 屬性變更為 True。</span><span class="sxs-lookup"><span data-stu-id="949ba-116">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

 

 




