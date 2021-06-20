---
description: 閱讀 ItemFolderPathDisplay 屬性，其代表專案之父資料夾的使用者易記顯示路徑。
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System. ItemFolderPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12909b29790ea2c016154cea9fccf7c53e45630
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403931"
---
# <a name="systemitemfolderpathdisplay"></a><span data-ttu-id="e192b-103">System. ItemFolderPathDisplay</span><span class="sxs-lookup"><span data-stu-id="e192b-103">System.ItemFolderPathDisplay</span></span>

<span data-ttu-id="e192b-104">專案之父資料夾的使用者易記顯示路徑。</span><span class="sxs-lookup"><span data-stu-id="e192b-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="e192b-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="e192b-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="e192b-106">備註</span><span class="sxs-lookup"><span data-stu-id="e192b-106">Remarks</span></span>

<span data-ttu-id="e192b-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="e192b-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="e192b-108">如果 [ItemPathDisplay](./props-system-itempathdisplay.md) 是 VT \_ 空白，則此屬性也應為空白。</span><span class="sxs-lookup"><span data-stu-id="e192b-108">If [System.ItemPathDisplay](./props-system-itempathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="e192b-109">否則，應該由 ItemPathDisplay 中的資料來源適當地衍生。</span><span class="sxs-lookup"><span data-stu-id="e192b-109">Otherwise, it should be derived appropriately by the data source from System.ItemPathDisplay.</span></span>

<span data-ttu-id="e192b-110">範例值：</span><span class="sxs-lookup"><span data-stu-id="e192b-110">Example values:</span></span>



| <span data-ttu-id="e192b-111">路徑</span><span class="sxs-lookup"><span data-stu-id="e192b-111">Path</span></span>                                   | <span data-ttu-id="e192b-112">ItemFolderPathDisplay</span><span class="sxs-lookup"><span data-stu-id="e192b-112">ItemFolderPathDisplay</span></span>    |
|----------------------------------------|--------------------------|
| <span data-ttu-id="e192b-113">c： \\ files \\ personal \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="e192b-113">c:\\files\\personal\\hello.txt</span></span>         | <span data-ttu-id="e192b-114">c： \\ \\ 個人檔案</span><span class="sxs-lookup"><span data-stu-id="e192b-114">c:\\files\\personal</span></span>      |
| <span data-ttu-id="e192b-115">\\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="e192b-115">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="e192b-116">\\\\伺服器 \\ 共用 \\ mydir</span><span class="sxs-lookup"><span data-stu-id="e192b-116">\\\\server\\share\\mydir</span></span> |
| <span data-ttu-id="e192b-117">\\\\伺服器 \\ 共用 \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="e192b-117">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="e192b-118">\\\\伺服器 \\ 共用</span><span class="sxs-lookup"><span data-stu-id="e192b-118">\\\\server\\share</span></span>        |
| <span data-ttu-id="e192b-119">c： \\ 食物 \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="e192b-119">c:\\food\\MyFolder</span></span>                     | <span data-ttu-id="e192b-120">c： \\ 食物</span><span class="sxs-lookup"><span data-stu-id="e192b-120">c:\\food</span></span>                 |
| <span data-ttu-id="e192b-121">/Mailbox 帳戶/收件匣/' Re： Hello！ '</span><span class="sxs-lookup"><span data-stu-id="e192b-121">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="e192b-122">/Mailbox 帳戶/收件匣</span><span class="sxs-lookup"><span data-stu-id="e192b-122">/Mailbox Account/Inbox</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="e192b-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="e192b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e192b-124">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e192b-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e192b-125">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e192b-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e192b-126">labelInfo</span><span class="sxs-lookup"><span data-stu-id="e192b-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e192b-127">typeInfo</span><span class="sxs-lookup"><span data-stu-id="e192b-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e192b-128">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e192b-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e192b-129">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e192b-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e192b-130">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="e192b-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e192b-131">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="e192b-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e192b-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e192b-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e192b-133">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="e192b-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e192b-134">drawControl</span><span class="sxs-lookup"><span data-stu-id="e192b-134">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e192b-135">editControl</span><span class="sxs-lookup"><span data-stu-id="e192b-135">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e192b-136">filterControl</span><span class="sxs-lookup"><span data-stu-id="e192b-136">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e192b-137">queryControl</span><span class="sxs-lookup"><span data-stu-id="e192b-137">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
