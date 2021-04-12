---
description: 此屬性代表自建立檔之後，每次開啟和儲存之間累積的總時間。 這會以100ns 個單位來測量，而不是以毫秒為單位。 \_適用于 IPropertySetStorage 處理常式的 VT FILETIME (舊版) 。
ms.assetid: 27d374ae-366c-4b2c-88a8-93e760db6fba
title: System.Doc>ument。TotalEditingTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b135433713028d302ed4dac82b530a332917434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319744"
---
# <a name="systemdocumenttotaleditingtime"></a><span data-ttu-id="85bd6-105">System.Doc>ument。TotalEditingTime</span><span class="sxs-lookup"><span data-stu-id="85bd6-105">System.Document.TotalEditingTime</span></span>

<span data-ttu-id="85bd6-106">此屬性代表自建立檔之後，每次開啟和儲存之間累積的總時間。</span><span class="sxs-lookup"><span data-stu-id="85bd6-106">This property represents the total time between each open and save, accumulated since the creation of the document.</span></span> <span data-ttu-id="85bd6-107">這會以100ns 個單位來測量，而不是以毫秒為單位。</span><span class="sxs-lookup"><span data-stu-id="85bd6-107">This is measured in 100ns units, not milliseconds.</span></span> <span data-ttu-id="85bd6-108">\_適用于 IPropertySetStorage 處理常式的 VT FILETIME (舊版) </span><span class="sxs-lookup"><span data-stu-id="85bd6-108">VT\_FILETIME for IPropertySetStorage handlers (legacy)</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="85bd6-109">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="85bd6-109">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Document.TotalEditingTime
   shellPKey = PKEY_Document_TotalEditingTime
   formatID = F29F85E0-4FF9-1068-AB91-08002B27B3D9
   propID = 10
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt64
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="85bd6-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85bd6-110">Windows Vista</span></span>

```
propertyDescription
   name = System.Document.TotalEditingTime
   shellPKey = PKEY_Document_TotalEditingTime
   formatID = F29F85E0-4FF9-1068-AB91-08002B27B3D9
   propID = 10
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt64
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="85bd6-111">備註</span><span class="sxs-lookup"><span data-stu-id="85bd6-111">Remarks</span></span>

<span data-ttu-id="85bd6-112">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="85bd6-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85bd6-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="85bd6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85bd6-114">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="85bd6-114">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="85bd6-115">searchInfo</span><span class="sxs-lookup"><span data-stu-id="85bd6-115">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="85bd6-116">labelInfo</span><span class="sxs-lookup"><span data-stu-id="85bd6-116">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="85bd6-117">typeInfo</span><span class="sxs-lookup"><span data-stu-id="85bd6-117">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="85bd6-118">displayInfo</span><span class="sxs-lookup"><span data-stu-id="85bd6-118">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="85bd6-119">stringFormat</span><span class="sxs-lookup"><span data-stu-id="85bd6-119">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="85bd6-120">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="85bd6-120">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="85bd6-121">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="85bd6-121">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="85bd6-122">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="85bd6-122">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="85bd6-123">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="85bd6-123">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="85bd6-124">drawControl</span><span class="sxs-lookup"><span data-stu-id="85bd6-124">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="85bd6-125">editControl</span><span class="sxs-lookup"><span data-stu-id="85bd6-125">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="85bd6-126">filterControl</span><span class="sxs-lookup"><span data-stu-id="85bd6-126">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="85bd6-127">queryControl</span><span class="sxs-lookup"><span data-stu-id="85bd6-127">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
