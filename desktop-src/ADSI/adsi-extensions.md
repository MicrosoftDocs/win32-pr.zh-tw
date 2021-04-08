---
title: ADSI 擴充功能
description: ADSI 擴充功能是特殊的 COM 物件，可讓開發人員擴充 ADSI 物件。
ms.assetid: 3e40e702-089a-4d2a-806c-cd5b29d11bfd
ms.tgt_platform: multiple
keywords:
- ADSI 擴充功能
- ADSI ADSI，使用擴充功能
- 擴充功能 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3852e64ad282c11ecd17c6b13904738ee7f46a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020813"
---
# <a name="adsi-extensions"></a><span data-ttu-id="8c832-106">ADSI 擴充功能</span><span class="sxs-lookup"><span data-stu-id="8c832-106">ADSI Extensions</span></span>

<span data-ttu-id="8c832-107">ADSI 擴充功能是特殊的 COM 物件，可讓開發人員擴充 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="8c832-107">An ADSI extension is a special COM object that enable a developer to extend an ADSI object.</span></span> <span data-ttu-id="8c832-108">每個擴充功能都與目錄中的指定類別相關聯。</span><span class="sxs-lookup"><span data-stu-id="8c832-108">Each extension is associated with a specified class in the directory.</span></span> <span data-ttu-id="8c832-109">使用此延伸模組模型，開發人員可以加入方法來為物件提供更多動態意義。</span><span class="sxs-lookup"><span data-stu-id="8c832-109">With this extension model, developers can add methods to give more dynamic meaning to an object.</span></span> <span data-ttu-id="8c832-110">在傳統的目錄程式設計模型中，藉由取得和設定物件屬性來存取物件。</span><span class="sxs-lookup"><span data-stu-id="8c832-110">In a traditional directory programming model, an object is accessed by getting and setting the object attributes.</span></span> <span data-ttu-id="8c832-111">使用 ADSI 擴充功能，您可以將更多功能新增至目錄物件。</span><span class="sxs-lookup"><span data-stu-id="8c832-111">Using ADSI extensions, you can add more features to a directory object.</span></span>

<span data-ttu-id="8c832-112">本節將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="8c832-112">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="8c832-113">使用 ADSI 擴充功能的優點</span><span class="sxs-lookup"><span data-stu-id="8c832-113">Benefits of Using ADSI Extensions</span></span>](benefits-of-using-adsi-extensions.md)
-   [<span data-ttu-id="8c832-114">ADSI 擴充功能架構</span><span class="sxs-lookup"><span data-stu-id="8c832-114">ADSI Extension Architecture</span></span>](adsi-extension-architecture.md)
-   [<span data-ttu-id="8c832-115">ADSI 如何整合延伸模組</span><span class="sxs-lookup"><span data-stu-id="8c832-115">How ADSI Integrates Extensions</span></span>](adsi-and-extensions.md)
-   [<span data-ttu-id="8c832-116">用戶端會看到什麼？</span><span class="sxs-lookup"><span data-stu-id="8c832-116">What Does a Client See?</span></span>](what-does-a-client-see.md)
-   [<span data-ttu-id="8c832-117">從您的延伸模組取得 ADSI 介面</span><span class="sxs-lookup"><span data-stu-id="8c832-117">Getting ADSI Interfaces From Your Extension</span></span>](getting-adsi-interfaces-from-your-extension.md)
-   [<span data-ttu-id="8c832-118">ADSI 擴充功能類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8c832-118">ADSI Extension Type Libraries</span></span>](adsi-extension-type-libraries.md)
-   [<span data-ttu-id="8c832-119">早期繫結支援</span><span class="sxs-lookup"><span data-stu-id="8c832-119">Early Binding Support</span></span>](early-binding-support.md)
-   [<span data-ttu-id="8c832-120">晚期繫結支援</span><span class="sxs-lookup"><span data-stu-id="8c832-120">Late Binding Support</span></span>](late-binding-support.md)
-   [<span data-ttu-id="8c832-121">IADsExtension 介面</span><span class="sxs-lookup"><span data-stu-id="8c832-121">IADsExtension Interface</span></span>](iadsextension-interface.md)
-   [<span data-ttu-id="8c832-122">支援雙重或分派介面</span><span class="sxs-lookup"><span data-stu-id="8c832-122">Supporting Dual or Dispatch Interfaces</span></span>](supporting-dual-or-dispatch-interfaces.md)
-   [<span data-ttu-id="8c832-123">使用 ADSI 擴充功能重新使用 COM 匯總規則</span><span class="sxs-lookup"><span data-stu-id="8c832-123">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>](revisiting-com-aggregation-rules-with-adsi-extensions.md)
-   [<span data-ttu-id="8c832-124">支援相同介面的多個匯總元件的解析</span><span class="sxs-lookup"><span data-stu-id="8c832-124">Resolution of Multiple Aggregation Components Supporting the Same Interface</span></span>](resolution-of-multiple-aggregation-components-supporting-the-same-interface.md)
-   [<span data-ttu-id="8c832-125">函數/屬性名稱在延伸模組中的自動化衝突</span><span class="sxs-lookup"><span data-stu-id="8c832-125">Resolution of Function/Property Name Conflicts in Automation in Extensions</span></span>](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)

 

 




