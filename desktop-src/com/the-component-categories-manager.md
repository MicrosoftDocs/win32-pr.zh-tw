---
title: 元件類別管理員
description: 元件類別管理員
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462196"
---
# <a name="the-component-categories-manager"></a><span data-ttu-id="ea088-103">元件類別管理員</span><span class="sxs-lookup"><span data-stu-id="ea088-103">The Component Categories Manager</span></span>

<span data-ttu-id="ea088-104">為了協助處理元件類別以及保證登錄的一致性，系統會提供元件類別目錄管理員，也就是具有 CLSID StdComponentCategoriesMgr CLSID 的 COM 物件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ea088-104">To facilitate the handling of component categories and to guarantee consistency of the registry, the system provides the Component Categories Manager, a COM object with a CLSID of CLSID\_StdComponentCategoriesMgr.</span></span> <span data-ttu-id="ea088-105">這個 COM 物件提供下列介面：</span><span class="sxs-lookup"><span data-stu-id="ea088-105">This COM object provides the following interfaces:</span></span>

-   [<span data-ttu-id="ea088-106">**ICatInformation**</span><span class="sxs-lookup"><span data-stu-id="ea088-106">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [<span data-ttu-id="ea088-107">**ICatRegister**</span><span class="sxs-lookup"><span data-stu-id="ea088-107">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)

<span data-ttu-id="ea088-108">[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) 會提供方法，以取得特定類別所執行之類別的相關資訊，並提供在指定電腦上註冊之類別的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ea088-108">[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) provides methods for obtaining information about the categories implemented or required by a certain class and provides information about the categories registered on a given machine.</span></span>

<span data-ttu-id="ea088-109">[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) 提供在登錄中註冊和取消註冊元件類別目錄資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="ea088-109">[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) provides methods for registering and unregistering component category information in the registry.</span></span> <span data-ttu-id="ea088-110">這包括人類看得懂的類別名稱，以及指定元件或類別所執行或所需的類別。</span><span class="sxs-lookup"><span data-stu-id="ea088-110">This includes both the human-readable names of categories and the categories implemented or required by a given component or class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea088-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="ea088-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea088-112">將圖示與類別產生關聯</span><span class="sxs-lookup"><span data-stu-id="ea088-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="ea088-113">依元件功能分類</span><span class="sxs-lookup"><span data-stu-id="ea088-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="ea088-114">依容器功能分類</span><span class="sxs-lookup"><span data-stu-id="ea088-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="ea088-115">預設類別和關聯</span><span class="sxs-lookup"><span data-stu-id="ea088-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="ea088-116">定義元件類別</span><span class="sxs-lookup"><span data-stu-id="ea088-116">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> </dl>

 

 




