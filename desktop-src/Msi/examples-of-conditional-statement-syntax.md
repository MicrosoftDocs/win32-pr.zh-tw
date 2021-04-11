---
description: 以下提供一些常見的條件陳述式實例。 如需詳細資訊，請參閱條件陳述式語法。
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: 條件陳述式語法的範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca91a2b3e89160fad19ad5d9b1c6a3d33929e5d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943934"
---
# <a name="examples-of-conditional-statement-syntax"></a><span data-ttu-id="470fc-104">條件陳述式語法的範例</span><span class="sxs-lookup"><span data-stu-id="470fc-104">Examples of Conditional Statement Syntax</span></span>

<span data-ttu-id="470fc-105">以下提供一些常見的條件陳述式實例。</span><span class="sxs-lookup"><span data-stu-id="470fc-105">The following provides some common instances of conditional statements.</span></span> <span data-ttu-id="470fc-106">如需詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="470fc-106">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

## <a name="run-action-on-removal"></a><span data-ttu-id="470fc-107">移除時執行動作。</span><span class="sxs-lookup"><span data-stu-id="470fc-107">Run action on removal.</span></span>

<span data-ttu-id="470fc-108">如需詳細資訊，請參閱 [移除時要執行的調節動作](conditioning-actions-to-run-during-removal.md)。</span><span class="sxs-lookup"><span data-stu-id="470fc-108">For information, see [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span>

## <a name="run-action-only-if-the-product-has-not-been-installed"></a><span data-ttu-id="470fc-109">只有在尚未安裝產品時，才執行動作。</span><span class="sxs-lookup"><span data-stu-id="470fc-109">Run action only if the product has not been installed.</span></span>

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a><span data-ttu-id="470fc-110">只有在將產品安裝在本機時，才執行動作。</span><span class="sxs-lookup"><span data-stu-id="470fc-110">Run action only if the product will be installed local.</span></span> <span data-ttu-id="470fc-111">請勿在重新安裝時執行動作。</span><span class="sxs-lookup"><span data-stu-id="470fc-111">Do not run action on a reinstallation.</span></span>

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

<span data-ttu-id="470fc-112">「&功能人員 = 3」一詞表示動作是在本機安裝功能。</span><span class="sxs-lookup"><span data-stu-id="470fc-112">The term "&FeatureName=3" means the action is to install the feature local.</span></span> <span data-ttu-id="470fc-113">「不 (！」一詞功能說明 = 3) 」表示功能未安裝在本機。</span><span class="sxs-lookup"><span data-stu-id="470fc-113">The term "NOT(!FeatureName=3)" means the feature is not installed local.</span></span>

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a><span data-ttu-id="470fc-114">只有在即將卸載功能時，才執行動作。</span><span class="sxs-lookup"><span data-stu-id="470fc-114">Run action only if the feature will be uninstalled.</span></span>

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

<span data-ttu-id="470fc-115">這種情況只會檢查功能是否從本機的已安裝狀態轉換為不存在的狀態。</span><span class="sxs-lookup"><span data-stu-id="470fc-115">This condition only checks for a transition of the feature from an installed state of local to the absent state.</span></span>

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a><span data-ttu-id="470fc-116">只有在元件已安裝在本機，但正在轉換為狀態時，才執行動作。</span><span class="sxs-lookup"><span data-stu-id="470fc-116">Run action only if the component was installed local, but is transitioning out of state.</span></span>

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

<span data-ttu-id="470fc-117">「？」一詞ComponetName = 3 "表示元件是安裝在本機。</span><span class="sxs-lookup"><span data-stu-id="470fc-117">The term "?ComponetName=3" means the component is installed local.</span></span> <span data-ttu-id="470fc-118">「$ComponentName = 2」一詞表示元件上的動作狀態不存在。</span><span class="sxs-lookup"><span data-stu-id="470fc-118">The term "$ComponentName=2" means that the action state on the component is Absent.</span></span> <span data-ttu-id="470fc-119">「$ComponentName = 4」一詞表示元件上的動作狀態是從來源執行。</span><span class="sxs-lookup"><span data-stu-id="470fc-119">The term "$ComponentName=4" means that the action state on the component is run from source.</span></span> <span data-ttu-id="470fc-120">請注意，公告的動作狀態對元件無效。</span><span class="sxs-lookup"><span data-stu-id="470fc-120">Note that an action state of advertise is not valid for a component.</span></span>

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a><span data-ttu-id="470fc-121">只在重新安裝元件時執行動作。</span><span class="sxs-lookup"><span data-stu-id="470fc-121">Run action only on the reinstallation of a component.</span></span>

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a><span data-ttu-id="470fc-122">只在套用特定修補程式時執行動作。</span><span class="sxs-lookup"><span data-stu-id="470fc-122">Run action only when a particular patch is applied.</span></span>

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

<span data-ttu-id="470fc-123">如需詳細資訊，請參閱 [ [**修補**](patch.md) ] 屬性頁上的 [備註] 區段。</span><span class="sxs-lookup"><span data-stu-id="470fc-123">For more information, see the Remarks section on the [**PATCH**](patch.md) property page.</span></span>

 

 



