---
description: 專案的標準型別。
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System.servicemodel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0159a12e1cc3c6d85e461461cad20334a641fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194820"
---
# <a name="systemitemtype"></a><span data-ttu-id="dae47-103">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="dae47-103">System.ItemType</span></span>

<span data-ttu-id="dae47-104">專案的標準型別。</span><span class="sxs-lookup"><span data-stu-id="dae47-104">The canonical type of the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="dae47-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="dae47-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="dae47-106">備註</span><span class="sxs-lookup"><span data-stu-id="dae47-106">Remarks</span></span>

<span data-ttu-id="dae47-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="dae47-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="dae47-108">System.servicemodel 的值是要以程式設計方式剖析，而且可以是：</span><span class="sxs-lookup"><span data-stu-id="dae47-108">The value for System.ItemType is intended to be programmatically parsed, and can be either:</span></span>

-   <span data-ttu-id="dae47-109">指向 ProgID 值的副檔名， (HKEY \_ 類別 \_ 根 \\ <ProgID>) 保留類型的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="dae47-109">A file extension that points to a ProgID value (HKEY\_CLASSES\_ROOT\\<ProgID>) holding the display name for the type.</span></span>
-   <span data-ttu-id="dae47-110">ProgID 值 (HKEY \_ 類別 \_ RROOT \\ <ProgID>) ，其中包含類型的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="dae47-110">A ProgID value (HKEY\_CLASSES\_RROOT\\<ProgID>), containing the display name for the type.</span></span>

<span data-ttu-id="dae47-111">ProgID 的 FriendlyTypeName 元素應為應用程式名稱的當地語系化版本 (@winword.dll 、-42) ，而 progid 索引鍵的預設值為非當地語系化的名稱 (Word.Doc>ument. 12) 。</span><span class="sxs-lookup"><span data-stu-id="dae47-111">The FriendlyTypeName element of a ProgID should be a localized version of the application name (@winword.dll,-42), while the default value of the ProgID key is a non-localized name (Word.Document.12).</span></span>

<span data-ttu-id="dae47-112">如果沒有標準型別，則此值為 VT \_ 空白。</span><span class="sxs-lookup"><span data-stu-id="dae47-112">If there is no canonical type, the value is VT\_EMPTY.</span></span> <span data-ttu-id="dae47-113">如果專案是檔案 ([系統檔案名](./props-system-filename.md) 不是 VT \_ 空白) ，則值與 [FileExtension](./props-system-fileextension.md)相同。</span><span class="sxs-lookup"><span data-stu-id="dae47-113">If the item is a file ([System.FileName](./props-system-filename.md) is not VT\_EMPTY), the value is the same as [System.FileExtension](./props-system-fileextension.md).</span></span> <span data-ttu-id="dae47-114">當您想要在視圖中顯示類型給終端使用者時，請使用 [ItemTypeText](./props-system-itemtypetext.md) 。</span><span class="sxs-lookup"><span data-stu-id="dae47-114">Use [System.ItemTypeText](./props-system-itemtypetext.md) when you want to display the type to end users in a view.</span></span>

> [!Note]  
> <span data-ttu-id="dae47-115">如果專案是檔案，則傳遞 [system.string 值給]() [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) 會產生與 [ItemTypeText](./props-system-itemtypetext.md)相同的值。</span><span class="sxs-lookup"><span data-stu-id="dae47-115">If the item is a file, passing the [System.ItemType]() value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) results in the same value as [System.ItemTypeText](./props-system-itemtypetext.md).</span></span>

 

<span data-ttu-id="dae47-116">範例值：</span><span class="sxs-lookup"><span data-stu-id="dae47-116">Example values:</span></span>



| <span data-ttu-id="dae47-117">路徑</span><span class="sxs-lookup"><span data-stu-id="dae47-117">Path</span></span>                                   | <span data-ttu-id="dae47-118">ItemType</span><span class="sxs-lookup"><span data-stu-id="dae47-118">ItemType</span></span>         |
|----------------------------------------|------------------|
| <span data-ttu-id="dae47-119">c： \\ mydir \\ bar \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="dae47-119">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="dae47-120">.txt</span><span class="sxs-lookup"><span data-stu-id="dae47-120">.txt</span></span>             |
| <span data-ttu-id="dae47-121">\\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="dae47-121">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="dae47-122">.doc</span><span class="sxs-lookup"><span data-stu-id="dae47-122">.doc</span></span>             |
| <span data-ttu-id="dae47-123">\\\\伺服器 \\ 共用 \\ 資料夾</span><span class="sxs-lookup"><span data-stu-id="dae47-123">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="dae47-124">目錄</span><span class="sxs-lookup"><span data-stu-id="dae47-124">Directory</span></span>        |
| <span data-ttu-id="dae47-125">c： \\ MyDir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="dae47-125">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="dae47-126">目錄</span><span class="sxs-lookup"><span data-stu-id="dae47-126">Directory</span></span>        |
| <span data-ttu-id="dae47-127">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="dae47-127">\[desktop\]</span></span>                            | <span data-ttu-id="dae47-128">資料夾</span><span class="sxs-lookup"><span data-stu-id="dae47-128">Folder</span></span>           |
| <span data-ttu-id="dae47-129">/Mailbox 帳戶/收件匣/' Re： Hello！ '</span><span class="sxs-lookup"><span data-stu-id="dae47-129">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="dae47-130">MAPI/IPM。消息</span><span class="sxs-lookup"><span data-stu-id="dae47-130">MAPI/IPM.Message</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="dae47-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="dae47-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dae47-132">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="dae47-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="dae47-133">searchInfo</span><span class="sxs-lookup"><span data-stu-id="dae47-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="dae47-134">labelInfo</span><span class="sxs-lookup"><span data-stu-id="dae47-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="dae47-135">typeInfo</span><span class="sxs-lookup"><span data-stu-id="dae47-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="dae47-136">displayInfo</span><span class="sxs-lookup"><span data-stu-id="dae47-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="dae47-137">stringFormat</span><span class="sxs-lookup"><span data-stu-id="dae47-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="dae47-138">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="dae47-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="dae47-139">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="dae47-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="dae47-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="dae47-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="dae47-141">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="dae47-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="dae47-142">drawControl</span><span class="sxs-lookup"><span data-stu-id="dae47-142">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="dae47-143">editControl</span><span class="sxs-lookup"><span data-stu-id="dae47-143">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="dae47-144">filterControl</span><span class="sxs-lookup"><span data-stu-id="dae47-144">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="dae47-145">queryControl</span><span class="sxs-lookup"><span data-stu-id="dae47-145">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="dae47-146">程式設計識別碼</span><span class="sxs-lookup"><span data-stu-id="dae47-146">Programmatic Identifiers</span></span>](../shell/fa-progids.md)
</dt> </dl>

 

 
