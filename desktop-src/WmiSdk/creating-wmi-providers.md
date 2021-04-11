---
description: 開發人員可以藉由開發 WMI 提供者來擴充 WMI 基礎結構。
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: 建立 WMI 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980d3cd10b7108397a577d54ef93e502fb28d1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027561"
---
# <a name="creating-wmi-providers"></a><span data-ttu-id="b3236-103">建立 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="b3236-103">Creating WMI Providers</span></span>

<span data-ttu-id="b3236-104">開發人員可以藉由開發 WMI 提供者來擴充 WMI 基礎結構。</span><span class="sxs-lookup"><span data-stu-id="b3236-104">Developers can extend the WMI infrastructure by developing WMI providers.</span></span> <span data-ttu-id="b3236-105">WMI 提供者是 COM 物件，可執行一組指定的介面，直到最近，一直都是在 c + + 中執行。</span><span class="sxs-lookup"><span data-stu-id="b3236-105">WMI providers are COM objects that implement a specified set of interfaces and, until recently, were always implemented in C++.</span></span> <span data-ttu-id="b3236-106">您現在可以使用 c # 之類的 managed 語言來執行 WMI 提供者。</span><span class="sxs-lookup"><span data-stu-id="b3236-106">You can now use managed languages like C# to implement WMI providers.</span></span> <span data-ttu-id="b3236-107">3.5 版的 .NET framework 引進了 WMI 提供者延伸架構，讓這項功能得以實現。</span><span class="sxs-lookup"><span data-stu-id="b3236-107">Version 3.5 of the .NET framework introduced the WMI Provider Extensions framework that makes this possible.</span></span> <span data-ttu-id="b3236-108">若要深入瞭解如何使用該架構來建立 WMI 提供者，請參閱文章， [使用 WMI.NET 提供者延伸模組2.0 撰寫結合的 wmi 提供者](/previous-versions/dotnet/articles/cc268228(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="b3236-108">To learn more about creating WMI providers by using that framework, read the article, [Writing coupled WMI providers using WMI.NET Provider Extension 2.0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="b3236-109">您也可以使用 Windows 管理基礎結構 (MI) （WMI 的下一代版本）來建立提供者。</span><span class="sxs-lookup"><span data-stu-id="b3236-109">You can also create a provider using Windows Management Infrastructure (MI), the next-generation version of WMI.</span></span> <span data-ttu-id="b3236-110">如需詳細資訊，請參閱 [如何執行 MI 提供者](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider)。</span><span class="sxs-lookup"><span data-stu-id="b3236-110">For more information, see [How to Implement an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).</span></span>

 

<span data-ttu-id="b3236-111">下表說明本節中的內容。</span><span class="sxs-lookup"><span data-stu-id="b3236-111">The following table describes the contents in this section.</span></span>



| <span data-ttu-id="b3236-112">主題</span><span class="sxs-lookup"><span data-stu-id="b3236-112">Topic</span></span>                                                      | <span data-ttu-id="b3236-113">描述</span><span class="sxs-lookup"><span data-stu-id="b3236-113">Description</span></span>                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="b3236-114">將資料提供給 WMI</span><span class="sxs-lookup"><span data-stu-id="b3236-114">Providing Data to WMI</span></span>](providing-data-to-wmi.md)         | <span data-ttu-id="b3236-115">概要說明建立 WMI 提供者所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="b3236-115">Provides an overview of the steps involved in creating a WMI provider.</span></span>         |
| [<span data-ttu-id="b3236-116">開發 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="b3236-116">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md) | <span data-ttu-id="b3236-117">描述當您建立各種類型的 WMI 提供者時，必須執行的工作。</span><span class="sxs-lookup"><span data-stu-id="b3236-117">Describes tasks you must perform when creating various types of WMI providers.</span></span> |



 

 

 
