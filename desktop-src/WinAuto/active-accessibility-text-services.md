---
title: Active Accessibility 文字服務
description: 本節討論 Active Accessibility 的文字服務介面。
ms.assetid: 8bbc647f-1687-45b8-8b63-a6ea45a0a721
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe9fdb4d9d9972f93db780d274b39e587e51c03b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463392"
---
# <a name="active-accessibility-text-services"></a><span data-ttu-id="1c5c4-103">Active Accessibility 文字服務</span><span class="sxs-lookup"><span data-stu-id="1c5c4-103">Active Accessibility Text Services</span></span>

<span data-ttu-id="1c5c4-104">本節討論 Active Accessibility 的文字服務介面。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-104">This section discusses the Active Accessibility Text Services interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="1c5c4-105">Active Accessibility 的文字服務已淘汰。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-105">Active Accessibility Text Services is deprecated.</span></span> <span data-ttu-id="1c5c4-106">如需有關 advanced Text 輸入和自然語言技術的詳細資訊，請參閱 [Microsoft Windows 文字服務架構](../tsf/text-services-framework.md) 。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-106">Please see [Microsoft Windows Text Services Framework](../tsf/text-services-framework.md) for more information on advanced text input and natural language technologies.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1c5c4-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="1c5c4-107">In this section</span></span>

| <span data-ttu-id="1c5c4-108">主題</span><span class="sxs-lookup"><span data-stu-id="1c5c4-108">Topic</span></span>                                                     | <span data-ttu-id="1c5c4-109">描述</span><span class="sxs-lookup"><span data-stu-id="1c5c4-109">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c5c4-110">**IAccServerDocMgr**</span><span class="sxs-lookup"><span data-stu-id="1c5c4-110">**IAccServerDocMgr**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-iaccserverdocmgr)   | <span data-ttu-id="1c5c4-111">公開可讓用戶端應用程式存取檔的方法。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-111">Exposes methods that make documents accessible to client applications.</span></span>                              |
| [<span data-ttu-id="1c5c4-112">**IAccClientDocMgr**</span><span class="sxs-lookup"><span data-stu-id="1c5c4-112">**IAccClientDocMgr**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-iaccclientdocmgr)   | <span data-ttu-id="1c5c4-113">公開用戶端應用程式取出檔的方法。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-113">Exposes methods for client applications to retrieve documents.</span></span>                                      |
| [<span data-ttu-id="1c5c4-114">**IAccDictionary**</span><span class="sxs-lookup"><span data-stu-id="1c5c4-114">**IAccDictionary**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary)       | <span data-ttu-id="1c5c4-115">公開字串操作的方法。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-115">Exposes methods for string manipulation.</span></span>                                                            |
| [<span data-ttu-id="1c5c4-116">**ICoCreateLocally**</span><span class="sxs-lookup"><span data-stu-id="1c5c4-116">**ICoCreateLocally**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-icocreatelocally)   | <span data-ttu-id="1c5c4-117">公開方法，可讓用戶端應用程式在伺服器內容中建立 helper 物件。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-117">Exposes a method that enables a client application to create a helper object in the server context.</span></span> |
| [<span data-ttu-id="1c5c4-118">**ICoCreatedLocally**</span><span class="sxs-lookup"><span data-stu-id="1c5c4-118">**ICoCreatedLocally**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-icocreatedlocally) | <span data-ttu-id="1c5c4-119">公開方法，以傳回本機物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-119">Exposes a method to return information about a local object.</span></span>                                        |
| [<span data-ttu-id="1c5c4-120">**IVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="1c5c4-120">**IVersionInfo**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-iversioninfo)           | <span data-ttu-id="1c5c4-121">公開提供可存取元素之版本資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-121">Exposes methods that supply version information for accessible elements.</span></span>                            |

## <a name="related-topics"></a><span data-ttu-id="1c5c4-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c5c4-122">Related topics</span></span>

[<span data-ttu-id="1c5c4-123">Active Accessibility 消費者介面服務</span><span class="sxs-lookup"><span data-stu-id="1c5c4-123">Active Accessibility User Interface Services</span></span>](active-accessibility-user-interface-services-dev-guide.md)