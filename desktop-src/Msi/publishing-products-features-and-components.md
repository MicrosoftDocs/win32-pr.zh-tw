---
description: 若要發佈產品、元件或功能，請使用其中一個發佈動作。
ms.assetid: 2c395d81-4f46-444e-a275-7a5d806e473c
title: 發佈產品、功能和元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdd8c8445491646399c7d118a69ae497d27faff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192649"
---
# <a name="publishing-products-features-and-components"></a><span data-ttu-id="ca8ca-103">發佈產品、功能和元件</span><span class="sxs-lookup"><span data-stu-id="ca8ca-103">Publishing Products, Features, and Components</span></span>

<span data-ttu-id="ca8ca-104">若要 [發佈](components-and-features.md) 產品、元件或功能，請使用其中一個發佈動作。</span><span class="sxs-lookup"><span data-stu-id="ca8ca-104">To [publish](components-and-features.md) a product, component, or feature, use one of the publishing actions.</span></span> <span data-ttu-id="ca8ca-105">[PublishProduct 動作](publishproduct-action.md)會向系統註冊產品資訊。</span><span class="sxs-lookup"><span data-stu-id="ca8ca-105">The [PublishProduct action](publishproduct-action.md) registers the product information with the system.</span></span> <span data-ttu-id="ca8ca-106">執行 PublishProduct 動作之後，請使用 [PublishComponents 動作](publishcomponents-action.md)來發行元件，而該動作接著會使用 [PublishComponent 資料表](publishcomponent-table.md) 來判斷設定為已公告的元件。</span><span class="sxs-lookup"><span data-stu-id="ca8ca-106">After executing the PublishProduct action, publish the components with the [PublishComponents action](publishcomponents-action.md), which in turn uses the [PublishComponent table](publishcomponent-table.md) to determine the components that are set as advertised.</span></span> <span data-ttu-id="ca8ca-107">若要以每個功能為基礎來發佈，請叫用 [PublishFeatures 動作](publishfeatures-action.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8ca-107">To publish on a per-feature basis, invoke the [PublishFeatures action](publishfeatures-action.md).</span></span> <span data-ttu-id="ca8ca-108">此動作會使用 [FeatureComponents 資料表](featurecomponents-table.md) 做為資料，來解析已公告的功能。</span><span class="sxs-lookup"><span data-stu-id="ca8ca-108">This action uses the [FeatureComponents table](featurecomponents-table.md) as data to resolve which features are advertised.</span></span>

<span data-ttu-id="ca8ca-109">另外還有兩個對應的動作，可取消發行功能或元件： [UnpublishComponents 動作](unpublishcomponents-action.md) 和 [UnpublishFeatures 動作](unpublishfeatures-action.md)。</span><span class="sxs-lookup"><span data-stu-id="ca8ca-109">There are also two corresponding actions that unpublish a feature or a component: the [UnpublishComponents action](unpublishcomponents-action.md) and the [UnpublishFeatures action](unpublishfeatures-action.md).</span></span>

 

 



