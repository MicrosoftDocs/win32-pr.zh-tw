---
title: 動態注釋 API
description: 動態批註 API 是 Microsoft Active Accessibility 的延伸模組，可讓開發人員自訂現有的 IAccessible 支援，而不需要使用容易出錯的子類別化或包裝技術。
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7f73c1da79784fdd86652128b572fd81904023c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932588"
---
# <a name="dynamic-annotation-api"></a><span data-ttu-id="3cccc-103">動態注釋 API</span><span class="sxs-lookup"><span data-stu-id="3cccc-103">Dynamic Annotation API</span></span>

<span data-ttu-id="3cccc-104">動態批註 API 是 Microsoft Active Accessibility 的延伸模組，可讓開發人員自訂現有的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 支援，而不需要使用容易出錯的子類別化或包裝技術。</span><span class="sxs-lookup"><span data-stu-id="3cccc-104">The Dynamic Annotation API is an extension to Microsoft Active Accessibility that allows developers to customize existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support without having to use error-prone subclassing or wrapping techniques.</span></span> <span data-ttu-id="3cccc-105">這種機制也可讓開發人員將提示或其他有用的資訊傳遞給 Oleacc.dll proxy。</span><span class="sxs-lookup"><span data-stu-id="3cccc-105">This mechanism also allows developers to pass hints or other useful information to the Oleacc.dll proxies.</span></span>

<span data-ttu-id="3cccc-106">動態注釋通常用來更正或修改現有 Oleacc.dll proxy 所公開的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件不正確的實例。</span><span class="sxs-lookup"><span data-stu-id="3cccc-106">Dynamic Annotation is typically used to correct or amend an inaccurate instance of an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object exposed by an existing Oleacc.dll proxy.</span></span> <span data-ttu-id="3cccc-107">例如，您可以使用它來覆寫預設 proxy 所提供的 [**名稱**](name-property.md)和 [**角色**](role-property.md)屬性 [**，並提供**](help-property.md)描述和 [**說明**](description-property.md)屬性 (預設 proxy) 可能無法提供。</span><span class="sxs-lookup"><span data-stu-id="3cccc-107">For example, you can use it to override the [**Name**](name-property.md) and [**Role**](role-property.md) properties provided by the default proxy, and to supply [**Description**](description-property.md) and [**Help**](help-property.md) properties (which may not be provided by the default proxy).</span></span>

<span data-ttu-id="3cccc-108">在 Windows 7 中，開發人員可以使用動態批註 API 來標注 Microsoft 消費者介面自動化屬性，以及 Oleacc.dll 為標準 Windows 控制項建立的 proxy 物件 Microsoft Active Accessibility 屬性。</span><span class="sxs-lookup"><span data-stu-id="3cccc-108">With Windows 7, developers can use the Dynamic Annotation API to annotate Microsoft UI Automation properties as well as Microsoft Active Accessibility properties of the proxy objects that Oleacc.dll creates for standard Windows controls.</span></span> <span data-ttu-id="3cccc-109">Oleacc.dll 的 proxy 物件可同時為 Microsoft Active Accessibility 和消費者介面自動化用戶端提供服務。</span><span class="sxs-lookup"><span data-stu-id="3cccc-109">The Oleacc.dll proxy objects serve both Microsoft Active Accessibility and UI Automation clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3cccc-110">本節內容</span><span class="sxs-lookup"><span data-stu-id="3cccc-110">In this section</span></span>

-   [<span data-ttu-id="3cccc-111">背景資訊</span><span class="sxs-lookup"><span data-stu-id="3cccc-111">Background Information</span></span>](background-information.md)
-   [<span data-ttu-id="3cccc-112">動態注釋的替代方案</span><span class="sxs-lookup"><span data-stu-id="3cccc-112">Alternatives to Dynamic Annotation</span></span>](alternatives-to-dynamic-annotation.md)
-   [<span data-ttu-id="3cccc-113">動態注釋的類型</span><span class="sxs-lookup"><span data-stu-id="3cccc-113">Types of Dynamic Annotation</span></span>](types-of-dynamic-annotation.md)
-   [<span data-ttu-id="3cccc-114">直接注釋</span><span class="sxs-lookup"><span data-stu-id="3cccc-114">Direct Annotation</span></span>](direct-annotation.md)
-   [<span data-ttu-id="3cccc-115">值對應注釋</span><span class="sxs-lookup"><span data-stu-id="3cccc-115">Value Map Annotation</span></span>](value-map-annotation.md)
-   [<span data-ttu-id="3cccc-116">伺服器注釋</span><span class="sxs-lookup"><span data-stu-id="3cccc-116">Server Annotation</span></span>](server-annotation.md)
-   [<span data-ttu-id="3cccc-117">問題與限制</span><span class="sxs-lookup"><span data-stu-id="3cccc-117">Issues and Limitations</span></span>](issues-and-limitations.md)

 

 




