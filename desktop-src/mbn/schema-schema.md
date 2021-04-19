---
description: 定義行動寬頻設定檔。
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: 行動寬頻設定檔架構參考
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425db1d38002e40969bb47c03952330dd6ccd26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972056"
---
# <a name="mobile-broadband-profile-schema-reference"></a><span data-ttu-id="ebcc0-103">行動寬頻設定檔架構參考</span><span class="sxs-lookup"><span data-stu-id="ebcc0-103">Mobile Broadband Profile Schema Reference</span></span>

<span data-ttu-id="ebcc0-104">Mobile 寬頻設定檔架構會定義行動寬頻設定檔。</span><span class="sxs-lookup"><span data-stu-id="ebcc0-104">The Mobile Broadband Profile Schema defines a Mobile Broadband Profile.</span></span>

<span data-ttu-id="ebcc0-105">設定檔儲存行動寬頻連線相關使用者和網路設定參數。</span><span class="sxs-lookup"><span data-stu-id="ebcc0-105">Profiles store Mobile Broadband connection related user and network configuration parameters.</span></span> <span data-ttu-id="ebcc0-106">它們也會儲存連接的使用者喜好設定。</span><span class="sxs-lookup"><span data-stu-id="ebcc0-106">They also store the user preferences for a connection.</span></span>

<span data-ttu-id="ebcc0-107">行動寬頻設定檔的根項目是 [**MBNProfile**](schema-mbnprofile-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="ebcc0-107">The root element of a Mobile Broadband profile is the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span> <span data-ttu-id="ebcc0-108">每個設定檔都只會有一個根項目。</span><span class="sxs-lookup"><span data-stu-id="ebcc0-108">Each profile has exactly one root element.</span></span> <span data-ttu-id="ebcc0-109">Windows 7 使用的所有行動寬頻設定檔架構元素都在命名空間中 `https://www.microsoft.com/networking/WWAN/profile/v1` ，而 Windows 8 所使用的元素則在命名空間中 `https://www.microsoft.com/networking/WWAN/profile/v2` 。</span><span class="sxs-lookup"><span data-stu-id="ebcc0-109">All Mobile Broadband Profile Schema elements used by Windows 7 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v1` and the elements used by Windows 8 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v2`.</span></span>

<span data-ttu-id="ebcc0-110">Mobile 寬頻設定檔架構會嚴格地強制執行節點的順序。</span><span class="sxs-lookup"><span data-stu-id="ebcc0-110">The Mobile Broadband Profile Schema strictly enforces the order of the nodes.</span></span> <span data-ttu-id="ebcc0-111">設定檔中指定的節點必須遵守行動 **寬頻設定檔架構** ，並且以架構定義中指定的順序顯示。</span><span class="sxs-lookup"><span data-stu-id="ebcc0-111">Nodes specified in a profile must adhere to the **Mobile Broadband Profile Schema** and appear in the order prescribed in the schema definition.</span></span> <span data-ttu-id="ebcc0-112">例如， [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) 必須在 [**AccessString**](schema-accessstring-contexttype-element.md)之後立即指定。</span><span class="sxs-lookup"><span data-stu-id="ebcc0-112">For example, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) must be specified immediately after [**AccessString**](schema-accessstring-contexttype-element.md).</span></span>

-   [<span data-ttu-id="ebcc0-113">Mobile 寬頻設定檔架構 v1</span><span class="sxs-lookup"><span data-stu-id="ebcc0-113">Mobile Broadband Profile Schema v1</span></span>](mobile-broadband-profile-schema.md)
-   [<span data-ttu-id="ebcc0-114">Mobile 寬頻設定檔架構 v2</span><span class="sxs-lookup"><span data-stu-id="ebcc0-114">Mobile Broadband Profile Schema v2</span></span>](mobile-broadband-profile-schema-v2.md)
-   [<span data-ttu-id="ebcc0-115">Mobile 寬頻設定檔架構 v3</span><span class="sxs-lookup"><span data-stu-id="ebcc0-115">Mobile Broadband Profile Schema v3</span></span>](mobile-broadband-profile-schema-v3.md)
-   <span data-ttu-id="ebcc0-116">[Mobile 寬頻設定檔架構 v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebcc0-116">[Mobile Broadband Profile Schema v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span></span>

 

 
