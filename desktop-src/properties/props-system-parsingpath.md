---
description: 專案的 Shell 命名空間路徑。
ms.assetid: e0fb2092-0427-40c9-9e09-aefc5ef017e6
title: System. ParsingPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae62243ff37464617f87654f8ca1f04c3ea606da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849040"
---
# <a name="systemparsingpath"></a><span data-ttu-id="a94e7-103">System. ParsingPath</span><span class="sxs-lookup"><span data-stu-id="a94e7-103">System.ParsingPath</span></span>

<span data-ttu-id="a94e7-104">專案的 Shell 命名空間路徑。</span><span class="sxs-lookup"><span data-stu-id="a94e7-104">The Shell namespace path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="a94e7-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="a94e7-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ParsingPath
   shellPKey = PKEY_ParsingPath
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 30
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="a94e7-106">備註</span><span class="sxs-lookup"><span data-stu-id="a94e7-106">Remarks</span></span>

<span data-ttu-id="a94e7-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="a94e7-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="a94e7-108">這個值可以傳遞給 [**SHParseDisplayName**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) ，以剖析正確 Shell 資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="a94e7-108">This value can be passed to [**SHParseDisplayName**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) to parse the path to the correct Shell folder.</span></span> <span data-ttu-id="a94e7-109">如果專案是檔案，則值與 [ItemPathDisplay](./props-system-itempathdisplay.md)相同。</span><span class="sxs-lookup"><span data-stu-id="a94e7-109">If the item is a file, the value is identical to [System.ItemPathDisplay](./props-system-itempathdisplay.md).</span></span> <span data-ttu-id="a94e7-110">如果無法透過 Shell 命名空間存取專案，此值會是 VT \_ 空白。</span><span class="sxs-lookup"><span data-stu-id="a94e7-110">If the item cannot be accessed through the Shell namespace, this value is VT\_EMPTY.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a94e7-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="a94e7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a94e7-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="a94e7-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a94e7-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="a94e7-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a94e7-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="a94e7-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a94e7-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="a94e7-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a94e7-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a94e7-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a94e7-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="a94e7-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a94e7-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="a94e7-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a94e7-119">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="a94e7-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a94e7-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a94e7-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a94e7-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="a94e7-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a94e7-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="a94e7-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a94e7-123">editControl</span><span class="sxs-lookup"><span data-stu-id="a94e7-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a94e7-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="a94e7-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a94e7-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="a94e7-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
