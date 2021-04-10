---
title: 使用 ADSI 擴充功能重新使用 COM 匯總規則
description: 以下是 COM 匯總和 ADSI 擴充規則的簡短評論。
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- 延伸 ADSI、COM 匯總規則
- COM 匯總 ADSI
- 利用 ADSI 擴充功能來重新使用 COM 匯總規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683097"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a><span data-ttu-id="d5ac1-106">使用 ADSI 擴充功能重新使用 COM 匯總規則</span><span class="sxs-lookup"><span data-stu-id="d5ac1-106">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>

<span data-ttu-id="d5ac1-107">以下是 COM 匯總和 ADSI 擴充規則的簡短評論。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-107">The following is a brief review of COM aggregation and ADSI extension rules.</span></span>

-   <span data-ttu-id="d5ac1-108">**CreateInstance** 方法會傳回 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面的指標，如下所示，不會將任何函式呼叫委派給匯總工具。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-108">The **CreateInstance** method returns a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, as follows, that does not delegate any function calls to the aggregator.</span></span>

    <span data-ttu-id="d5ac1-109">[**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法會傳回它所支援之介面的指標，以及它不支援的介面錯誤。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-109">The [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method returns pointers to the interfaces that it supports, and errors for interfaces it does not support.</span></span>

    <span data-ttu-id="d5ac1-110">[**IUnknown：： AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)方法會遞增匯總延伸模組物件本身的參考計數。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-110">The [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method increments the reference count on the aggregated extension object itself.</span></span>

    <span data-ttu-id="d5ac1-111">[**IUnkown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法會遞減匯總延伸模組物件本身的參考計數，並在參考計數為0時終結本身。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-111">The [**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method decrements the reference count on the aggregated extension object itself and destroys itself when the reference count is 0.</span></span>

-   <span data-ttu-id="d5ac1-112">在 [](/windows/win32/api/unknwn/nn-unknwn-iunknown) \_ **CreateInstance** 方法的執行期間，擴充物件應儲存匯總工具的 IUnknown 指標，例如 m pOuterUnknown。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-112">The extension object should store the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer of the aggregator, such as m\_pOuterUnknown, during the implementation of the **CreateInstance** method.</span></span>
-   <span data-ttu-id="d5ac1-113">擴充功能物件支援的所有介面（包括 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)）都應該繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)，這會將所有函式呼叫委派回匯總工具。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-113">All interfaces that the extension object supports, including [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), should inherit from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), which delegates all function calls back to the aggregator.</span></span>
    -   <span data-ttu-id="d5ac1-114">[**IUnknown：： queryinterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 呼叫 "m \_ POuterUnknown->QueryInterface"</span><span class="sxs-lookup"><span data-stu-id="d5ac1-114">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) calls "m\_pOuterUnknown->QueryInterface"</span></span>
    -   <span data-ttu-id="d5ac1-115">[**IUnknown：： AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 會呼叫 "m \_ POuterUnknown->AddRef"</span><span class="sxs-lookup"><span data-stu-id="d5ac1-115">[**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) calls "m\_pOuterUnknown->AddRef"</span></span>
    -   <span data-ttu-id="d5ac1-116">[**IUnkown：： release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 呼叫 "m \_ POuterUnknown->版本"</span><span class="sxs-lookup"><span data-stu-id="d5ac1-116">[**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls "m\_pOuterUnknown->Release"</span></span>

<span data-ttu-id="d5ac1-117">延伸模組寫入器可以選擇任何想要的內部執行，前提是它們遵循標準 COM 匯總規則。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-117">Extension writers can choose any internal implementation they prefer as long as they obey standard COM aggregation rules.</span></span> <span data-ttu-id="d5ac1-118">請注意，擴充物件不需要做為獨立物件。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-118">Be aware that an extension object does not have to work as a standalone object.</span></span> <span data-ttu-id="d5ac1-119">延伸模組是設計來做為匯總。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-119">Extensions are designed to work as aggregates.</span></span> <span data-ttu-id="d5ac1-120">不過，您可以撰寫延伸模組，以做為獨立物件和匯總。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-120">However, an extension can be written to work as both a standalone object and as an aggregate.</span></span>

<span data-ttu-id="d5ac1-121">除了標準的 COM 匯總支援，擴充物件也可支援 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) 以取得更先進的功能。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-121">In addition to standard COM aggregation support, an extension object may support [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) for more advanced features.</span></span> <span data-ttu-id="d5ac1-122">如果支援晚期繫結，則延伸模組應：</span><span class="sxs-lookup"><span data-stu-id="d5ac1-122">If late binding is supported, the extension should:</span></span>

-   <span data-ttu-id="d5ac1-123">將 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 的函式委派回匯總工具。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-123">Delegate functions for [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) back to the aggregator.</span></span>
-   <span data-ttu-id="d5ac1-124">在 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)中執行 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-124">Implement the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface in [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>

 

 