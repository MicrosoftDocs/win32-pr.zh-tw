---
title: 動態注釋的類型
description: Microsoft Active Accessibility 直接批註、值對應注釋和伺服器批註支援三種類型的動態注釋。 每種類型都提供特定的優點，因此請務必瞭解差異。
ms.assetid: 113fea65-982e-4291-9d60-bbb57282f3f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0453d3b5d05e2713d1a57fb0f475d4ec2a481b02
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840040"
---
# <a name="types-of-dynamic-annotation"></a><span data-ttu-id="8bd42-104">動態注釋的類型</span><span class="sxs-lookup"><span data-stu-id="8bd42-104">Types of Dynamic Annotation</span></span>

<span data-ttu-id="8bd42-105">Microsoft Active Accessibility 中支援三種動態注釋類型： *直接批註*、 *值對應注釋* 和 *伺服器注釋*。</span><span class="sxs-lookup"><span data-stu-id="8bd42-105">There are three types of Dynamic Annotation supported in Microsoft Active Accessibility: *direct annotation*, *value-mapped annotation*, and *server annotation*.</span></span> <span data-ttu-id="8bd42-106">每種類型都提供特定的優點，因此請務必瞭解差異。</span><span class="sxs-lookup"><span data-stu-id="8bd42-106">Each type offers specific advantages, so it is important to understand the differences.</span></span>

## <a name="direct-annotation"></a><span data-ttu-id="8bd42-107">直接注釋</span><span class="sxs-lookup"><span data-stu-id="8bd42-107">Direct Annotation</span></span>

<span data-ttu-id="8bd42-108">直接注釋是動態注釋最簡單的形式。</span><span class="sxs-lookup"><span data-stu-id="8bd42-108">Direct annotation is the simplest form of Dynamic Annotation.</span></span> <span data-ttu-id="8bd42-109">它最適用于批註屬性不相依于控制項狀態的可存取專案，而且不需要由值對應注釋和伺服器批註提供的額外支援。</span><span class="sxs-lookup"><span data-stu-id="8bd42-109">It is most applicable for accessible elements whose annotated property is not dependent upon the control's state and does not require the additional support provided by value-mapped annotation and server annotation.</span></span> <span data-ttu-id="8bd42-110">直接批註是用來覆寫可存取專案的一或多個 Microsoft Active Accessibility 屬性的值，以及覆寫或加入 Microsoft 消費者介面自動化屬性至控制項。</span><span class="sxs-lookup"><span data-stu-id="8bd42-110">Direct annotation is used to override the value of one or more Microsoft Active Accessibility properties of an accessible element, and to override or add a Microsoft UI Automation property to the control.</span></span> <span data-ttu-id="8bd42-111">Microsoft Active Accessibility 屬性中所做的所有批註都會反映在消費者介面自動化轉譯和 Microsoft Active Accessibility 對消費者介面自動化 proxy 中。</span><span class="sxs-lookup"><span data-stu-id="8bd42-111">All annotations made in a Microsoft Active Accessibility property are reflected in the UI Automation translation as well as in the Microsoft Active Accessibility-to-UI Automation proxy.</span></span> <span data-ttu-id="8bd42-112">如需詳細資訊，請參閱 [直接批註](direct-annotation.md)。</span><span class="sxs-lookup"><span data-stu-id="8bd42-112">For more information, see [Direct Annotation](direct-annotation.md).</span></span>

## <a name="value-map-annotation"></a><span data-ttu-id="8bd42-113">值對應注釋</span><span class="sxs-lookup"><span data-stu-id="8bd42-113">Value Map Annotation</span></span>

<span data-ttu-id="8bd42-114">除了直接批註 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性以外，通常還需要將控制項特定的值轉換成可由使用者理解的字串。</span><span class="sxs-lookup"><span data-stu-id="8bd42-114">In addition to directly annotating [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties, there is often a need to convert a control-specific value into a string that can be understood by an end user.</span></span> <span data-ttu-id="8bd42-115">例如，在 [設定] 索引標籤的 [**設定**] 索引標籤下的 [螢幕解析度] 滑杆控制項， (**主控台**) 的 **顯示內容**。</span><span class="sxs-lookup"><span data-stu-id="8bd42-115">An example is the screen resolution slider control under the **Settings** tab on the **Display Properties** window (from **Control Panel**).</span></span> <span data-ttu-id="8bd42-116">雖然每個滑杆位置都對應至不同的解析度 (例如，640 x 480、1024 x 768) 、控制項並不知道此關聯性，也無法將這項資訊傳遞給 Microsoft Active Accessibility。</span><span class="sxs-lookup"><span data-stu-id="8bd42-116">While each slider position corresponds to a different resolution (for example, 640 x 480, 1024 x 768), the control has no knowledge of this relationship and cannot convey this information to Microsoft Active Accessibility.</span></span>

<span data-ttu-id="8bd42-117">值對應批註可讓這項工作更容易。</span><span class="sxs-lookup"><span data-stu-id="8bd42-117">Value-mapped annotation makes this task easier.</span></span> <span data-ttu-id="8bd42-118">您可以使用這種形式的注釋來指定滑杆值的字串，並指定清單和樹狀檢視中圖示的角色、狀態和描述。</span><span class="sxs-lookup"><span data-stu-id="8bd42-118">Using this form of annotation, you can specify strings for slider values and specify roles, states, and descriptions for icons in list and tree views.</span></span> <span data-ttu-id="8bd42-119">如需詳細資訊，請參閱 [值對應注釋](value-map-annotation.md)。</span><span class="sxs-lookup"><span data-stu-id="8bd42-119">For more information, see [Value Map Annotation](value-map-annotation.md).</span></span>

## <a name="server-annotation"></a><span data-ttu-id="8bd42-120">伺服器注釋</span><span class="sxs-lookup"><span data-stu-id="8bd42-120">Server Annotation</span></span>

<span data-ttu-id="8bd42-121">伺服器批註可讓開發人員註冊回呼物件，以服務用戶端對專案標注屬性的要求。</span><span class="sxs-lookup"><span data-stu-id="8bd42-121">Server annotation allows developers to register a callback object to service client requests for an element's annotated property.</span></span> <span data-ttu-id="8bd42-122">此回呼物件必須執行 [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) 介面，並向 Microsoft Active Accessibility 注釋服務註冊。</span><span class="sxs-lookup"><span data-stu-id="8bd42-122">This callback object must implement the [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) interface and be registered with Microsoft Active Accessibility annotation services.</span></span> <span data-ttu-id="8bd42-123">註冊之後，系統會要求您針對該可存取專案的屬性值服務所有用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="8bd42-123">Once registered, it will be asked to service all client requests for that accessible element's property value.</span></span>

<span data-ttu-id="8bd42-124">伺服器批註的一個特別有用的功能是，可以註冊一次伺服器來處理容器及其所有子系的要求。</span><span class="sxs-lookup"><span data-stu-id="8bd42-124">One particularly useful feature of server annotation is that a server can be registered once to handle requests for a container and all of its children.</span></span> <span data-ttu-id="8bd42-125">比方說，單一伺服器可以設定一次，以處理所有專案的要求是一個清單方塊。</span><span class="sxs-lookup"><span data-stu-id="8bd42-125">So, for example, a single server can be set up once to handle requests for all the items is a list box.</span></span> <span data-ttu-id="8bd42-126">如需詳細資訊，請參閱 [伺服器注釋](server-annotation.md)。</span><span class="sxs-lookup"><span data-stu-id="8bd42-126">For more information, see [Server Annotation](server-annotation.md).</span></span>

 

 




