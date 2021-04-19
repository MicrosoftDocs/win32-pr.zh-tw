---
description: WMI 提供者通常是設計來提供單一電腦上特定受管理物件的相關資訊。
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: 將類別連結在一起
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c36956d20d9390462577332e7ac7b644d4ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984237"
---
# <a name="linking-classes-together"></a><span data-ttu-id="6ade5-103">將類別連結在一起</span><span class="sxs-lookup"><span data-stu-id="6ade5-103">Linking Classes Together</span></span>

<span data-ttu-id="6ade5-104">WMI 提供者通常是設計來提供單一電腦上特定受管理物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6ade5-104">WMI providers are usually designed to provide information about a specific managed object on a single computer.</span></span> <span data-ttu-id="6ade5-105">如果有一個通用屬性可作為索引鍵來唯一識別所有不同的來源實例，則請使用 [View 提供者](view-provider.md) 將不同類別、命名空間或電腦的屬性合併為單一類別。</span><span class="sxs-lookup"><span data-stu-id="6ade5-105">If there is a common property that can serve as a key to uniquely identify all the different source instances, then use the [View Provider](view-provider.md) to combine properties from different classes, namespaces, or computers into a single class.</span></span>

<span data-ttu-id="6ade5-106">您必須先 [註冊 View Provider](registering-the-view-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="6ade5-106">You must first [register the View Provider](registering-the-view-provider.md).</span></span> <span data-ttu-id="6ade5-107">註冊之後，您可以建立下列類型的 view 類別：</span><span class="sxs-lookup"><span data-stu-id="6ade5-107">After registration, you can create the following types of view classes:</span></span>

-   [<span data-ttu-id="6ade5-108">聯結視圖</span><span class="sxs-lookup"><span data-stu-id="6ade5-108">Join view</span></span>](creating-a-new-instance-from-old-properties.md)

    <span data-ttu-id="6ade5-109">由通用屬性值連接之不同類別的實例。</span><span class="sxs-lookup"><span data-stu-id="6ade5-109">Instances of different classes connected by a common property value.</span></span>

-   [<span data-ttu-id="6ade5-110">相關檢視</span><span class="sxs-lookup"><span data-stu-id="6ade5-110">Association view</span></span>](associating-instances-between-namespaces.md)

    <span data-ttu-id="6ade5-111">跨命名空間界限的現有關聯類別的視圖。</span><span class="sxs-lookup"><span data-stu-id="6ade5-111">Views of existing association classes across the namespace boundary.</span></span>

-   [<span data-ttu-id="6ade5-112">聯集視圖</span><span class="sxs-lookup"><span data-stu-id="6ade5-112">Union view</span></span>](creating-a-union-view-class.md)

    <span data-ttu-id="6ade5-113">一或多個實例的聯集。</span><span class="sxs-lookup"><span data-stu-id="6ade5-113">Union of one or more instances.</span></span>

 

 



