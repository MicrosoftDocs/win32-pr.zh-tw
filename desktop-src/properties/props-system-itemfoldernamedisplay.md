---
description: 專案之父資料夾的使用者易記顯示名稱。
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. ItemFolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d637412b02345b52fee2e1c13e8f499314af4c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193740"
---
# <a name="systemitemfoldernamedisplay"></a><span data-ttu-id="97d55-103">System. ItemFolderNameDisplay</span><span class="sxs-lookup"><span data-stu-id="97d55-103">System.ItemFolderNameDisplay</span></span>

<span data-ttu-id="97d55-104">專案之父資料夾的使用者易記顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="97d55-104">The user-friendly display name of an item's parent folder.</span></span>

<span data-ttu-id="97d55-105">這是衍生自 [ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md)。</span><span class="sxs-lookup"><span data-stu-id="97d55-105">This is derived from [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md).</span></span> <span data-ttu-id="97d55-106">如果該屬性為 VT \_ 空白，則此屬性應該也是。</span><span class="sxs-lookup"><span data-stu-id="97d55-106">If that property is VT\_EMPTY, then this property should be too.</span></span>

<span data-ttu-id="97d55-107">如果資料夾是檔案資料夾，則如果有可用的當地語系化名稱，此值就會當地語系化。</span><span class="sxs-lookup"><span data-stu-id="97d55-107">If the folder is a file folder, the value will be localized if a localized name is available.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="97d55-108">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="97d55-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="97d55-109">備註</span><span class="sxs-lookup"><span data-stu-id="97d55-109">Remarks</span></span>

<span data-ttu-id="97d55-110">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="97d55-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="97d55-111">如果 [ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) 是 VT \_ 空白，則此屬性也應為空白。</span><span class="sxs-lookup"><span data-stu-id="97d55-111">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="97d55-112">否則，應該由 ItemFolderPathDisplay 中的資料來源適當地衍生。</span><span class="sxs-lookup"><span data-stu-id="97d55-112">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

<span data-ttu-id="97d55-113">範例：</span><span class="sxs-lookup"><span data-stu-id="97d55-113">Examples:</span></span>



| <span data-ttu-id="97d55-114">指定的路徑</span><span class="sxs-lookup"><span data-stu-id="97d55-114">Given path</span></span>                             | <span data-ttu-id="97d55-115">資料夾顯示名稱</span><span class="sxs-lookup"><span data-stu-id="97d55-115">Folder Display Name</span></span> |
|----------------------------------------|---------------------|
| <span data-ttu-id="97d55-116">c： \\ MyFiles \\ 文字 \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="97d55-116">c:\\MyFiles\\Text\\hello.txt</span></span>           | <span data-ttu-id="97d55-117">Text</span><span class="sxs-lookup"><span data-stu-id="97d55-117">Text</span></span>                |
| <span data-ttu-id="97d55-118">\\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="97d55-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="97d55-119">mydir</span><span class="sxs-lookup"><span data-stu-id="97d55-119">mydir</span></span>               |
| <span data-ttu-id="97d55-120">\\\\伺服器 \\ 共用 \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="97d55-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="97d55-121">分享</span><span class="sxs-lookup"><span data-stu-id="97d55-121">share</span></span>               |
| <span data-ttu-id="97d55-122">c： \\ 資料夾 \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="97d55-122">c:\\Folders\\MyFolder</span></span>                  | <span data-ttu-id="97d55-123">資料夾</span><span class="sxs-lookup"><span data-stu-id="97d55-123">Folders</span></span>             |
| <span data-ttu-id="97d55-124">/Mailbox 帳戶/收件匣/' Re： Hello！ '</span><span class="sxs-lookup"><span data-stu-id="97d55-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="97d55-125">Inbox</span><span class="sxs-lookup"><span data-stu-id="97d55-125">Inbox</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="97d55-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="97d55-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97d55-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="97d55-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="97d55-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="97d55-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="97d55-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="97d55-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="97d55-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="97d55-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="97d55-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="97d55-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="97d55-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="97d55-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="97d55-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="97d55-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="97d55-134">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="97d55-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="97d55-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="97d55-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="97d55-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="97d55-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="97d55-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="97d55-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="97d55-138">editControl</span><span class="sxs-lookup"><span data-stu-id="97d55-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="97d55-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="97d55-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="97d55-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="97d55-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
