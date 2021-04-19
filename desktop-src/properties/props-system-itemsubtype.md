---
description: 描述專案的子類型。
ms.assetid: 7b949b2a-77c9-41d3-90f3-f2ba4cfa2762
title: System. ItemSubType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8132c2df1b532a4452006cadb661b082d0c6ef69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974090"
---
# <a name="systemitemsubtype"></a><span data-ttu-id="b7704-103">System. ItemSubType</span><span class="sxs-lookup"><span data-stu-id="b7704-103">System.ItemSubType</span></span>

<span data-ttu-id="b7704-104">描述專案的子類型。</span><span class="sxs-lookup"><span data-stu-id="b7704-104">Describes the sub-type of an item.</span></span> <span data-ttu-id="b7704-105">此值是為了向使用者顯示。相較于 System.object，通常用來描述 itemsthat 類別的一般內容格式，ItemSubType 可能會根據專案的個別內容或用途而有所不同。例如，您可以使用這個屬性來識別具有 system.string = "jpg" 的專案，例如 ItemSubType = "全景" 或 ItemSubType = "Smart 照"。</span><span class="sxs-lookup"><span data-stu-id="b7704-105">The value is intended for display to the user.In contrast to System.ItemType, which is generally used to describe a class of itemsthat all have the same common content format, System.ItemSubType may differ based onthe individual contents or purpose of the item.For example, this property may be used to identify an item with System.ItemType = "jpg"as System.ItemSubType = "Panorama" or System.ItemSubType = "Smart Shot".</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507"></a><span data-ttu-id="b7704-106">Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、1507版</span><span class="sxs-lookup"><span data-stu-id="b7704-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507</span></span>

```
propertyDescription
   name = System.ItemSubType
   shellPKey = PKEY_ItemSubType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 37
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="b7704-107">備註</span><span class="sxs-lookup"><span data-stu-id="b7704-107">Remarks</span></span>

<span data-ttu-id="b7704-108">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="b7704-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7704-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7704-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7704-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="b7704-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="b7704-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="b7704-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="b7704-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="b7704-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="b7704-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="b7704-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="b7704-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="b7704-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="b7704-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="b7704-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="b7704-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="b7704-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="b7704-117">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="b7704-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="b7704-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="b7704-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="b7704-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="b7704-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="b7704-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="b7704-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="b7704-121">editControl</span><span class="sxs-lookup"><span data-stu-id="b7704-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="b7704-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="b7704-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="b7704-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="b7704-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
