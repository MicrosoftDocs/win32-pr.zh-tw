---
description: 評等系統，其使用介於0和5之間的整數值範圍。
ms.assetid: 50353ba9-86dd-4172-91b4-1898c8fc5522
title: System. SimpleRating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4741edd076b6027bc5f8dfbe3b2ff2a31374a7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000182"
---
# <a name="systemsimplerating"></a><span data-ttu-id="4ad77-103">System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="4ad77-103">System.SimpleRating</span></span>

<span data-ttu-id="4ad77-104">評等系統，其使用介於0和5之間的整數值範圍。</span><span class="sxs-lookup"><span data-stu-id="4ad77-104">A rating system that uses a range of integer values between 0 and 5.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="4ad77-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="4ad77-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.SimpleRating
   shellPKey = PKEY_SimpleRating
   formatID = A09F084E-AD41-489F-8076-AA5BE3082BCA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="4ad77-106">備註</span><span class="sxs-lookup"><span data-stu-id="4ad77-106">Remarks</span></span>

<span data-ttu-id="4ad77-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="4ad77-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="4ad77-108">為了與 Windows Vista Shell 分級系統相容，您的屬性處理常式也應該將對應填入 [system. 評](./props-system-rating.md) 等屬性，如該屬性所述。</span><span class="sxs-lookup"><span data-stu-id="4ad77-108">For compatibility with the Windows Vista Shell rating system, your property handler should also populate the [System.Rating](./props-system-rating.md) property with the mapping as described for that property.</span></span>

<span data-ttu-id="4ad77-109">您可以使用下表，從 [系統的評](./props-system-rating.md) 等轉換為 [SimpleRating]()。</span><span class="sxs-lookup"><span data-stu-id="4ad77-109">Use the following table to convert from [System.Rating](./props-system-rating.md) to [System.SimpleRating]().</span></span>



| <span data-ttu-id="4ad77-110">系統評分</span><span class="sxs-lookup"><span data-stu-id="4ad77-110">System.Rating</span></span> | <span data-ttu-id="4ad77-111">System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="4ad77-111">System.SimpleRating</span></span> |
|---------------|---------------------|
| <span data-ttu-id="4ad77-112">0</span><span class="sxs-lookup"><span data-stu-id="4ad77-112">0</span></span>             | <span data-ttu-id="4ad77-113">0</span><span class="sxs-lookup"><span data-stu-id="4ad77-113">0</span></span>                   |
| <span data-ttu-id="4ad77-114">1-12</span><span class="sxs-lookup"><span data-stu-id="4ad77-114">1-12</span></span>          | <span data-ttu-id="4ad77-115">1</span><span class="sxs-lookup"><span data-stu-id="4ad77-115">1</span></span>                   |
| <span data-ttu-id="4ad77-116">13-37</span><span class="sxs-lookup"><span data-stu-id="4ad77-116">13-37</span></span>         | <span data-ttu-id="4ad77-117">2</span><span class="sxs-lookup"><span data-stu-id="4ad77-117">2</span></span>                   |
| <span data-ttu-id="4ad77-118">38-62</span><span class="sxs-lookup"><span data-stu-id="4ad77-118">38-62</span></span>         | <span data-ttu-id="4ad77-119">3</span><span class="sxs-lookup"><span data-stu-id="4ad77-119">3</span></span>                   |
| <span data-ttu-id="4ad77-120">63-87</span><span class="sxs-lookup"><span data-stu-id="4ad77-120">63-87</span></span>         | <span data-ttu-id="4ad77-121">4</span><span class="sxs-lookup"><span data-stu-id="4ad77-121">4</span></span>                   |
| <span data-ttu-id="4ad77-122">88-99</span><span class="sxs-lookup"><span data-stu-id="4ad77-122">88-99</span></span>         | <span data-ttu-id="4ad77-123">5</span><span class="sxs-lookup"><span data-stu-id="4ad77-123">5</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="4ad77-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ad77-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ad77-125">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="4ad77-125">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="4ad77-126">searchInfo</span><span class="sxs-lookup"><span data-stu-id="4ad77-126">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="4ad77-127">labelInfo</span><span class="sxs-lookup"><span data-stu-id="4ad77-127">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="4ad77-128">typeInfo</span><span class="sxs-lookup"><span data-stu-id="4ad77-128">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="4ad77-129">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4ad77-129">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="4ad77-130">stringFormat</span><span class="sxs-lookup"><span data-stu-id="4ad77-130">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="4ad77-131">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="4ad77-131">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="4ad77-132">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="4ad77-132">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="4ad77-133">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="4ad77-133">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="4ad77-134">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="4ad77-134">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="4ad77-135">drawControl</span><span class="sxs-lookup"><span data-stu-id="4ad77-135">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="4ad77-136">editControl</span><span class="sxs-lookup"><span data-stu-id="4ad77-136">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="4ad77-137">filterControl</span><span class="sxs-lookup"><span data-stu-id="4ad77-137">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="4ad77-138">queryControl</span><span class="sxs-lookup"><span data-stu-id="4ad77-138">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
