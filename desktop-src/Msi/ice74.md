---
description: ICE74 會確認 FASTOEM 屬性尚未撰寫至屬性資料表。
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fe2762710e061f2c88f55893294a40fbac8700f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974322"
---
# <a name="ice74"></a><span data-ttu-id="18f07-103">ICE74</span><span class="sxs-lookup"><span data-stu-id="18f07-103">ICE74</span></span>

<span data-ttu-id="18f07-104">ICE74 會確認 [**FASTOEM**](fastoem.md) 屬性尚未撰寫至 [屬性資料表](property-table.md)。</span><span class="sxs-lookup"><span data-stu-id="18f07-104">ICE74 verifies that the [**FASTOEM**](fastoem.md) property has not been authored into the [Property table](property-table.md).</span></span>

<span data-ttu-id="18f07-105">[**FASTOEM**](fastoem.md)屬性可讓 oem 縮短第一次安裝 Windows Installer 應用程式所需的時間。</span><span class="sxs-lookup"><span data-stu-id="18f07-105">The [**FASTOEM**](fastoem.md) property enables OEMs to reduce the time required to install Windows Installer applications for the first time.</span></span> <span data-ttu-id="18f07-106">它無法在第一次安裝之後使用。</span><span class="sxs-lookup"><span data-stu-id="18f07-106">It cannot be used after the first install.</span></span> <span data-ttu-id="18f07-107">**FASTOEM** 屬性不能在屬性工作表中撰寫，因為這會干擾應用程式的維護、移除或修復後續安裝。</span><span class="sxs-lookup"><span data-stu-id="18f07-107">The **FASTOEM** property must not be authored in the Property table because this interferes with subsequent installations for the maintenance, removal, or repair of the application.</span></span>

<span data-ttu-id="18f07-108">ICE74 也會確認 [**UpgradeCode**](upgradecode.md) 屬性已撰寫至 [屬性工作表](property-table.md)，而且其值不是 null GUID {00000000-0000-0000-0000-000000000000} 。</span><span class="sxs-lookup"><span data-stu-id="18f07-108">ICE74 also verifies that the [**UpgradeCode**](upgradecode.md) property is authored into the [Property table](property-table.md), and that its value is not a null GUID, {00000000-0000-0000-0000-000000000000}.</span></span>

## <a name="result"></a><span data-ttu-id="18f07-109">結果</span><span class="sxs-lookup"><span data-stu-id="18f07-109">Result</span></span>

<span data-ttu-id="18f07-110">ICE74 可以張貼下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="18f07-110">ICE74 can post the following errors.</span></span>



| <span data-ttu-id="18f07-111">ICE74 錯誤</span><span class="sxs-lookup"><span data-stu-id="18f07-111">ICE74 error</span></span>                                                                       | <span data-ttu-id="18f07-112">Description</span><span class="sxs-lookup"><span data-stu-id="18f07-112">Description</span></span>                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18f07-113">[**FASTOEM**](fastoem.md)屬性無法在屬性工作表中撰寫。</span><span class="sxs-lookup"><span data-stu-id="18f07-113">The [**FASTOEM**](fastoem.md) property cannot be authored in the Property table.</span></span> | <span data-ttu-id="18f07-114">已在屬性工作表中設定 [**FASTOEM**](fastoem.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="18f07-114">The [**FASTOEM**](fastoem.md) property has been set in the Property table.</span></span>                             |
| <span data-ttu-id="18f07-115">' \[ 2 \] ' 不是有效的 [**UpgradeCode**](upgradecode.md)。</span><span class="sxs-lookup"><span data-stu-id="18f07-115">'\[2\]' is not a valid [**UpgradeCode**](upgradecode.md).</span></span>                        | <span data-ttu-id="18f07-116">在屬性資料表中， [**UpgradeCode**](upgradecode.md) 屬性已輸入 null GUID。</span><span class="sxs-lookup"><span data-stu-id="18f07-116">A null GUID has been entered for the [**UpgradeCode**](upgradecode.md) property in the Property table.</span></span> |



 

<span data-ttu-id="18f07-117">ICE74 可以張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="18f07-117">ICE74 can post the following warning.</span></span>



| <span data-ttu-id="18f07-118">ICE74 警告</span><span class="sxs-lookup"><span data-stu-id="18f07-118">ICE74 warning</span></span>                                                                                                                                                                                             | <span data-ttu-id="18f07-119">Description</span><span class="sxs-lookup"><span data-stu-id="18f07-119">Description</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18f07-120">[**UpgradeCode**](upgradecode.md)屬性不是在屬性工作表中撰寫的。</span><span class="sxs-lookup"><span data-stu-id="18f07-120">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> <span data-ttu-id="18f07-121">強烈建議安裝套件的作者為其應用程式指定 **UpgradeCode** 。</span><span class="sxs-lookup"><span data-stu-id="18f07-121">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span> | <span data-ttu-id="18f07-122">[**UpgradeCode**](upgradecode.md)屬性不是在屬性工作表中撰寫的。</span><span class="sxs-lookup"><span data-stu-id="18f07-122">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> |



 

## <a name="example"></a><span data-ttu-id="18f07-123">範例</span><span class="sxs-lookup"><span data-stu-id="18f07-123">Example</span></span>

<span data-ttu-id="18f07-124">如果設定 [**FASTOEM**](fastoem.md) 屬性，ICE74 會報告下列錯誤： FASTOEM</span><span class="sxs-lookup"><span data-stu-id="18f07-124">ICE74 reports the following error if the [**FASTOEM**](fastoem.md) property is set: The FASTOEM</span></span>

``` syntax
 property cannot be authored in the Property table.
```

<span data-ttu-id="18f07-125">[屬性工作表](property-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="18f07-125">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="18f07-126">屬性</span><span class="sxs-lookup"><span data-stu-id="18f07-126">Property</span></span>                   | <span data-ttu-id="18f07-127">值</span><span class="sxs-lookup"><span data-stu-id="18f07-127">Value</span></span> |
|----------------------------|-------|
| [<span data-ttu-id="18f07-128">**FASTOEM**</span><span class="sxs-lookup"><span data-stu-id="18f07-128">**FASTOEM**</span></span>](fastoem.md) | <span data-ttu-id="18f07-129">1</span><span class="sxs-lookup"><span data-stu-id="18f07-129">1</span></span>     |



 

<span data-ttu-id="18f07-130">若要修正這個錯誤，請從屬性資料表中移除 [**FASTOEM**](fastoem.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="18f07-130">To fix this error remove the [**FASTOEM**](fastoem.md) property from the Property Table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18f07-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="18f07-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18f07-132">**FASTOEM 屬性**</span><span class="sxs-lookup"><span data-stu-id="18f07-132">**FASTOEM property**</span></span>](fastoem.md)
</dt> <dt>

[<span data-ttu-id="18f07-133">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="18f07-133">Property table</span></span>](property-table.md)
</dt> <dt>

[<span data-ttu-id="18f07-134">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="18f07-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



