---
description: ItemNameDisplay 屬性的基底名稱。
ms.assetid: 8add2d72-efd3-4971-89d9-428190115ba0
title: System.servicemodel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5ba987d8bdcd966724c15f0632edbfc8eb3d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944086"
---
# <a name="systemitemname"></a><span data-ttu-id="0e481-103">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="0e481-103">System.ItemName</span></span>

<span data-ttu-id="0e481-104">[ItemNameDisplay](./props-system-itemnamedisplay.md)屬性的基底名稱。</span><span class="sxs-lookup"><span data-stu-id="0e481-104">The base name of the [System.ItemNameDisplay](./props-system-itemnamedisplay.md) property.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="0e481-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="0e481-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemName
   shellPKey = PKEY_ItemName
   formatID = 6B8DA074-3B5C-43BC-886F-0A2CDCE00B6F
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="0e481-106">備註</span><span class="sxs-lookup"><span data-stu-id="0e481-106">Remarks</span></span>

<span data-ttu-id="0e481-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="0e481-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="0e481-108">如果專案是檔案，則在所有情況下，這個屬性會包含副檔名，而且如果有當地語系化的名稱可供使用，則會進行當地語系化。</span><span class="sxs-lookup"><span data-stu-id="0e481-108">If the item is a file, this property includes the extension in all cases and is localized if a localized name is available.</span></span> <span data-ttu-id="0e481-109">如果專案是訊息，這個屬性的值就不會包含轉送或回復首碼。</span><span class="sxs-lookup"><span data-stu-id="0e481-109">If the item is a message, the value of this property does not include the forwarding or reply prefixes.</span></span> <span data-ttu-id="0e481-110">如需詳細資訊，請參閱 [ItemNamePrefix](./props-system-itemnameprefix.md) 。</span><span class="sxs-lookup"><span data-stu-id="0e481-110">See [System.ItemNamePrefix](./props-system-itemnameprefix.md) for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e481-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e481-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e481-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="0e481-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="0e481-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="0e481-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="0e481-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="0e481-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="0e481-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="0e481-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="0e481-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="0e481-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="0e481-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="0e481-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="0e481-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="0e481-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="0e481-119">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="0e481-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="0e481-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0e481-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="0e481-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="0e481-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="0e481-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="0e481-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="0e481-123">editControl</span><span class="sxs-lookup"><span data-stu-id="0e481-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="0e481-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="0e481-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="0e481-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="0e481-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
