---
description: 專案的使用者易記顯示路徑。
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef7b9d03a78a23e955c20f52e32062a8bcabd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194264"
---
# <a name="systemitempathdisplaynarrow"></a><span data-ttu-id="7e41f-103">System. ItemPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="7e41f-103">System.ItemPathDisplayNarrow</span></span>

<span data-ttu-id="7e41f-104">專案的使用者易記顯示路徑。</span><span class="sxs-lookup"><span data-stu-id="7e41f-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="7e41f-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="7e41f-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="7e41f-106">備註</span><span class="sxs-lookup"><span data-stu-id="7e41f-106">Remarks</span></span>

<span data-ttu-id="7e41f-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="7e41f-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="7e41f-108">若要針對窄的視圖資料行進行優化，必須量身打造字串的格式，以便先取得名稱。</span><span class="sxs-lookup"><span data-stu-id="7e41f-108">To optimize for a narrow viewing column, the format of the string should be tailored so that the name comes first.</span></span>

<span data-ttu-id="7e41f-109">如果專案是檔案，則屬性值會排除副檔名，但會包含當地語系化名稱（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="7e41f-109">If the item is a file, the property value excludes the file extension, but includes localized names if they are present.</span></span> <span data-ttu-id="7e41f-110">如果專案是訊息，此值會包含 [ItemNamePrefix](./props-system-itemnameprefix.md)。</span><span class="sxs-lookup"><span data-stu-id="7e41f-110">If the item is a message, the value includes the [System.ItemNamePrefix](./props-system-itemnameprefix.md).</span></span> <span data-ttu-id="7e41f-111">若要剖析專案路徑，請使用 [ItemUrl](./props-system-itemurl.md) 或 [ParsingPath](./props-system-parsingpath.md)。</span><span class="sxs-lookup"><span data-stu-id="7e41f-111">To parse an item path, use [System.ItemUrl](./props-system-itemurl.md) or [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="7e41f-112">範例值：</span><span class="sxs-lookup"><span data-stu-id="7e41f-112">Example values:</span></span>



| <span data-ttu-id="7e41f-113">路徑</span><span class="sxs-lookup"><span data-stu-id="7e41f-113">Path</span></span>                                   | <span data-ttu-id="7e41f-114">ItemPathDisplayName</span><span class="sxs-lookup"><span data-stu-id="7e41f-114">ItemPathDisplayName</span></span>                 |
|----------------------------------------|-------------------------------------|
| <span data-ttu-id="7e41f-115">c： \\ mydir \\ bar \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="7e41f-115">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="7e41f-116">hello (c： \\ mydir \\ bar) </span><span class="sxs-lookup"><span data-stu-id="7e41f-116">hello (c:\\mydir\\bar)</span></span>              |
| <span data-ttu-id="7e41f-117">\\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="7e41f-117">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="7e41f-118">goodnews (\\ \\ server \\ share \\ mydir) </span><span class="sxs-lookup"><span data-stu-id="7e41f-118">goodnews (\\\\server\\share\\mydir)</span></span> |
| <span data-ttu-id="7e41f-119">\\\\伺服器 \\ 共用 \\ 資料夾</span><span class="sxs-lookup"><span data-stu-id="7e41f-119">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="7e41f-120"> (\\ \\ server \\ 共用) 資料夾</span><span class="sxs-lookup"><span data-stu-id="7e41f-120">folder (\\\\server\\share)</span></span>          |
| <span data-ttu-id="7e41f-121">c： \\ MyDir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="7e41f-121">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="7e41f-122">MyFolder (c： \\ mydir) </span><span class="sxs-lookup"><span data-stu-id="7e41f-122">MyFolder (c:\\mydir)</span></span>                |
| <span data-ttu-id="7e41f-123">/Mailbox 帳戶/收件匣/' Re： Hello！ '</span><span class="sxs-lookup"><span data-stu-id="7e41f-123">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="7e41f-124">Re：您好！</span><span class="sxs-lookup"><span data-stu-id="7e41f-124">Re: Hello!</span></span> <span data-ttu-id="7e41f-125"> (/Mailbox 帳戶/收件匣) </span><span class="sxs-lookup"><span data-stu-id="7e41f-125">(/Mailbox Account/Inbox)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7e41f-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e41f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e41f-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="7e41f-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="7e41f-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="7e41f-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="7e41f-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="7e41f-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="7e41f-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="7e41f-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="7e41f-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="7e41f-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="7e41f-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="7e41f-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="7e41f-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="7e41f-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="7e41f-134">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="7e41f-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="7e41f-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="7e41f-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="7e41f-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="7e41f-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="7e41f-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="7e41f-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="7e41f-138">editControl</span><span class="sxs-lookup"><span data-stu-id="7e41f-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="7e41f-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="7e41f-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="7e41f-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="7e41f-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
