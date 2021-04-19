---
description: 檔案名，包括副檔名。
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System.string
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f535eff4625178b3c32a04ea6d325505266a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991856"
---
# <a name="systemfilename"></a><span data-ttu-id="9b0d4-103">System.string</span><span class="sxs-lookup"><span data-stu-id="9b0d4-103">System.FileName</span></span>

<span data-ttu-id="9b0d4-104">檔案名，包括副檔名。</span><span class="sxs-lookup"><span data-stu-id="9b0d4-104">The file name, including its extension.</span></span> <span data-ttu-id="9b0d4-105">FileExtension 衍生自這個屬性。</span><span class="sxs-lookup"><span data-stu-id="9b0d4-105">System.FileExtension is derived from this property.</span></span>

<span data-ttu-id="9b0d4-106">專案可能不存在於檔案系統上 (也可能無法使用 CreateFile) 開啟。</span><span class="sxs-lookup"><span data-stu-id="9b0d4-106">It is possible that the item might not exist on a filesystem (that is, it may not be opened using CreateFile).</span></span> <span data-ttu-id="9b0d4-107">但是，如果專案是以檔案表示，且其名稱遵循標準 Win32 檔案命名語法，則資料來源應該發出這個屬性。</span><span class="sxs-lookup"><span data-stu-id="9b0d4-107">Nonetheless, if the item is represented as a file and its name follows standard Win32 file-naming syntax, then the data source should emit this property.</span></span> <span data-ttu-id="9b0d4-108">如果專案不是檔案，則資料來源應該將此屬性發出為 VT \_ 空白。</span><span class="sxs-lookup"><span data-stu-id="9b0d4-108">If the item is not a file, then the data source should emit this property as VT\_EMPTY.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="9b0d4-109">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="9b0d4-109">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="9b0d4-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b0d4-110">Windows Vista</span></span>

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0-9
         enumRange
            minValue = A
            setValue = A
            text = A-H
         enumRange
            minValue = I
            setValue = I
            text = I-P
         enumRange
            minValue = Q
            setValue = Q
            text = Q-Z
```

## <a name="remarks"></a><span data-ttu-id="9b0d4-111">備註</span><span class="sxs-lookup"><span data-stu-id="9b0d4-111">Remarks</span></span>

<span data-ttu-id="9b0d4-112">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="9b0d4-112">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="9b0d4-113">專案可能不存在於檔案系統上 (也就是說，它可能不會使用 CreateFile) 開啟，但如果專案是以邏輯意義的檔案表示，而且其名稱遵循標準 Win32 檔案命名語法，則資料來源應該發出這個屬性。</span><span class="sxs-lookup"><span data-stu-id="9b0d4-113">The item might not exist on a filesystem (that is, it may not be opened using CreateFile), but if the item is represented as a file from the logical sense and its name follows standard Win32 file-naming syntax, then the data source should emit this property.</span></span> <span data-ttu-id="9b0d4-114">如果專案不是檔案，則此屬性的值為 VT \_ 空白。</span><span class="sxs-lookup"><span data-stu-id="9b0d4-114">If an item is not a file, then the value for this property is VT\_EMPTY.</span></span> <span data-ttu-id="9b0d4-115">請參閱 ItemNameDisplay。</span><span class="sxs-lookup"><span data-stu-id="9b0d4-115">See System.ItemNameDisplay.</span></span> <span data-ttu-id="9b0d4-116">針對 Shell 的檔案資料夾所提供的專案，其值與 ParsingName 相同。</span><span class="sxs-lookup"><span data-stu-id="9b0d4-116">This has the same value as System.ParsingName for items that are provided by the Shell's file folder.</span></span>

<span data-ttu-id="9b0d4-117">下表列出 [路徑] 和 [檔案名] 屬性值的範例：</span><span class="sxs-lookup"><span data-stu-id="9b0d4-117">The following table lists examples of path and filename property values:</span></span>



| <span data-ttu-id="9b0d4-118">路徑</span><span class="sxs-lookup"><span data-stu-id="9b0d4-118">Path</span></span>                               | <span data-ttu-id="9b0d4-119">屬性值</span><span class="sxs-lookup"><span data-stu-id="9b0d4-119">Property Value</span></span> |
|------------------------------------|----------------|
| <span data-ttu-id="9b0d4-120">c： \\ files \\ personal \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="9b0d4-120">c:\\files\\personal\\hello.txt</span></span>     | <span data-ttu-id="9b0d4-121">hello.txt</span><span class="sxs-lookup"><span data-stu-id="9b0d4-121">hello.txt</span></span>      |
| <span data-ttu-id="9b0d4-122">\\\\伺服器 \\ 共用 \\ mydir \\news.doc</span><span class="sxs-lookup"><span data-stu-id="9b0d4-122">\\\\server\\share\\mydir\\news.doc</span></span> | <span data-ttu-id="9b0d4-123">news.doc</span><span class="sxs-lookup"><span data-stu-id="9b0d4-123">news.doc</span></span>       |
| <span data-ttu-id="9b0d4-124">\\\\伺服器 \\ 共用 \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="9b0d4-124">\\\\server\\share\\numbers.xls</span></span>     | <span data-ttu-id="9b0d4-125">numbers.xls</span><span class="sxs-lookup"><span data-stu-id="9b0d4-125">numbers.xls</span></span>    |
| <span data-ttu-id="9b0d4-126">c： \\ 東西 \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="9b0d4-126">c:\\Stuff\\MyFolder</span></span>                | <span data-ttu-id="9b0d4-127">MyFolder</span><span class="sxs-lookup"><span data-stu-id="9b0d4-127">MyFolder</span></span>       |
| <span data-ttu-id="9b0d4-128">\[電子郵件訊息\]</span><span class="sxs-lookup"><span data-stu-id="9b0d4-128">\[email message\]</span></span>                  | <span data-ttu-id="9b0d4-129">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="9b0d4-129">VT\_EMPTY</span></span>      |
| <span data-ttu-id="9b0d4-130">\[song. 可攜式裝置上的 wma\]</span><span class="sxs-lookup"><span data-stu-id="9b0d4-130">\[song.wma on portable device\]</span></span>    | <span data-ttu-id="9b0d4-131">song</span><span class="sxs-lookup"><span data-stu-id="9b0d4-131">song.wma</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="9b0d4-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b0d4-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b0d4-133">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="9b0d4-133">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="9b0d4-134">searchInfo</span><span class="sxs-lookup"><span data-stu-id="9b0d4-134">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="9b0d4-135">labelInfo</span><span class="sxs-lookup"><span data-stu-id="9b0d4-135">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="9b0d4-136">typeInfo</span><span class="sxs-lookup"><span data-stu-id="9b0d4-136">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="9b0d4-137">displayInfo</span><span class="sxs-lookup"><span data-stu-id="9b0d4-137">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="9b0d4-138">stringFormat</span><span class="sxs-lookup"><span data-stu-id="9b0d4-138">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="9b0d4-139">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="9b0d4-139">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="9b0d4-140">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="9b0d4-140">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="9b0d4-141">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="9b0d4-141">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="9b0d4-142">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="9b0d4-142">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="9b0d4-143">drawControl</span><span class="sxs-lookup"><span data-stu-id="9b0d4-143">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="9b0d4-144">editControl</span><span class="sxs-lookup"><span data-stu-id="9b0d4-144">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="9b0d4-145">filterControl</span><span class="sxs-lookup"><span data-stu-id="9b0d4-145">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="9b0d4-146">queryControl</span><span class="sxs-lookup"><span data-stu-id="9b0d4-146">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
