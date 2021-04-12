---
title: 公開 IAccessible 介面未涵蓋的其他資訊
description: 根據其產品而定，除了 Microsoft Active Accessibility 支援之外，伺服器開發人員可能還需要公開資訊或功能。
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316027"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a><span data-ttu-id="848df-103">公開 IAccessible 介面未涵蓋的其他資訊</span><span class="sxs-lookup"><span data-stu-id="848df-103">Exposing Additional Information Not Covered by IAccessible Interface</span></span>

<span data-ttu-id="848df-104">根據其產品而定，除了 Microsoft Active Accessibility 支援之外，伺服器開發人員可能還需要公開資訊或功能。</span><span class="sxs-lookup"><span data-stu-id="848df-104">Depending on their products, server developers might need to expose information or functionality in addition to Microsoft Active Accessibility support.</span></span> <span data-ttu-id="848df-105">如果是這種情況，請與 (用戶端) 的輔助技術廠商合作，以確保他們新增功能的支援。</span><span class="sxs-lookup"><span data-stu-id="848df-105">If this is the case, work with assistive technology vendors (clients) to ensure that they add support for the features.</span></span>

<span data-ttu-id="848df-106">請勿嘗試擴充 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。</span><span class="sxs-lookup"><span data-stu-id="848df-106">Do not attempt to extend the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="848df-107">一旦發行介面之後，就無法變更它們。</span><span class="sxs-lookup"><span data-stu-id="848df-107">Interfaces cannot be changed once they are published.</span></span> <span data-ttu-id="848df-108">若要公開其他資訊，請使用自訂介面，並使用下列其中一種技術來公開它：</span><span class="sxs-lookup"><span data-stu-id="848df-108">To expose additional information, use a custom interface and expose it by using one of the following techniques:</span></span>

-   [<span data-ttu-id="848df-109">使用 OBJID \_ NATIVEOM 來公開視窗的原生物件模型介面</span><span class="sxs-lookup"><span data-stu-id="848df-109">Using OBJID\_NATIVEOM to expose a native object model interface for a window</span></span>](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [<span data-ttu-id="848df-110">使用 QueryService 公開 IAccessible 物件的原生物件模型介面</span><span class="sxs-lookup"><span data-stu-id="848df-110">Using QueryService to expose a native object model interface for an IAccessible object</span></span>](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

<span data-ttu-id="848df-111">請注意， [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的目標是要有伺服器和用戶端所使用的妥善定義介面。</span><span class="sxs-lookup"><span data-stu-id="848df-111">Note that the goal of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is to have a well-defined interface that is used by servers and clients.</span></span> <span data-ttu-id="848df-112">公開自訂介面之前，請務必透過 **IAccessible** 公開盡可能多的資訊。</span><span class="sxs-lookup"><span data-stu-id="848df-112">Before exposing custom interfaces, be sure to expose as much information as possible through **IAccessible**.</span></span>

<span data-ttu-id="848df-113">您無法使用 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來公開自訂介面。</span><span class="sxs-lookup"><span data-stu-id="848df-113">You cannot use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to expose custom interfaces.</span></span> <span data-ttu-id="848df-114">使用 **IServiceProvider：： QueryService** ，如下列程式所述。</span><span class="sxs-lookup"><span data-stu-id="848df-114">Use **IServiceProvider::QueryService** as outlined in the following procedures.</span></span>

 

 