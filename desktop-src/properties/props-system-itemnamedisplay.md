---
description: '&0034 中的顯示名稱 \# ; 最完整的&\# 0034; 形式。'
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691232"
---
# <a name="systemitemnamedisplay"></a><span data-ttu-id="82b28-103">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="82b28-103">System.ItemNameDisplay</span></span>

<span data-ttu-id="82b28-104">「最完整」表單中的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="82b28-104">The display name in "most complete" form.</span></span> <span data-ttu-id="82b28-105">它是最適合終端使用者的專案名稱唯一標記法。</span><span class="sxs-lookup"><span data-stu-id="82b28-105">It is the unique representation of the item name most appropriate for end users.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="82b28-106">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="82b28-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="82b28-107">備註</span><span class="sxs-lookup"><span data-stu-id="82b28-107">Remarks</span></span>

<span data-ttu-id="82b28-108">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="82b28-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="82b28-109">這個值是[ItemNamePrefix](./props-system-itemnameprefix.md) [和 system.servicemodel 的串連。](./props-system-itemname.md)</span><span class="sxs-lookup"><span data-stu-id="82b28-109">This value is the concatentation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span>

<span data-ttu-id="82b28-110">如果專案是檔案，這個屬性會包含顯示名稱，如檔案總管所示。</span><span class="sxs-lookup"><span data-stu-id="82b28-110">If the item is a file, this property includes the display name as shown in File Explorer.</span></span> <span data-ttu-id="82b28-111">[當指定了 system.string，但](./props-system-filename.md)這個屬性的值完全不同時，會有可接受的情況。</span><span class="sxs-lookup"><span data-stu-id="82b28-111">There are acceptable cases when [System.FileName](./props-system-filename.md) is given but the value of this property is completely different.</span></span> <span data-ttu-id="82b28-112">電子郵件訊息是很好的範例。</span><span class="sxs-lookup"><span data-stu-id="82b28-112">E-mail messages are a good example.</span></span> <span data-ttu-id="82b28-113">如果專案是電子郵件訊息，則專案名稱通常是主旨。</span><span class="sxs-lookup"><span data-stu-id="82b28-113">If the item is an e-mail message, the item name is normally the subject.</span></span> <span data-ttu-id="82b28-114">在此情況下，此值必須是[ItemNamePrefix](./props-system-itemnameprefix.md) [和 system.servicemodel 的串連。](./props-system-itemname.md)</span><span class="sxs-lookup"><span data-stu-id="82b28-114">In that case, the value must be the concatenation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span> <span data-ttu-id="82b28-115">由於 ItemNamePrefix 的值會排除任何尾端空格，因此在產生 [ItemNameDisplay]()時，串連必須包含空格。</span><span class="sxs-lookup"><span data-stu-id="82b28-115">Since the value of System.ItemNamePrefix excludes any trailing spaces, the concatenation must include a space when generating [System.ItemNameDisplay]().</span></span> <span data-ttu-id="82b28-116">請注意，此屬性不一定是唯一的，但其設計目的是要升級最可能是唯一的候選項，而且對終端使用者來說也很合理。</span><span class="sxs-lookup"><span data-stu-id="82b28-116">Note that this property is not guaranteed to be unique, but is designed to promote the most likely candidate that can be unique and also makes sense to end users.</span></span>

<span data-ttu-id="82b28-117">例如， [如果是檔，則可以](./props-system-title.md) 使用 system.string 做為 [ItemNameDisplay]()，但實際上，檔的標題可能不太實用，也無法作為唯一的 ItemNameDisplay。</span><span class="sxs-lookup"><span data-stu-id="82b28-117">For example, for documents, the [System.Title](./props-system-title.md) could be used as the [System.ItemNameDisplay](), but in practice the title of the documents may not be useful or unique enough to function as the sole System.ItemNameDisplay.</span></span> <span data-ttu-id="82b28-118">相反地，提供 [system.object](./props-system-filename.md) 作為 ItemNameDisplay 的值是較佳的選擇。</span><span class="sxs-lookup"><span data-stu-id="82b28-118">Instead, providing [System.FileName](./props-system-filename.md) as the value of System.ItemNameDisplay is a better choice.</span></span> <span data-ttu-id="82b28-119">在 Windows Mail 中，電子郵件會以 .eml 檔案的形式儲存在檔案系統中。</span><span class="sxs-lookup"><span data-stu-id="82b28-119">In Windows Mail, e-mail is stored in the file system as .eml files.</span></span> <span data-ttu-id="82b28-120">這些檔案的檔案名不太方便，因為它們是 Guid。</span><span class="sxs-lookup"><span data-stu-id="82b28-120">The System.FileName values for those files are not human-friendly as they are GUIDs.</span></span> <span data-ttu-id="82b28-121">在此範例中，將 [system.object](./props-system-subject.md) 升階為 ItemNameDisplay，會更有意義。</span><span class="sxs-lookup"><span data-stu-id="82b28-121">In this example, promoting [System.Subject](./props-system-subject.md) as System.ItemNameDisplay makes more sense.</span></span>

<span data-ttu-id="82b28-122">**相容性注意事項：**</span><span class="sxs-lookup"><span data-stu-id="82b28-122">**Compatibility notes:**</span></span>

-   <span data-ttu-id="82b28-123">Windows Vista 上的 Shell 資料夾執行： \_ 當您想要 Windows 檔案總管呼叫 [**IShellFolder：： GETDISPLAYNAMEOF**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) (SHGDN \_ NORMAL) 來取得名稱的值時，請使用 PKEY ItemNameDisplay 做為名稱資料行。</span><span class="sxs-lookup"><span data-stu-id="82b28-123">Shell folder implementations on Windows Vista: use PKEY\_ItemNameDisplay for the name column when you want Windows Explorer to call [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN\_NORMAL) to get the value of the name.</span></span> <span data-ttu-id="82b28-124">\_當您想要 Windows 檔案總管呼叫資料夾的屬性存放區或 [**IShellFolder2：： GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex)來取得名稱的值時，請使用另一個 PKEY，例如 PKEY 的名稱。</span><span class="sxs-lookup"><span data-stu-id="82b28-124">Use another PKEY, such as PKEY\_ItemName, when you want Windows Explorer to call either the folder's property store or [**IShellFolder2::GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) to get the value of the name.</span></span>
-   <span data-ttu-id="82b28-125">Windows XP 上的 Shell 資料夾執行：第一個資料行必須是 [名稱] 資料行，而 Windows 檔案總管會呼叫 [**IShellFolder：： GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) 來取得名稱的值。</span><span class="sxs-lookup"><span data-stu-id="82b28-125">Shell folder implementations on Windows XP: the first column must be the name column, and Windows Explorer calls [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to get the value of the name.</span></span> <span data-ttu-id="82b28-126">PKEY/SCID 並不重要。</span><span class="sxs-lookup"><span data-stu-id="82b28-126">The PKEY/SCID does not matter.</span></span>



| <span data-ttu-id="82b28-127">項目類型</span><span class="sxs-lookup"><span data-stu-id="82b28-127">Item type</span></span>     | <span data-ttu-id="82b28-128">範例</span><span class="sxs-lookup"><span data-stu-id="82b28-128">Example</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="82b28-129">檔案</span><span class="sxs-lookup"><span data-stu-id="82b28-129">File</span></span>          | <span data-ttu-id="82b28-130">hello.txt</span><span class="sxs-lookup"><span data-stu-id="82b28-130">hello.txt</span></span>                 |
| <span data-ttu-id="82b28-131">訊息</span><span class="sxs-lookup"><span data-stu-id="82b28-131">Message</span></span>       | <span data-ttu-id="82b28-132">Re：會議在哪裡？</span><span class="sxs-lookup"><span data-stu-id="82b28-132">Re: Where is the meeting?</span></span> |
| <span data-ttu-id="82b28-133">裝置資料夾</span><span class="sxs-lookup"><span data-stu-id="82b28-133">Device folder</span></span> | <span data-ttu-id="82b28-134">song</span><span class="sxs-lookup"><span data-stu-id="82b28-134">song.wma</span></span>                  |
| <span data-ttu-id="82b28-135">資料夾</span><span class="sxs-lookup"><span data-stu-id="82b28-135">Folder</span></span>        | <span data-ttu-id="82b28-136">文件</span><span class="sxs-lookup"><span data-stu-id="82b28-136">Documents</span></span>                 |



 

## <a name="related-topics"></a><span data-ttu-id="82b28-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="82b28-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82b28-138">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="82b28-138">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="82b28-139">searchInfo</span><span class="sxs-lookup"><span data-stu-id="82b28-139">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="82b28-140">labelInfo</span><span class="sxs-lookup"><span data-stu-id="82b28-140">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="82b28-141">typeInfo</span><span class="sxs-lookup"><span data-stu-id="82b28-141">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="82b28-142">displayInfo</span><span class="sxs-lookup"><span data-stu-id="82b28-142">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="82b28-143">stringFormat</span><span class="sxs-lookup"><span data-stu-id="82b28-143">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="82b28-144">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="82b28-144">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="82b28-145">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="82b28-145">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="82b28-146">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="82b28-146">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="82b28-147">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="82b28-147">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="82b28-148">drawControl</span><span class="sxs-lookup"><span data-stu-id="82b28-148">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="82b28-149">editControl</span><span class="sxs-lookup"><span data-stu-id="82b28-149">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="82b28-150">filterControl</span><span class="sxs-lookup"><span data-stu-id="82b28-150">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="82b28-151">queryControl</span><span class="sxs-lookup"><span data-stu-id="82b28-151">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
