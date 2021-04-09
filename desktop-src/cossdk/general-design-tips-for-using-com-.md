---
description: 設計良好的關鍵是規劃。 如果您不熟悉如何設計三層式應用程式，請參閱使用 UML 設計 COM + 應用程式一節。
ms.assetid: 463f4154-92f6-46c3-95ff-8513963dcadd
title: 使用 COM + 的一般設計秘訣
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5765259f170b1a98f1abb2d097dfdaec2e09d47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110557"
---
# <a name="general-design-tips-for-using-com"></a><span data-ttu-id="d8d11-104">使用 COM + 的一般設計秘訣</span><span class="sxs-lookup"><span data-stu-id="d8d11-104">General Design Tips for Using COM+</span></span>

<span data-ttu-id="d8d11-105">設計良好的關鍵是規劃。</span><span class="sxs-lookup"><span data-stu-id="d8d11-105">The key to good design is planning.</span></span> <span data-ttu-id="d8d11-106">如果您不熟悉如何設計三層式應用程式，請參閱 [使用 UML 設計 COM + 應用程式](designing-the-com--application-using-uml.md)一節。</span><span class="sxs-lookup"><span data-stu-id="d8d11-106">If you are unfamiliar with designing a three-tier application, see the section entitled [Designing the COM+ Application Using UML](designing-the-com--application-using-uml.md).</span></span>

<span data-ttu-id="d8d11-107">您如何建立組成 COM + 應用程式中介層的 COM 元件，可能會大幅影響效能、擴充性和部署的便利性。</span><span class="sxs-lookup"><span data-stu-id="d8d11-107">How you construct the COM components that make up the middle tier of your COM+ application can dramatically affect performance, scalability, and ease of deployment.</span></span> <span data-ttu-id="d8d11-108">下列主題提供設計 COM 元件時，您應該瞭解的設計考慮和執行秘訣。</span><span class="sxs-lookup"><span data-stu-id="d8d11-108">The following topics provide design considerations and implementation tips you should know about when designing COM components.</span></span>



| <span data-ttu-id="d8d11-109">主題</span><span class="sxs-lookup"><span data-stu-id="d8d11-109">Topic</span></span>                                                                   | <span data-ttu-id="d8d11-110">描述</span><span class="sxs-lookup"><span data-stu-id="d8d11-110">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8d11-111">擴充性設計</span><span class="sxs-lookup"><span data-stu-id="d8d11-111">Designing for Scalability</span></span>](designing-for-scalability.md)<br/>   | <span data-ttu-id="d8d11-112">建議增加 COM + 應用程式擴充性的方式。</span><span class="sxs-lookup"><span data-stu-id="d8d11-112">Suggests ways to increase the scalability of your COM+ application.</span></span><br/>                                             |
| [<span data-ttu-id="d8d11-113">可用性設計</span><span class="sxs-lookup"><span data-stu-id="d8d11-113">Designing for Availability</span></span>](designing-for-availability.md)<br/> | <span data-ttu-id="d8d11-114">討論您可以用來改善在 COM + 應用程式中中介層功能可用性的服務。</span><span class="sxs-lookup"><span data-stu-id="d8d11-114">Discusses services you can use to improve the availability your middle-tier functionality in COM+ applications.</span></span><br/> |
| [<span data-ttu-id="d8d11-115">安全性設計</span><span class="sxs-lookup"><span data-stu-id="d8d11-115">Designing for Security</span></span>](designing-for-security.md)<br/>         | <span data-ttu-id="d8d11-116">討論最有效率地設定 COM + 應用程式安全性的方式。</span><span class="sxs-lookup"><span data-stu-id="d8d11-116">Discusses ways to most efficiently set up security for a COM+ application.</span></span><br/>                                      |
| [<span data-ttu-id="d8d11-117">設計部署</span><span class="sxs-lookup"><span data-stu-id="d8d11-117">Designing for Deployment</span></span>](designing-for-deployment.md)<br/>     | <span data-ttu-id="d8d11-118">討論在設計分散式應用程式時，將部署的麻煩降至最低的方式。</span><span class="sxs-lookup"><span data-stu-id="d8d11-118">Discusses ways to minimize deployment headaches when designing a distributed application.</span></span><br/>                       |



 

<span data-ttu-id="d8d11-119">此外，也請務必瞭解如何使用 [物件共用改善效能](improving-performance-with-object-pooling.md) ，以取得最有效使用物件共用的方法。</span><span class="sxs-lookup"><span data-stu-id="d8d11-119">Also, be sure to see [Improving Performance with Object Pooling](improving-performance-with-object-pooling.md) for ways to most effectively use object pooling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8d11-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8d11-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8d11-121">COM + 設計假設和原則</span><span class="sxs-lookup"><span data-stu-id="d8d11-121">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="d8d11-122">使用 UML 設計 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="d8d11-122">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="d8d11-123">優化與 COM + 商務邏輯層的互動</span><span class="sxs-lookup"><span data-stu-id="d8d11-123">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="d8d11-124">用來建立分散式應用程式的其他 Microsoft 工具</span><span class="sxs-lookup"><span data-stu-id="d8d11-124">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 




