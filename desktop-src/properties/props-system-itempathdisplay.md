---
description: 請閱讀 ItemPathDisplay 屬性，它代表使用者易記的專案顯示路徑。
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ddad0edbc1a77a3de1fab7956d8ce6e6f906f06
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403901"
---
# <a name="systemitempathdisplay"></a><span data-ttu-id="14948-103">System. ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="14948-103">System.ItemPathDisplay</span></span>

<span data-ttu-id="14948-104">專案的使用者易記顯示路徑。</span><span class="sxs-lookup"><span data-stu-id="14948-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="14948-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="14948-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="14948-106">備註</span><span class="sxs-lookup"><span data-stu-id="14948-106">Remarks</span></span>

<span data-ttu-id="14948-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="14948-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="14948-108">如果專案是檔案或資料夾，則這個屬性會在所有情況下都包含副檔名，而且如果有可用的當地語系化名稱，則會當地語系化。</span><span class="sxs-lookup"><span data-stu-id="14948-108">If the item is a file or folder, this property includes the extension in all cases, and is localized if a localized name is available.</span></span> <span data-ttu-id="14948-109">如果是其他專案，這會是相當方便使用的專案，前提是該專案存在於階層式儲存體中。</span><span class="sxs-lookup"><span data-stu-id="14948-109">For other items, this is the user-friendly equivalent, assuming that the item exists in hierarchical storage.</span></span>

<span data-ttu-id="14948-110">不同于 [ItemUrl](./props-system-itemurl.md)，此屬性值不包含 URL 配置。</span><span class="sxs-lookup"><span data-stu-id="14948-110">Unlike [System.ItemUrl](./props-system-itemurl.md), this property value does not include the URL scheme.</span></span> <span data-ttu-id="14948-111">若要剖析專案路徑，請使用 ItemUrl 或 [ParsingPath](./props-system-parsingpath.md)。</span><span class="sxs-lookup"><span data-stu-id="14948-111">To parse an item path, use System.ItemUrl or [System.ParsingPath](./props-system-parsingpath.md).</span></span> <span data-ttu-id="14948-112">若要使用 Shell Api 參考 Shell 命名空間專案，請使用 ParsingPath。</span><span class="sxs-lookup"><span data-stu-id="14948-112">To reference Shell namespace items using Shell APIs, use System.ParsingPath.</span></span>

<span data-ttu-id="14948-113">範例值：</span><span class="sxs-lookup"><span data-stu-id="14948-113">Example values:</span></span>



| <span data-ttu-id="14948-114">路徑</span><span class="sxs-lookup"><span data-stu-id="14948-114">Path</span></span>                                   | <span data-ttu-id="14948-115">ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="14948-115">ItemPathDisplay</span></span>                        |
|----------------------------------------|----------------------------------------|
| <span data-ttu-id="14948-116">c： \\ mydir \\ bar \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="14948-116">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="14948-117">c： \\ mydir \\ bar \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="14948-117">c:\\mydir\\bar\\hello.txt</span></span>              |
| <span data-ttu-id="14948-118">\\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="14948-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="14948-119">\\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="14948-119">\\\\server\\share\\mydir\\goodnews.doc</span></span> |
| <span data-ttu-id="14948-120">\\\\伺服器 \\ 共用 \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="14948-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="14948-121">\\\\伺服器 \\ 共用 \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="14948-121">\\\\server\\share\\numbers.xls</span></span>         |
| <span data-ttu-id="14948-122">c： \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="14948-122">c:\\mydir\\MyFolder</span></span>                    | <span data-ttu-id="14948-123">c： \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="14948-123">c:\\mydir\\MyFolder</span></span>                    |
| <span data-ttu-id="14948-124">/Mailbox 帳戶/收件匣/' Re： Hello！ '</span><span class="sxs-lookup"><span data-stu-id="14948-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="14948-125">/Mailbox 帳戶/收件匣/' Re： Hello！ '</span><span class="sxs-lookup"><span data-stu-id="14948-125">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="14948-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="14948-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14948-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="14948-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="14948-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="14948-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="14948-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="14948-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="14948-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="14948-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="14948-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="14948-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="14948-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="14948-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="14948-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="14948-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="14948-134">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="14948-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="14948-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="14948-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="14948-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="14948-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="14948-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="14948-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="14948-138">editControl</span><span class="sxs-lookup"><span data-stu-id="14948-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="14948-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="14948-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="14948-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="14948-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
