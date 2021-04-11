---
description: 沒有元件的 COM + 服務
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: 沒有元件的 COM + 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eeed5a9af96e241d137714d151cc632dd0f20e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110925"
---
# <a name="com-services-without-components"></a><span data-ttu-id="3c850-103">沒有元件的 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="3c850-103">COM+ Services Without Components</span></span>

<span data-ttu-id="3c850-104">使用 COM + 1.5，您可以使用 COM + 所提供的服務，而不需要建立元件來包含呼叫這些服務的方法。</span><span class="sxs-lookup"><span data-stu-id="3c850-104">With COM+ 1.5, you can use the services provided by COM+ without needing to build a component to contain the methods that call those services.</span></span> <span data-ttu-id="3c850-105">這可大幅獲益于通常不使用元件，但想要使用 COM + 服務（例如交易或 COM + 追蹤器）的開發人員。</span><span class="sxs-lookup"><span data-stu-id="3c850-105">This greatly benefits developers who do not normally use components but want to use COM+ services such as transactions or the COM+ Tracker.</span></span> <span data-ttu-id="3c850-106">藉由使用沒有元件的 COM + 服務，開發人員可以避免建立元件的額外負荷，而此元件只會用來存取所需的 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="3c850-106">By using COM+ services without components, developers can avoid the overhead of creating a component that is used to access only the COM+ services they need.</span></span>

<span data-ttu-id="3c850-107">例如，腳本環境傳統上是 COM + 服務的最大取用者，但因為服務需要在 COM + 元件內配套，所以永遠不能有效率地使用這些服務。</span><span class="sxs-lookup"><span data-stu-id="3c850-107">For example, script environments traditionally have been the largest consumers of COM+ services but they were never able to use those services efficiently because the services needed to be bundled within a COM+ component.</span></span> <span data-ttu-id="3c850-108">這項組合需求會提高效能成本，因為腳本環境所需的資料的通訊和重復資料也會與元件互動。</span><span class="sxs-lookup"><span data-stu-id="3c850-108">This bundling requirement increased performance costs because of the increased communication and duplication of data necessary for the scripting environment to interact with the component.</span></span> <span data-ttu-id="3c850-109">使用沒有元件的服務，就會將這類成本降至最低。</span><span class="sxs-lookup"><span data-stu-id="3c850-109">By using services without components, such costs are minimized.</span></span>

<span data-ttu-id="3c850-110">下表所述的主題提供有關使用 COM + 服務而不含元件的背景和工作資訊。</span><span class="sxs-lookup"><span data-stu-id="3c850-110">The topics described in the following table provide background and task information about using COM+ services without components.</span></span> <span data-ttu-id="3c850-111">這項功能適用于關心效能的 advanced Visual C++ 開發人員。</span><span class="sxs-lookup"><span data-stu-id="3c850-111">This feature is intended for advanced Visual C++ developers who are concerned about performance.</span></span>



| <span data-ttu-id="3c850-112">主題</span><span class="sxs-lookup"><span data-stu-id="3c850-112">Topic</span></span>                                                                                                 | <span data-ttu-id="3c850-113">描述</span><span class="sxs-lookup"><span data-stu-id="3c850-113">Description</span></span>                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c850-114">沒有元件概念的 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="3c850-114">COM+ Services Without Components Concepts</span></span>](com--services-without-components-concepts.md)<br/> | <span data-ttu-id="3c850-115">概要說明如何使用不含元件的 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="3c850-115">Provides an overview of using COM+ services without components.</span></span><br/>                     |
| [<span data-ttu-id="3c850-116">沒有元件工作的 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="3c850-116">COM+ Services Without Components Tasks</span></span>](com--services-without-components-tasks.md)<br/>       | <span data-ttu-id="3c850-117">提供指示，說明如何使用 COM + 來建立及使用不含元件的服務。</span><span class="sxs-lookup"><span data-stu-id="3c850-117">Provides instructions for using COM+ to create and use services without components.</span></span><br/> |



 

 

 




