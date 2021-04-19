---
description: 識別以檔案為基礎之專案的副檔名，包括前置句點。
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. FileExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8792a3965c394a1944985515df527e41e3a159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983470"
---
# <a name="systemfileextension"></a><span data-ttu-id="56899-103">System. FileExtension</span><span class="sxs-lookup"><span data-stu-id="56899-103">System.FileExtension</span></span>

<span data-ttu-id="56899-104">識別以檔案為基礎之專案的副檔名，包括前置句點。</span><span class="sxs-lookup"><span data-stu-id="56899-104">Identifies the file extension of the file-based item, including the leading period.</span></span> <span data-ttu-id="56899-105">這個屬性是衍生自 System.object。</span><span class="sxs-lookup"><span data-stu-id="56899-105">This property is derived from System.FileName.</span></span> <span data-ttu-id="56899-106">如果 system.string 沒有副檔名或 VT \_ 空白，則此屬性的值應該是 vt \_ 空白。</span><span class="sxs-lookup"><span data-stu-id="56899-106">If System.FileName either does not have a file extension or is VT\_EMPTY, the value for this property should be VT\_EMPTY.</span></span>

<span data-ttu-id="56899-107">若要取得任何專案的類型 (包括非檔案) 的專案，請使用 system.servicemodel。</span><span class="sxs-lookup"><span data-stu-id="56899-107">To obtain the type of any item (including an item that is not a file), use System.ItemType.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="56899-108">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="56899-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="56899-109">備註</span><span class="sxs-lookup"><span data-stu-id="56899-109">Remarks</span></span>

<span data-ttu-id="56899-110">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="56899-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="56899-111">如果 [system.string](./props-system-filename.md) 是 VT \_ 空白，這個屬性也應該是空的。</span><span class="sxs-lookup"><span data-stu-id="56899-111">If [System.FileName](./props-system-filename.md) is VT\_EMPTY, this property should also be empty.</span></span> <span data-ttu-id="56899-112">否則，這個屬性應該由 system.string 中的資料來源適當地衍生。</span><span class="sxs-lookup"><span data-stu-id="56899-112">Otherwise, this property should be derived appropriately by the data source from System.FileName.</span></span> <span data-ttu-id="56899-113">如果 system.string 不包含副檔名， [FileExtension]() 應該是 VT \_ 空白。</span><span class="sxs-lookup"><span data-stu-id="56899-113">If System.FileName does not include a file extension, [System.FileExtension]() should be VT\_EMPTY.</span></span> <span data-ttu-id="56899-114">若要取得任何專案的類型 (包括非檔案) 的專案，[請使用 system.servicemodel。](./props-system-itemtype.md)</span><span class="sxs-lookup"><span data-stu-id="56899-114">To obtain the type of any item (including an item that is not a file), use [System.ItemType](./props-system-itemtype.md).</span></span>

<span data-ttu-id="56899-115">路徑和副檔名屬性範例。</span><span class="sxs-lookup"><span data-stu-id="56899-115">Path and file extension property examples.</span></span> 

| <span data-ttu-id="56899-116">路徑</span><span class="sxs-lookup"><span data-stu-id="56899-116">Path</span></span>                               | <span data-ttu-id="56899-117">副檔名</span><span class="sxs-lookup"><span data-stu-id="56899-117">File Extension</span></span> |
|------------------------------------|----------------|
| <span data-ttu-id="56899-118">c： \\ files \\ personal \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="56899-118">c:\\files\\personal\\hello.txt</span></span>     | <span data-ttu-id="56899-119">.txt</span><span class="sxs-lookup"><span data-stu-id="56899-119">.txt</span></span>           |
| <span data-ttu-id="56899-120">\\\\伺服器 \\ 共用 \\ mydir \\news.doc</span><span class="sxs-lookup"><span data-stu-id="56899-120">\\\\server\\share\\mydir\\news.doc</span></span> | <span data-ttu-id="56899-121">.doc</span><span class="sxs-lookup"><span data-stu-id="56899-121">.doc</span></span>           |
| <span data-ttu-id="56899-122">\\\\伺服器 \\ 共用 \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="56899-122">\\\\server\\share\\numbers.xls</span></span>     | <span data-ttu-id="56899-123">.xls</span><span class="sxs-lookup"><span data-stu-id="56899-123">.xls</span></span>           |
| <span data-ttu-id="56899-124">\\\\伺服器 \\ 共用 \\ 資料夾</span><span class="sxs-lookup"><span data-stu-id="56899-124">\\\\server\\share\\folder</span></span>          | <span data-ttu-id="56899-125">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="56899-125">VT\_EMPTY</span></span>      |
| <span data-ttu-id="56899-126">c： \\ 東西 \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="56899-126">c:\\Stuff\\MyFolder</span></span>                | <span data-ttu-id="56899-127">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="56899-127">VT\_EMPTY</span></span>      |
| <span data-ttu-id="56899-128">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="56899-128">\[desktop\]</span></span>                        | <span data-ttu-id="56899-129">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="56899-129">VT\_EMPTY</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="56899-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="56899-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56899-131">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="56899-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="56899-132">searchInfo</span><span class="sxs-lookup"><span data-stu-id="56899-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="56899-133">labelInfo</span><span class="sxs-lookup"><span data-stu-id="56899-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="56899-134">typeInfo</span><span class="sxs-lookup"><span data-stu-id="56899-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="56899-135">displayInfo</span><span class="sxs-lookup"><span data-stu-id="56899-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="56899-136">stringFormat</span><span class="sxs-lookup"><span data-stu-id="56899-136">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="56899-137">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="56899-137">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="56899-138">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="56899-138">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="56899-139">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="56899-139">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="56899-140">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="56899-140">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="56899-141">drawControl</span><span class="sxs-lookup"><span data-stu-id="56899-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="56899-142">editControl</span><span class="sxs-lookup"><span data-stu-id="56899-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="56899-143">filterControl</span><span class="sxs-lookup"><span data-stu-id="56899-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="56899-144">queryControl</span><span class="sxs-lookup"><span data-stu-id="56899-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
