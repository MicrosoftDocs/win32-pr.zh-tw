---
description: 系統裝置列舉值
ms.assetid: ea98be7f-580d-4986-bd6b-d254a2c075e8
title: 系統裝置列舉值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b80f7157843f11af307e6573abe3c76f30f23e5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908436"
---
# <a name="system-device-enumerator"></a><span data-ttu-id="52288-103">系統裝置列舉值</span><span class="sxs-lookup"><span data-stu-id="52288-103">System Device Enumerator</span></span>

<span data-ttu-id="52288-104">系統裝置列舉值會列舉安裝在系統上的篩選器和硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="52288-104">The System Device Enumerator enumerates filters and hardware devices installed on the system.</span></span> <span data-ttu-id="52288-105">應用程式可以使用此元件找出指定類別中的篩選器和裝置。</span><span class="sxs-lookup"><span data-stu-id="52288-105">Applications can use this component to locate filters and devices in a given category.</span></span> <span data-ttu-id="52288-106">藉由呼叫 **CoCreateInstance** 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="52288-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="52288-107">標籤</span><span class="sxs-lookup"><span data-stu-id="52288-107">Label</span></span> | <span data-ttu-id="52288-108">值</span><span class="sxs-lookup"><span data-stu-id="52288-108">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="52288-109">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="52288-109">Class Identifier</span></span> | <span data-ttu-id="52288-110">CLSID \_ SystemDeviceEnum</span><span class="sxs-lookup"><span data-stu-id="52288-110">CLSID\_SystemDeviceEnum</span></span>                  |
| <span data-ttu-id="52288-111">介面</span><span class="sxs-lookup"><span data-stu-id="52288-111">Interfaces</span></span>       | [<span data-ttu-id="52288-112">**ICreateDevEnum**</span><span class="sxs-lookup"><span data-stu-id="52288-112">**ICreateDevEnum**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) |



 

## <a name="related-topics"></a><span data-ttu-id="52288-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="52288-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52288-114">DirectShow 物件</span><span class="sxs-lookup"><span data-stu-id="52288-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="52288-115">列舉裝置和篩選器</span><span class="sxs-lookup"><span data-stu-id="52288-115">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="52288-116">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="52288-116">Filter Categories</span></span>](filter-categories.md)
</dt> </dl>

 

 



