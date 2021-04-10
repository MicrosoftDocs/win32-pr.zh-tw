---
title: 背景資訊
description: Microsoft Active Accessibility 元件 oleacc.dll 會建立代表標準 Windows 控制項來執行 IAccessible 的 proxy 物件。
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a9b044f8035a474f02b8457dc99ec39aca73c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092237"
---
# <a name="background-information"></a><span data-ttu-id="fa508-103">背景資訊</span><span class="sxs-lookup"><span data-stu-id="fa508-103">Background Information</span></span>

<span data-ttu-id="fa508-104">Microsoft Active Accessibility 元件 oleacc.dll 會建立代表標準 Windows 控制項來執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 的 proxy 物件。</span><span class="sxs-lookup"><span data-stu-id="fa508-104">The Microsoft Active Accessibility component, oleacc.dll, creates proxy objects that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) on behalf of standard Windows controls.</span></span> <span data-ttu-id="fa508-105">因為這些 proxy 使用標準的 Windows 訊息和控制特定的 Api 來收集每個控制項的相關資訊，所以沒有直接機制可以自訂這些 proxy 透過 **IAccessible** 公開的資訊。</span><span class="sxs-lookup"><span data-stu-id="fa508-105">Because these proxies use standard Windows messages and control-specific APIs to collect information about each control, there has been no direct mechanism for customizing the information these proxies expose through **IAccessible**.</span></span>

<span data-ttu-id="fa508-106">目前，您可以使用子類別化和包裝技術來自訂現有的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 執行。</span><span class="sxs-lookup"><span data-stu-id="fa508-106">Currently, you can customize an existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation using subclassing and wrapping techniques.</span></span> <span data-ttu-id="fa508-107">不過，這些技術既繁瑣又容易出錯。</span><span class="sxs-lookup"><span data-stu-id="fa508-107">However, these techniques are tedious and error-prone.</span></span> <span data-ttu-id="fa508-108">事實上，撰寫用來覆寫一或兩個屬性的大部分程式碼，都很在意如何執行子類別化和包裝;只有一個小部分會執行覆寫資訊的實際工作。</span><span class="sxs-lookup"><span data-stu-id="fa508-108">In fact, the majority of the code written to override one or two properties is concerned with implementing subclassing and wrapping; only a small fraction carries out the real task of overriding information.</span></span> <span data-ttu-id="fa508-109">動態注釋藉由提供類似的功能，而不需要撰寫子類別化或包裝程式碼，來改善這種情況。</span><span class="sxs-lookup"><span data-stu-id="fa508-109">Dynamic Annotation improves the situation by providing similar capabilities without requiring you to write subclassing or wrapping code.</span></span> <span data-ttu-id="fa508-110">相反地，您可以將焦點放在提供提供正確資訊的程式碼。</span><span class="sxs-lookup"><span data-stu-id="fa508-110">Instead, you can focus on providing code that supplies the correct information.</span></span> <span data-ttu-id="fa508-111">動態批註可讓開發人員將提示和其他有用的資訊傳遞給 OLEACC，以自訂其公開的資訊。</span><span class="sxs-lookup"><span data-stu-id="fa508-111">Dynamic Annotation allows developers to pass hints and other useful information to OLEACC to customize the information it exposes.</span></span> <span data-ttu-id="fa508-112">這項功能會降低支援 Microsoft Active Accessibility 的成本，並可讓開發人員大幅改善其使用者介面的可存取性。</span><span class="sxs-lookup"><span data-stu-id="fa508-112">This capability alone will reduce the cost of supporting Microsoft Active Accessibility and allow developers to greatly improve the accessibility of their user interfaces.</span></span>

 

 




