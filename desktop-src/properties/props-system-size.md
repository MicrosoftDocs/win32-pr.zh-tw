---
description: 系統提供的專案檔案系統大小（以位元組為單位）。
ms.assetid: 471c38fc-2382-4df8-8f70-e1af0dd6c746
title: System. Size
ms.topic: article
ms.date: 09/10/2019
ms.openlocfilehash: 4d0e988f4a757e6aa2e7d2dd611594d7705bd9ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321123"
---
# <a name="systemsize"></a><span data-ttu-id="84ffc-103">System. Size</span><span class="sxs-lookup"><span data-stu-id="84ffc-103">System.Size</span></span>

<span data-ttu-id="84ffc-104">系統提供的專案檔案系統大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="84ffc-104">The system-provided file system size of the item, in bytes.</span></span>

## <a name="windows-10-version-1809-and-later"></a><span data-ttu-id="84ffc-105">Windows 10 1809 版與更新版本</span><span class="sxs-lookup"><span data-stu-id="84ffc-105">Windows 10, version 1809 and later</span></span>

```
propertyDescription
   name = System.Size
   shellPKey = PKEY_Size
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = Empty
            minValue = 0
            setValue = 0
            text = Empty (0 KB)
            defineToken = SIZE_EMPTY
            mnemonics = empty
         enumRange
            name = Tiny
            minValue = 1
            setValue = 1
            text = Tiny (0 - 16 KB)
            defineToken = SIZE_TINY
            mnemonics = tiny
         enumRange
            name = Small
            minValue = 16383
            setValue = 16383
            text = Small (16 - 1 MB)
            defineToken = SIZE_SMALL
            mnemonics = small
         enumRange
            name = Medium
            minValue = 1048577
            setValue = 1048577
            text = Medium (1 - 128 MB)
            defineToken = SIZE_MEDIUM
            mnemonics = medium
         enumRange
            name = Large
            minValue = 134217729
            setValue = 134217729
            text = Large (128 MB - 1 GB)
            defineToken = SIZE_LARGE
            mnemonics = large
         enumRange
            name = Huge
            minValue = 1073741825
            setValue = 1073741825
            text = Huge (1 - 4 GB)
            defineToken = SIZE_HUGE
            mnemonics = huge
         enumRange
            name = Gigantic
            minValue = 4294967297
            setValue = 4294967297
            text = Gigantic (>4 GB)
            defineToken = SIZE_GIGANTIC
            mnemonics = gigantic
```

## <a name="windows-7-through-windows-10-version-1803"></a><span data-ttu-id="84ffc-106">Windows 7 到 Windows 10，版本1803</span><span class="sxs-lookup"><span data-stu-id="84ffc-106">Windows 7 through Windows 10, version 1803</span></span>

```
propertyDescription
   name = System.Size
   shellPKey = PKEY_Size
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = Empty
            minValue = 0
            setValue = 0
            text = Empty (0 KB)
            defineToken = SIZE_EMPTY
            mnemonics = empty
         enumRange
            name = Tiny
            minValue = 1
            setValue = 1
            text = Tiny (0 - 10 KB)
            defineToken = SIZE_TINY
            mnemonics = tiny
         enumRange
            name = Small
            minValue = 10241
            setValue = 10241
            text = Small (10 - 100 KB)
            defineToken = SIZE_SMALL
            mnemonics = small
         enumRange
            name = Medium
            minValue = 102401
            setValue = 102401
            text = Medium (100 KB - 1 MB)
            defineToken = SIZE_MEDIUM
            mnemonics = medium
         enumRange
            name = Large
            minValue = 1048577
            setValue = 1048577
            text = Large (1 - 16 MB)
            defineToken = SIZE_LARGE
            mnemonics = large
         enumRange
            name = Huge
            minValue = 16777217
            setValue = 16777217
            text = Huge (16 - 128 MB)
            defineToken = SIZE_HUGE
            mnemonics = huge
         enumRange
            name = Gigantic
            minValue = 134217729
            setValue = 134217729
            text = Gigantic (>128 MB)
            defineToken = SIZE_GIGANTIC
            mnemonics = gigantic
```

## <a name="windows-vista"></a><span data-ttu-id="84ffc-107">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84ffc-107">Windows Vista</span></span>

```
propertyDescription
   name = System.Size
   shellPKey = PKEY_Size
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 12
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0 KB
            mnemonics = empty
         enumRange
            minValue = 1
            setValue = 1
            text = 0 - 10 KB
            mnemonics = tiny
         enumRange
            minValue = 10241
            setValue = 10241
            text = 10 - 100 KB
            mnemonics = small
         enumRange
            minValue = 102401
            setValue = 102401
            text = 100 KB - 1 MB
            mnemonics = medium
         enumRange
            minValue = 1048577
            setValue = 1048577
            text = 1 - 16 MB
            mnemonics = large
         enumRange
            minValue = 16777217
            setValue = 16777217
            text = 16 - 128 MB
            mnemonics = huge
         enumRange
            minValue = 134217729
            setValue = 134217729
            text = >128 MB
            mnemonics = gigantic
```

## <a name="remarks"></a><span data-ttu-id="84ffc-108">備註</span><span class="sxs-lookup"><span data-stu-id="84ffc-108">Remarks</span></span>

<span data-ttu-id="84ffc-109">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="84ffc-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84ffc-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="84ffc-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84ffc-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="84ffc-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="84ffc-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="84ffc-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="84ffc-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="84ffc-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="84ffc-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="84ffc-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="84ffc-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="84ffc-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="84ffc-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="84ffc-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="84ffc-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="84ffc-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="84ffc-118">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="84ffc-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="84ffc-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="84ffc-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="84ffc-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="84ffc-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="84ffc-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="84ffc-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="84ffc-122">editControl</span><span class="sxs-lookup"><span data-stu-id="84ffc-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="84ffc-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="84ffc-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="84ffc-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="84ffc-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
