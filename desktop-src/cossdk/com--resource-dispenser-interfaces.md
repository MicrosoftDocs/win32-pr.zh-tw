---
description: COM + 資源配置器介面
ms.assetid: 66ee4dd6-15d2-49e8-89a3-6fbb5770cabf
title: COM + 資源配置器介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a6ea5c5c09f67f86b42ebf5b881f1d19ad1501
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847160"
---
# <a name="com-resource-dispenser-interfaces"></a><span data-ttu-id="e4705-103">COM + 資源配置器介面</span><span class="sxs-lookup"><span data-stu-id="e4705-103">COM+ Resource Dispenser Interfaces</span></span>

<span data-ttu-id="e4705-104">應用程式元件使用資源機來存取共用資訊。</span><span class="sxs-lookup"><span data-stu-id="e4705-104">Application components use resource dispensers to access shared information.</span></span> <span data-ttu-id="e4705-105">下表所述的介面提供資源機開發人員的詳細參考資訊。</span><span class="sxs-lookup"><span data-stu-id="e4705-105">The interfaces described in the following table provide detailed reference information for developers of resource dispensers.</span></span>



| <span data-ttu-id="e4705-106">介面</span><span class="sxs-lookup"><span data-stu-id="e4705-106">Interfaces</span></span>                                                | <span data-ttu-id="e4705-107">Description</span><span class="sxs-lookup"><span data-stu-id="e4705-107">Description</span></span>                                                                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4705-108">**IDispenserDriver**</span><span class="sxs-lookup"><span data-stu-id="e4705-108">**IDispenserDriver**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)<br/>   | <span data-ttu-id="e4705-109">資源配置器持有者會呼叫此介面來建立、登錄、評估和終結資源。</span><span class="sxs-lookup"><span data-stu-id="e4705-109">This interface is called by the resource dispenser holder to create, enlist, evaluate, and destroy a resource.</span></span><br/> |
| [<span data-ttu-id="e4705-110">**IDispenserManager**</span><span class="sxs-lookup"><span data-stu-id="e4705-110">**IDispenserManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager)<br/> | <span data-ttu-id="e4705-111">資源機使用此介面連接到分配器管理員。</span><span class="sxs-lookup"><span data-stu-id="e4705-111">Resource dispensers use this interface to connect to the dispenser manager.</span></span><br/>                                    |
| [<span data-ttu-id="e4705-112">**IHolder**</span><span class="sxs-lookup"><span data-stu-id="e4705-112">**IHolder**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)<br/>                     | <span data-ttu-id="e4705-113">此介面是用來準備和處理資源。</span><span class="sxs-lookup"><span data-stu-id="e4705-113">This interface is used to prepare and handle resources.</span></span><br/>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="e4705-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4705-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4705-115">COM + 資源配置器概念</span><span class="sxs-lookup"><span data-stu-id="e4705-115">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="e4705-116">COM + 資源配置器介面中使用的類型</span><span class="sxs-lookup"><span data-stu-id="e4705-116">Types Used in COM+ Resource Dispenser Interfaces</span></span>](types-used-in-com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 




