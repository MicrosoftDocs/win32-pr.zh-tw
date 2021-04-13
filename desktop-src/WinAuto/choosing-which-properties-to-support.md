---
title: 選擇要支援的屬性
description: IAccessible 屬性可讓伺服器開發人員描述各種不同的使用者介面元素。
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c88a808889403f88d414f7ad950b3e431c00e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301339"
---
# <a name="choosing-which-properties-to-support"></a><span data-ttu-id="75bbf-103">選擇要支援的屬性</span><span class="sxs-lookup"><span data-stu-id="75bbf-103">Choosing Which Properties to Support</span></span>

<span data-ttu-id="75bbf-104">[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)屬性可讓伺服器開發人員描述各種不同的使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="75bbf-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties provide a way for server developers to describe a wide variety of user interface elements.</span></span> <span data-ttu-id="75bbf-105">但並非所有屬性都適用于每種使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="75bbf-105">But not all of the properties are applicable for every kind of user interface element.</span></span> <span data-ttu-id="75bbf-106">此外，有些屬性會提供實用但不重要的描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="75bbf-106">Additionally, some properties provide descriptive information that is useful but not essential.</span></span>

<span data-ttu-id="75bbf-107">伺服器必須針對每個物件支援下列屬性和方法：</span><span class="sxs-lookup"><span data-stu-id="75bbf-107">Servers must support the following properties and methods for every object:</span></span>

-   [<span data-ttu-id="75bbf-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="75bbf-108">**Name**</span></span>](name-property.md)
-   [<span data-ttu-id="75bbf-109">**角色**</span><span class="sxs-lookup"><span data-stu-id="75bbf-109">**Role**</span></span>](role-property.md)
-   [<span data-ttu-id="75bbf-110">**狀態**</span><span class="sxs-lookup"><span data-stu-id="75bbf-110">**State**</span></span>](state-property.md)
-   <span data-ttu-id="75bbf-111">[**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)和 [ **IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span><span class="sxs-lookup"><span data-stu-id="75bbf-111">[**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span></span>
-   <span data-ttu-id="75bbf-112">[**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)和 [ **IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span><span class="sxs-lookup"><span data-stu-id="75bbf-112">[**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) and [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span></span>

<span data-ttu-id="75bbf-113">如果下列屬性和方法適用于物件，則必須加以支援：</span><span class="sxs-lookup"><span data-stu-id="75bbf-113">The following properties and method must be supported if they are applicable to the object:</span></span>

-   [<span data-ttu-id="75bbf-114">**KeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="75bbf-114">**KeyboardShortcut**</span></span>](keyboardshortcut-property.md)
-   [<span data-ttu-id="75bbf-115">**值**</span><span class="sxs-lookup"><span data-stu-id="75bbf-115">**Value**</span></span>](value-property.md)

<span data-ttu-id="75bbf-116">如果物件有子系，則必須支援下列屬性和方法：</span><span class="sxs-lookup"><span data-stu-id="75bbf-116">The following properties and method must be supported if the object has children:</span></span>

-   <span data-ttu-id="75bbf-117">[**子**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)系和 [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span><span class="sxs-lookup"><span data-stu-id="75bbf-117">[**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) and [**ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span></span>
-   <span data-ttu-id="75bbf-118">[**焦點、選取專案**](selection-and-focus-properties-and-methods.md)和 [ **IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span><span class="sxs-lookup"><span data-stu-id="75bbf-118">[**Focus, Selection**](selection-and-focus-properties-and-methods.md), and [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span></span>

<span data-ttu-id="75bbf-119">下列屬性是選擇性的，但提供物件的實用描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="75bbf-119">The following properties are optional, but provide useful descriptive information about the object.</span></span> <span data-ttu-id="75bbf-120">會執行 [**Description**](description-property.md) 屬性來描述點陣圖和其他影像。</span><span class="sxs-lookup"><span data-stu-id="75bbf-120">The [**Description**](description-property.md) property is implemented to describe bitmaps and other images.</span></span>

-   [<span data-ttu-id="75bbf-121">**描述**</span><span class="sxs-lookup"><span data-stu-id="75bbf-121">**Description**</span></span>](description-property.md)
-   <span data-ttu-id="75bbf-122">[**DefaultAction**](defaultaction-property.md)和 [ **IAccessible：： accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span><span class="sxs-lookup"><span data-stu-id="75bbf-122">[**DefaultAction**](defaultaction-property.md) and [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span></span>
-   [<span data-ttu-id="75bbf-123">**Help**</span><span class="sxs-lookup"><span data-stu-id="75bbf-123">**Help**</span></span>](help-property.md)
-   [<span data-ttu-id="75bbf-124">**HelpTopic**</span><span class="sxs-lookup"><span data-stu-id="75bbf-124">**HelpTopic**</span></span>](helptopic-property.md)

 

 




