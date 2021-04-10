---
description: 專案的使用者易記型別名稱。
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. ItemTypeText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699a953392054cb2344c5f3b3d652e64a9a2c1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192523"
---
# <a name="systemitemtypetext"></a><span data-ttu-id="531a1-103">System. ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="531a1-103">System.ItemTypeText</span></span>

<span data-ttu-id="531a1-104">專案的使用者易記型別名稱。</span><span class="sxs-lookup"><span data-stu-id="531a1-104">The user-friendly type name of the item.</span></span> <span data-ttu-id="531a1-105">此值不能以程式設計方式剖析。</span><span class="sxs-lookup"><span data-stu-id="531a1-105">This value is not intended to be programmatically parsed.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="531a1-106">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="531a1-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="531a1-107">備註</span><span class="sxs-lookup"><span data-stu-id="531a1-107">Remarks</span></span>

<span data-ttu-id="531a1-108">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="531a1-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="531a1-109">如果 [system.object](./props-system-itemtype.md) 是 vt \_ 空白，則這個屬性的值也是 vt \_ 空白。</span><span class="sxs-lookup"><span data-stu-id="531a1-109">If [System.ItemType](./props-system-itemtype.md) is VT\_EMPTY, the value of this property is also VT\_EMPTY.</span></span> <span data-ttu-id="531a1-110">如果專案是檔案，這個屬性的值就會與您將檔案的 system.string 值傳遞給 [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay)時相同。</span><span class="sxs-lookup"><span data-stu-id="531a1-110">If the item is a file, the value of this property is the same as if you passed the file's System.ItemType value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).</span></span>

<span data-ttu-id="531a1-111">這個屬性不應該與 [system.object](./props-system-kind.md)混淆，因為這是高階、使用者易記的種類名稱。</span><span class="sxs-lookup"><span data-stu-id="531a1-111">This property should not be confused with [System.Kind](./props-system-kind.md), which is a high-level, user-friendly kind name.</span></span> <span data-ttu-id="531a1-112">例如，針對 .doc 檔檔，不同的屬性如下所示：</span><span class="sxs-lookup"><span data-stu-id="531a1-112">For example, for a .doc document file, the various properties are as shown here:</span></span>



| <span data-ttu-id="531a1-113">屬性</span><span class="sxs-lookup"><span data-stu-id="531a1-113">Property</span></span>                                               | <span data-ttu-id="531a1-114">值</span><span class="sxs-lookup"><span data-stu-id="531a1-114">Value</span></span>                   |
|--------------------------------------------------------|-------------------------|
| [<span data-ttu-id="531a1-115">System.string</span><span class="sxs-lookup"><span data-stu-id="531a1-115">System.Kind</span></span>](./props-system-kind.md)                 | <span data-ttu-id="531a1-116">文件</span><span class="sxs-lookup"><span data-stu-id="531a1-116">Document</span></span>                |
| [<span data-ttu-id="531a1-117">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="531a1-117">System.ItemType</span></span>](./props-system-itemtype.md)         | <span data-ttu-id="531a1-118">.doc</span><span class="sxs-lookup"><span data-stu-id="531a1-118">.doc</span></span>                    |
| [<span data-ttu-id="531a1-119">System. ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="531a1-119">System.ItemTypeText</span></span>]() | <span data-ttu-id="531a1-120">Microsoft Word 檔</span><span class="sxs-lookup"><span data-stu-id="531a1-120">Microsoft Word Document</span></span> |



 

<span data-ttu-id="531a1-121">範例值：</span><span class="sxs-lookup"><span data-stu-id="531a1-121">Example values:</span></span>



| <span data-ttu-id="531a1-122">路徑</span><span class="sxs-lookup"><span data-stu-id="531a1-122">Path</span></span>                                   | <span data-ttu-id="531a1-123">ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="531a1-123">ItemTypeText</span></span>            |
|----------------------------------------|-------------------------|
| <span data-ttu-id="531a1-124">c： \\ mydir \\ bar \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="531a1-124">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="531a1-125">文字檔</span><span class="sxs-lookup"><span data-stu-id="531a1-125">Text File</span></span>               |
| <span data-ttu-id="531a1-126">\\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="531a1-126">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="531a1-127">Microsoft Word 檔</span><span class="sxs-lookup"><span data-stu-id="531a1-127">Microsoft Word Document</span></span> |
| <span data-ttu-id="531a1-128">\\\\伺服器 \\ 共用 \\ 資料夾</span><span class="sxs-lookup"><span data-stu-id="531a1-128">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="531a1-129">檔案資料夾</span><span class="sxs-lookup"><span data-stu-id="531a1-129">File Folder</span></span>             |
| <span data-ttu-id="531a1-130">c： \\ MyDir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="531a1-130">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="531a1-131">檔案資料夾</span><span class="sxs-lookup"><span data-stu-id="531a1-131">File Folder</span></span>             |
| <span data-ttu-id="531a1-132">/Mailbox 帳戶/收件匣/' Re： Hello！ '</span><span class="sxs-lookup"><span data-stu-id="531a1-132">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="531a1-133">Outlook 電子郵件訊息</span><span class="sxs-lookup"><span data-stu-id="531a1-133">Outlook E-Mail Message</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="531a1-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="531a1-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="531a1-135">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="531a1-135">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="531a1-136">searchInfo</span><span class="sxs-lookup"><span data-stu-id="531a1-136">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="531a1-137">labelInfo</span><span class="sxs-lookup"><span data-stu-id="531a1-137">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="531a1-138">typeInfo</span><span class="sxs-lookup"><span data-stu-id="531a1-138">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="531a1-139">displayInfo</span><span class="sxs-lookup"><span data-stu-id="531a1-139">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="531a1-140">stringFormat</span><span class="sxs-lookup"><span data-stu-id="531a1-140">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="531a1-141">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="531a1-141">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="531a1-142">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="531a1-142">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="531a1-143">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="531a1-143">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="531a1-144">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="531a1-144">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="531a1-145">drawControl</span><span class="sxs-lookup"><span data-stu-id="531a1-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="531a1-146">editControl</span><span class="sxs-lookup"><span data-stu-id="531a1-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="531a1-147">filterControl</span><span class="sxs-lookup"><span data-stu-id="531a1-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="531a1-148">queryControl</span><span class="sxs-lookup"><span data-stu-id="531a1-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
