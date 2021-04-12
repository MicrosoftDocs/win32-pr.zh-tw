---
description: 屬性集
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: " (DirectShow) 的屬性集"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdc65efbc99eeed3a5f94ab33ce5ec982975852
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385675"
---
# <a name="property-sets-directshow"></a><span data-ttu-id="892aa-103"> (DirectShow) 的屬性集</span><span class="sxs-lookup"><span data-stu-id="892aa-103">Property Sets (DirectShow)</span></span>

<span data-ttu-id="892aa-104">Microsoft DirectShow 使用屬性集來支援硬體及其相關驅動程式和篩選器所提供的擴充服務。</span><span class="sxs-lookup"><span data-stu-id="892aa-104">Microsoft DirectShow uses property sets to support extended services offered by hardware and its associated drivers and filters.</span></span> <span data-ttu-id="892aa-105">硬體和篩選廠商可以將新功能定義為屬性、在屬性集中排列它們，以及發佈這些屬性集的規格。</span><span class="sxs-lookup"><span data-stu-id="892aa-105">Hardware and filter vendors can define new capabilities as properties, arrange them in property sets, and publish the specification for these property sets.</span></span> <span data-ttu-id="892aa-106">應用程式開發人員可以使用 [**IKsPropertySet**](ikspropertyset.md) 介面的方法，來判斷驅動程式或篩選器是否支援一組特定的屬性，以及取得或設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="892aa-106">As the application developer, you can use the methods of the [**IKsPropertySet**](ikspropertyset.md) interface to determine whether a driver or filter supports a particular set of properties, and retrieve or set those properties.</span></span>

<span data-ttu-id="892aa-107">**IKsPropertySet** 所公開的所有方法都需要 **GUID** 來識別屬性集 (*guidPropSet* 參數) ，以及在 *dwPropID* 參數)  (屬性集內識別屬性的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="892aa-107">All the methods exposed by **IKsPropertySet** require a **GUID** that identifies the property set (the *guidPropSet* parameter) and a **DWORD** that identifies the property within the property set (the *dwPropID* parameter).</span></span> <span data-ttu-id="892aa-108">*DwPropID* 參數通常是列舉資料類型的成員。</span><span class="sxs-lookup"><span data-stu-id="892aa-108">The *dwPropID* parameter is typically a member of an enumerated data type.</span></span>

<span data-ttu-id="892aa-109">個別屬性可以有您在 [**IKsPropertySet：： Set**](ikspropertyset-set.md)和 [**IKsPropertySet：： Get**](ikspropertyset-get.md)方法的 *pPropData* 參數中指定的相關資料。</span><span class="sxs-lookup"><span data-stu-id="892aa-109">Individual properties can have associated data that you specify in the *pPropData* parameter in the [**IKsPropertySet::Set**](ikspropertyset-set.md) and [**IKsPropertySet::Get**](ikspropertyset-get.md) methods.</span></span> <span data-ttu-id="892aa-110">在這些方法中，屬性資料會輸入為的指標 `void` 。</span><span class="sxs-lookup"><span data-stu-id="892aa-110">In these methods, the property data is typed as a pointer to `void`.</span></span> <span data-ttu-id="892aa-111">資料類型和資料的意義是在屬性集的定義中指定。</span><span class="sxs-lookup"><span data-stu-id="892aa-111">The data type and the meaning of the data are specified in the definition of the property set.</span></span>

<span data-ttu-id="892aa-112">下列各節提供有關 DirectShow 所支援之屬性集的資訊：</span><span class="sxs-lookup"><span data-stu-id="892aa-112">The following sections provide information about the property sets supported in DirectShow:</span></span>

-   [<span data-ttu-id="892aa-113">**DVD 禁止複製屬性集**</span><span class="sxs-lookup"><span data-stu-id="892aa-113">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   [<span data-ttu-id="892aa-114">**DVD 卡拉卡拉屬性集**</span><span class="sxs-lookup"><span data-stu-id="892aa-114">**DVD Karaoke Property Set**</span></span>](dvd-karaoke-property-set.md)
-   [<span data-ttu-id="892aa-115">**DVD 子圖片屬性集**</span><span class="sxs-lookup"><span data-stu-id="892aa-115">**DVD Subpicture Property Set**</span></span>](dvd-subpicture-property-set.md)
-   [<span data-ttu-id="892aa-116">外部裝置傳輸屬性集</span><span class="sxs-lookup"><span data-stu-id="892aa-116">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
-   [<span data-ttu-id="892aa-117">框架逐步執行屬性集</span><span class="sxs-lookup"><span data-stu-id="892aa-117">Frame Stepping Property Set</span></span>](frame-stepping-property-set.md)
-   [<span data-ttu-id="892aa-118">釘選屬性集</span><span class="sxs-lookup"><span data-stu-id="892aa-118">Pin Property Set</span></span>](pin-property-set.md)
-   [<span data-ttu-id="892aa-119">**速率變更屬性集**</span><span class="sxs-lookup"><span data-stu-id="892aa-119">**Rate Change Property Set**</span></span>](rate-change-property-set.md)

 

 



