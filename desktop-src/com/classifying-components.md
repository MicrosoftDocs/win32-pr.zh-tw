---
title: 分類元件
description: 分類元件
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ea1547c219a44262fdeaf7edb02f65c7a3aac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840500"
---
# <a name="classifying-components"></a><span data-ttu-id="32d81-103">分類元件</span><span class="sxs-lookup"><span data-stu-id="32d81-103">Classifying Components</span></span>

<span data-ttu-id="32d81-104">當用戶端能夠流覽登錄中的 Clsid 清單並選取要使用的元件時，載入登錄中的每個元件，並針對其支援的介面進行查詢，會相當耗時。</span><span class="sxs-lookup"><span data-stu-id="32d81-104">While a client is able to browse through the list of CLSIDs in the registry and select a component to use, loading each component in the registry and querying it for its supported interfaces is very time-consuming.</span></span> <span data-ttu-id="32d81-105">若要在建立元件的實例之前，判斷元件是否支援所需的介面，已開發將元件分類為類別的方法。</span><span class="sxs-lookup"><span data-stu-id="32d81-105">To determine whether a component supports the interfaces required before creating an instance of the component, a method to classify components into categories was developed.</span></span>

<span data-ttu-id="32d81-106">元件類別是一組已指派 GUID 名為 CATID 的介面。</span><span class="sxs-lookup"><span data-stu-id="32d81-106">A component category is a set of interfaces that have been assigned a GUID named CATID.</span></span> <span data-ttu-id="32d81-107">在元件類別中執行所有介面的元件，會自行註冊為該元件類別目錄的成員。</span><span class="sxs-lookup"><span data-stu-id="32d81-107">Components that implement all of the interfaces in a component category register themselves as members of that component category.</span></span> <span data-ttu-id="32d81-108">然後可以從登錄中選取屬於特定元件類別目錄的元件。</span><span class="sxs-lookup"><span data-stu-id="32d81-108">Components that belong to a certain component category can then be selected from the registry.</span></span> <span data-ttu-id="32d81-109">藉由將本身註冊為元件類別目錄的成員，元件會保證它支援元件類別中的所有成員介面。</span><span class="sxs-lookup"><span data-stu-id="32d81-109">By registering itself as a member of a component category, the component is guaranteeing that it supports all of the member interfaces in the component category.</span></span>

<span data-ttu-id="32d81-110">元件可以是許多類別的成員。</span><span class="sxs-lookup"><span data-stu-id="32d81-110">A component can be a member of many categories.</span></span> <span data-ttu-id="32d81-111">它不限於元件類別中的支援介面。</span><span class="sxs-lookup"><span data-stu-id="32d81-111">It is not limited to supporting interfaces in a component category.</span></span> <span data-ttu-id="32d81-112">除了元件類別中的介面之外，它還可以支援任何介面。</span><span class="sxs-lookup"><span data-stu-id="32d81-112">It can support any interface, in addition to those in a component category.</span></span>

<span data-ttu-id="32d81-113">相較于標準註冊的元件，開發人員必須撰寫程式碼以手動方式註冊物件，但元件類別會將大部分的工作自動化。</span><span class="sxs-lookup"><span data-stu-id="32d81-113">In contrast to the standard registration of components, in which developers must write code that manually registers objects, component categories automates much of this work.</span></span> <span data-ttu-id="32d81-114">[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)介面的六個方法會定義元件類別，並註冊可執行或需要它們的物件。</span><span class="sxs-lookup"><span data-stu-id="32d81-114">The six methods of the [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) interface define component categories and register objects that implement or require them.</span></span> <span data-ttu-id="32d81-115">[元件類別管理員](the-component-categories-manager.md)物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="32d81-115">The [Component Categories Manager](the-component-categories-manager.md) object implements this interface.</span></span> <span data-ttu-id="32d81-116">如需使用元件類別的詳細資訊，請參閱 **ICatRegister** 和 [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) 。</span><span class="sxs-lookup"><span data-stu-id="32d81-116">See **ICatRegister** and [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) for additional information on using component categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32d81-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="32d81-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32d81-118">註冊 COM 應用程式</span><span class="sxs-lookup"><span data-stu-id="32d81-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




