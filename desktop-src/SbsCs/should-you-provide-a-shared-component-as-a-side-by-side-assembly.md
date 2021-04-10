---
description: 如果下列一或多個情況成立，共用元件的提供者應考慮將其元件當作並存元件提供。
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: 您是否應該提供共用元件作為並存元件？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733adf400ba9ce019d9f749fcd79a1a71380c9e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851767"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a><span data-ttu-id="fe4a0-103">您是否應該提供共用元件作為並存元件？</span><span class="sxs-lookup"><span data-stu-id="fe4a0-103">Should you provide a shared component as a side-by-side assembly?</span></span>

<span data-ttu-id="fe4a0-104">如果下列一或多個條件成立，共用元件的提供者應該考慮將其元件作為並存元件使用：</span><span class="sxs-lookup"><span data-stu-id="fe4a0-104">Providers of shared components should consider making their component available as a side-by-side assembly if one or more of the following are true:</span></span>

-   <span data-ttu-id="fe4a0-105">元件會公開許多應用程式所使用的豐富應用程式開發介面。</span><span class="sxs-lookup"><span data-stu-id="fe4a0-105">The component exposes a rich application programming interface that is used by many applications.</span></span> <span data-ttu-id="fe4a0-106">例如，MSHTML 之類的元件，可讓 C 和 c + + 應用程式存取動態 HTML (DHTML) 物件模型。</span><span class="sxs-lookup"><span data-stu-id="fe4a0-106">For example, a component such as MSHTML, which enables C and C++ applications to access the Dynamic HTML (DHTML) Object Model.</span></span>
-   <span data-ttu-id="fe4a0-107">元件已被多個應用程式共用。</span><span class="sxs-lookup"><span data-stu-id="fe4a0-107">The component is already being shared by multiple applications.</span></span> <span data-ttu-id="fe4a0-108">例如，COMCTL32.DLL 這類元件可讓應用程式存取通用控制項。</span><span class="sxs-lookup"><span data-stu-id="fe4a0-108">For example, a component such as COMCTL32, which provides applications access to the common controls.</span></span>
-   <span data-ttu-id="fe4a0-109">元件是一個新元件。</span><span class="sxs-lookup"><span data-stu-id="fe4a0-109">The component is a new component.</span></span>
-   <span data-ttu-id="fe4a0-110">此元件是使用者模式元件，而不是設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="fe4a0-110">The component is a user-mode component and not a device driver.</span></span>

<span data-ttu-id="fe4a0-111">並非每個元件都是並存元件的合適候選項。</span><span class="sxs-lookup"><span data-stu-id="fe4a0-111">Not every component is a suitable candidate for a side-by-side assembly.</span></span> <span data-ttu-id="fe4a0-112">如果下列任何一個條件成立，則元件不適合併存元件的候選元件：</span><span class="sxs-lookup"><span data-stu-id="fe4a0-112">A component is not a suitable candidate for a side-by-side assembly if any of the following are true:</span></span>

-   <span data-ttu-id="fe4a0-113">元件會處理應用程式之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="fe4a0-113">The component handles communication between applications.</span></span> <span data-ttu-id="fe4a0-114">例如，OLE32.LIB 的元件不會產生良好的並存元件，因為您不想要有兩個不同版本的元件，以協調在您系統上執行的應用程式之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="fe4a0-114">For example, parts of OLE32 would not make a good side-by-side assembly because you would not want to have two different versions of the parts that coordinate communication between applications run on your system.</span></span>
-   <span data-ttu-id="fe4a0-115">元件會管理系統的實體或虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="fe4a0-115">The component manages a physical or virtual device for the system.</span></span> <span data-ttu-id="fe4a0-116">例如，列印多工緩衝處理器的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="fe4a0-116">For example a device driver for a print spooler.</span></span>

<span data-ttu-id="fe4a0-117">在某些情況下，元件開發人員可能會重新設計現有的元件，使其適合以並存元件的形式發行。</span><span class="sxs-lookup"><span data-stu-id="fe4a0-117">In some cases it may be possible for the developer of the component to redesign an existing component in order to make it suitable for publication as a side-by-side assembly.</span></span> <span data-ttu-id="fe4a0-118">如需詳細資訊，請參閱 [建立並存元件的指導方針](guidelines-for-creating-side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="fe4a0-118">For more information see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

 

 



