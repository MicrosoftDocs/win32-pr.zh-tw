---
description: 部署以加快通訊速度
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: 部署以加快通訊速度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972797"
---
# <a name="deploying-for-faster-communication"></a><span data-ttu-id="06f06-103">部署以加快通訊速度</span><span class="sxs-lookup"><span data-stu-id="06f06-103">Deploying for Faster Communication</span></span>

<span data-ttu-id="06f06-104">在部署 COM + 應用程式時，效能是一個重要的考慮，而元件位置是從設計完善的應用程式取得最佳效能的關鍵。</span><span class="sxs-lookup"><span data-stu-id="06f06-104">Performance is a key consideration when deploying a COM+ application, and component location is the key to getting the best performance from a well-designed application.</span></span>

<span data-ttu-id="06f06-105">只要將應用程式的主要元件移到更快的硬體，就可以解決效能問題。</span><span class="sxs-lookup"><span data-stu-id="06f06-105">It was once widely held that with scalable application architectures, performance could be addressed by simply moving primary components of the application to faster hardware.</span></span> <span data-ttu-id="06f06-106">這已證明不成立。</span><span class="sxs-lookup"><span data-stu-id="06f06-106">This has proven not to be true.</span></span> <span data-ttu-id="06f06-107">效能問題不是來自個別元件效能，而是從連接元件的連結所引發。</span><span class="sxs-lookup"><span data-stu-id="06f06-107">Performance problems arise not from individual component performance but from the links connecting components.</span></span>

<span data-ttu-id="06f06-108">成功的主要因素是位置。</span><span class="sxs-lookup"><span data-stu-id="06f06-108">The primary factor for success is location.</span></span> <span data-ttu-id="06f06-109">鄰近性或實體位置、時間、容量和用途是適用于 COM + 應用程式部署之位置的不同層面，全都會影響效能。</span><span class="sxs-lookup"><span data-stu-id="06f06-109">Proximity or physical location, time, capacity, and purpose are distinct aspects of location that apply to the deployment of a COM+ application, all of which affect performance.</span></span>

<span data-ttu-id="06f06-110">當應用程式元件和資源經過設計和部署，以符合應用程式工作負載所放置的需求時，效能最佳。</span><span class="sxs-lookup"><span data-stu-id="06f06-110">The best performance comes when the application components and resources are designed and deployed to match the demands placed upon them by the application workload.</span></span>

<span data-ttu-id="06f06-111">一般而言，您應該部署元件以將跨進程（尤其是跨電腦）元件之間的通訊降至最低。</span><span class="sxs-lookup"><span data-stu-id="06f06-111">In general, you should deploy components to minimize cross-process, and especially cross-computer, communication between components.</span></span> <span data-ttu-id="06f06-112">如果您的應用程式設計很有效率，元件內的類別會使用和函式進行分組，以最大化元件內的通訊。</span><span class="sxs-lookup"><span data-stu-id="06f06-112">If your application design is efficient, classes within a component are grouped by use and function to maximize communications within components.</span></span> <span data-ttu-id="06f06-113">在部署元件中，您必須確保元件在邏輯上會使用元件之間的關聯性，並減少元件之間的訊息量。</span><span class="sxs-lookup"><span data-stu-id="06f06-113">In deploying components, you need to ensure that the components are logically located to make use of the relationships between the components and to reduce the amount of messaging between components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06f06-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="06f06-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06f06-115">設計部署</span><span class="sxs-lookup"><span data-stu-id="06f06-115">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> </dl>

 

 



