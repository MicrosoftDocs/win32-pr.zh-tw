---
title: IAccessible 支援的類型
description: IAccessible 支援的類型
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb2cb3d25e4cf95cc1ad790c77ffe66e02efda2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673324"
---
# <a name="types-of-iaccessible-support"></a><span data-ttu-id="b624e-103">IAccessible 支援的類型</span><span class="sxs-lookup"><span data-stu-id="b624e-103">Types of IAccessible Support</span></span>

<span data-ttu-id="b624e-104">Microsoft Active Accessibility 伺服器有兩種類型的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 支援：原生和 proxy。</span><span class="sxs-lookup"><span data-stu-id="b624e-104">Microsoft Active Accessibility servers have two types of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support: native and proxied.</span></span> <span data-ttu-id="b624e-105">應用程式中使用的 UI 元素決定適當的支援類型。</span><span class="sxs-lookup"><span data-stu-id="b624e-105">The UI elements used in an application determine which type of support is appropriate.</span></span> <span data-ttu-id="b624e-106">現今撰寫的許多伺服器都能充分利用 **IAccessible** proxy，並且只針對非由 Oleacc.dll 進行 proxy 處理的控制項執行 **IAccessible** ，例如使用自訂視窗類別名稱的無視窗控制項或控制項。</span><span class="sxs-lookup"><span data-stu-id="b624e-106">Many servers being written today take full advantage of **IAccessible** proxies and only implement **IAccessible** for those controls that are not proxied by Oleacc.dll, such as windowless controls or controls with a custom window class name.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b624e-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="b624e-107">In this section</span></span>

-   [<span data-ttu-id="b624e-108">原生 Active Accessibility 實作為</span><span class="sxs-lookup"><span data-stu-id="b624e-108">Native Active Accessibility Implementation</span></span>](native-active-accessibility-implementation.md)
-   [<span data-ttu-id="b624e-109">IAccessible proxy</span><span class="sxs-lookup"><span data-stu-id="b624e-109">IAccessible Proxies</span></span>](iaccessible-proxies.md)

 

 




