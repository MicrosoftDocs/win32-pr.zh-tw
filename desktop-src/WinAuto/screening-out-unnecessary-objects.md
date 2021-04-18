---
title: 篩選掉不必要的物件
description: 如果您使用 [檢查] 檢查 Microsoft WordPad 配件中的簡單控制項，例如 [確定] 按鈕，您可以看到這些父視窗物件也包含數個不可見的子物件。
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996550"
---
# <a name="screening-out-unnecessary-objects"></a><span data-ttu-id="38dce-103">篩選掉不必要的物件</span><span class="sxs-lookup"><span data-stu-id="38dce-103">Screening Out Unnecessary Objects</span></span>

<span data-ttu-id="38dce-104">如果您使用 [ [檢查](inspect-objects.md) ] 檢查 Microsoft WordPad 配件中的簡單控制項，例如 [確定] 按鈕，您可以看到這些父視窗物件也包含數個不可見的子物件。</span><span class="sxs-lookup"><span data-stu-id="38dce-104">If you use [Inspect](inspect-objects.md) to examine a simple control such as an OK push button in the Microsoft WordPad accessory, you can see that these parent window objects also contain several invisible child objects.</span></span> <span data-ttu-id="38dce-105">這些隱藏的物件具有與控制項相同的視窗類別名稱，且具有 [**狀態 \_ 系統 \_ 不可見**](object-state-constants.md)的 [狀態屬性](state-property.md)。</span><span class="sxs-lookup"><span data-stu-id="38dce-105">These invisible objects have the same window class name as the control and have the [State property](state-property.md) of [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> <span data-ttu-id="38dce-106">下表列出 Microsoft Active Accessibility 為控制項建立的不可見子物件。</span><span class="sxs-lookup"><span data-stu-id="38dce-106">The following table lists the invisible child objects that Microsoft Active Accessibility creates for the control.</span></span>



| <span data-ttu-id="38dce-107">Name</span><span class="sxs-lookup"><span data-stu-id="38dce-107">Name</span></span>          | <span data-ttu-id="38dce-108">角色</span><span class="sxs-lookup"><span data-stu-id="38dce-108">Role</span></span>                                                                  | <span data-ttu-id="38dce-109">ChildCount</span><span class="sxs-lookup"><span data-stu-id="38dce-109">ChildCount</span></span> |
|---------------|-----------------------------------------------------------------------|------------|
| <span data-ttu-id="38dce-110">系統</span><span class="sxs-lookup"><span data-stu-id="38dce-110">"System"</span></span>      | [<span data-ttu-id="38dce-111">**角色 \_ 系統 \_ 功能表列**</span><span class="sxs-lookup"><span data-stu-id="38dce-111">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="38dce-112">0</span><span class="sxs-lookup"><span data-stu-id="38dce-112">0</span></span>          |
| <span data-ttu-id="38dce-113">無</span><span class="sxs-lookup"><span data-stu-id="38dce-113">None</span></span>          | [<span data-ttu-id="38dce-114">**角色 \_ 系統 \_ 標題列**</span><span class="sxs-lookup"><span data-stu-id="38dce-114">**ROLE\_SYSTEM\_TITLEBAR**</span></span>](object-roles.md)   | <span data-ttu-id="38dce-115">5</span><span class="sxs-lookup"><span data-stu-id="38dce-115">5</span></span>          |
| <span data-ttu-id="38dce-116">程式</span><span class="sxs-lookup"><span data-stu-id="38dce-116">"Application"</span></span> | [<span data-ttu-id="38dce-117">**角色 \_ 系統 \_ 功能表列**</span><span class="sxs-lookup"><span data-stu-id="38dce-117">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="38dce-118">0</span><span class="sxs-lookup"><span data-stu-id="38dce-118">0</span></span>          |
| <span data-ttu-id="38dce-119">縱</span><span class="sxs-lookup"><span data-stu-id="38dce-119">"Vertical"</span></span>    | [<span data-ttu-id="38dce-120">**角色 \_ 系統 \_ 捲軸**</span><span class="sxs-lookup"><span data-stu-id="38dce-120">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="38dce-121">5</span><span class="sxs-lookup"><span data-stu-id="38dce-121">5</span></span>          |
| <span data-ttu-id="38dce-122">方向</span><span class="sxs-lookup"><span data-stu-id="38dce-122">"Horizontal"</span></span>  | [<span data-ttu-id="38dce-123">**角色 \_ 系統 \_ 捲軸**</span><span class="sxs-lookup"><span data-stu-id="38dce-123">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="38dce-124">5</span><span class="sxs-lookup"><span data-stu-id="38dce-124">5</span></span>          |
| <span data-ttu-id="38dce-125">"Size Box"</span><span class="sxs-lookup"><span data-stu-id="38dce-125">"Size Box"</span></span>    | [<span data-ttu-id="38dce-126">**角色 \_ 系統 \_ 抓住**</span><span class="sxs-lookup"><span data-stu-id="38dce-126">**ROLE\_SYSTEM\_GRIP**</span></span>](object-roles.md)           | <span data-ttu-id="38dce-127">0</span><span class="sxs-lookup"><span data-stu-id="38dce-127">0</span></span>          |



 

<span data-ttu-id="38dce-128">用戶端開發人員必須識別並篩選出這些父視窗物件和不可見的子物件，因為它們不會提供有意義的資訊給終端使用者。</span><span class="sxs-lookup"><span data-stu-id="38dce-128">Client developers must identify and filter out these parent window objects and invisible child objects because they do not provide meaningful information to end users.</span></span>

 

 




