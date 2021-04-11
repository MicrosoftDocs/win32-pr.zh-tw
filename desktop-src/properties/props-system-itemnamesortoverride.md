---
description: 此字串應該設定為 CJK 地區設定的 ItemNameDisplay 中所定義之顯示名稱的拼音版本， (CHS 拼音、JPN 平假名、KOR 韓文等 ) 。
ms.assetid: eb491644-bf59-4439-9e9b-bcafde619d66
title: System. ItemNameSortOverride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79f9bb07eb15eb5d25fbfa1e95d4c0f80b35611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193956"
---
# <a name="systemitemnamesortoverride"></a><span data-ttu-id="08594-103">System. ItemNameSortOverride</span><span class="sxs-lookup"><span data-stu-id="08594-103">System.ItemNameSortOverride</span></span>

<span data-ttu-id="08594-104">此字串應該設定為 CJK 地區設定的 ItemNameDisplay 中所定義之顯示名稱的拼音版本， (CHS 拼音、JPN 平假名、KOR 韓文等 ) 。</span><span class="sxs-lookup"><span data-stu-id="08594-104">This string should be set to the phonetic version of the display name as defined in System.ItemNameDisplay in CJK locales(CHS Pinyin, JPN Hiragana, KOR Hangul, etc.).</span></span> <span data-ttu-id="08594-105">這個欄位的第一個字元也會用來依 firstletter 來分組名稱。</span><span class="sxs-lookup"><span data-stu-id="08594-105">The first character of this field is also used for grouping names by firstletter.</span></span> <span data-ttu-id="08594-106">對於大部分的非 CJK 語言，此欄位不需要設定 (在這種情況下，將會使用) 的 ItemNameDisplay。但是，如果您想要覆寫群組信件 (例如，移除「a」和「) 」等前置文章，可以在這裡提供替代字串。</span><span class="sxs-lookup"><span data-stu-id="08594-106">For most non-CJK languages, this field does not need to be set (in which case System.ItemNameDisplay will be used).However, if it is desirable to override the grouping letter (for example, to remove leading articles such as "a" and "the"),an alternate string can be provided here.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="08594-107">Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8</span><span class="sxs-lookup"><span data-stu-id="08594-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.ItemNameSortOverride
   shellPKey = PKEY_ItemNameSortOverride
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="08594-108">備註</span><span class="sxs-lookup"><span data-stu-id="08594-108">Remarks</span></span>

<span data-ttu-id="08594-109">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="08594-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08594-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="08594-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08594-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="08594-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="08594-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="08594-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="08594-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="08594-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="08594-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="08594-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="08594-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="08594-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="08594-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="08594-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="08594-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="08594-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="08594-118">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="08594-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="08594-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="08594-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="08594-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="08594-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="08594-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="08594-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="08594-122">editControl</span><span class="sxs-lookup"><span data-stu-id="08594-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="08594-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="08594-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="08594-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="08594-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
