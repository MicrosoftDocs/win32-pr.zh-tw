---
title: 架構介面
description: 架構介面
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- 架構介面 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f414fdea2418fb92a0a3c8c9e8bf88eb6d7f00b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931831"
---
# <a name="schema-interfaces"></a><span data-ttu-id="b7c2e-104">架構介面</span><span class="sxs-lookup"><span data-stu-id="b7c2e-104">Schema Interfaces</span></span>

<span data-ttu-id="b7c2e-105">架構容器包含一組架構定義，這些定義會附加至提供者的命名空間樹狀結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-105">The schema container contains a set of schema definitions that are attached to part of the namespace tree of the provider.</span></span> <span data-ttu-id="b7c2e-106">一般而言，命名空間的每個實例都有自己的架構。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-106">Typically, each instance of a namespace has its own schema.</span></span> <span data-ttu-id="b7c2e-107">例如，在下圖中，ADSI 範例提供者會在每個根節點「西雅圖」和「多倫多」中定義架構容器。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-107">For example, in the following figure, the ADSI example provider defines a schema container in each of the root nodes "Seattle" and "Toronto".</span></span>

![架構內含專案](images/schemacont.png)

<span data-ttu-id="b7c2e-109">若要建立提供者的 ADSI 執行，您需要提供架構管理物件，以反映提供者的基礎命名空間，並支援 ADSI 架構介面。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-109">To create an ADSI implementation for a provider, you need to supply schema management objects that reflect the underlying namespace of the provider and which support ADSI schema interfaces.</span></span> <span data-ttu-id="b7c2e-110">以下是包含在架構容器中的 ADSI 架構介面清單。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-110">The following is a list of the ADSI schema interfaces, which are contained in the schema container.</span></span>

-   <span data-ttu-id="b7c2e-111">[**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) 代表目錄服務類別。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-111">[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) represents directory service classes.</span></span>
-   <span data-ttu-id="b7c2e-112">[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) 代表具有單一或多個值的目錄服務屬性。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-112">[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) represents directory service properties that have single or multiple values.</span></span>
-   <span data-ttu-id="b7c2e-113">[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) 代表單一 VARIANT 型別。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-113">[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) represents the single VARIANT type.</span></span>

<span data-ttu-id="b7c2e-114">ADSI 所定義的介面可以支援提供者的特定屬性和語法。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-114">Interfaces defined by ADSI can support specific properties and syntaxes for your provider.</span></span> <span data-ttu-id="b7c2e-115">提供者可以選擇使用建立和存取屬性的方法來擴充 ADSI 定義，例如，您可以使用 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面的方法，例如 [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get)、 [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex)、 [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) 和 [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex)。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-115">Providers can choose to extend an ADSI definition by using the methods that create and access properties, for example, you can use the methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex).</span></span> <span data-ttu-id="b7c2e-116">提供者也可以透過其他介面支援其他屬性。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-116">Providers can also support additional properties through additional interfaces.</span></span> <span data-ttu-id="b7c2e-117">如需 ADSI 介面的完整清單，請參閱 [Adsi 介面](adsi-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-117">For a complete list of ADSI interfaces, see [ADSI Interfaces](adsi-interfaces.md).</span></span>

<span data-ttu-id="b7c2e-118">具有複雜命名空間的 ADSI 提供者元件可能會允許多個架構存在於命名空間實例中，每個都位於樹狀結構的不同部分。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-118">An ADSI provider component with a complex namespace might allow multiple schemas to exist in a namespace instance, each at a different part of the tree.</span></span> <span data-ttu-id="b7c2e-119">不過，物件的 [**IADs：： Schema**](iads-property-methods.md) 屬性一律會命名它自己的架構定義。</span><span class="sxs-lookup"><span data-stu-id="b7c2e-119">The [**IADs::Schema**](iads-property-methods.md) property of an object, however, always names its own schema definition.</span></span>

 

 




