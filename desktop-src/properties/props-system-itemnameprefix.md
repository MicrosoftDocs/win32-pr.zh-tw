---
description: 專案的前置詞，用於主體開頭為首碼 &0034; 的電子郵件訊息 \# 。Re： &\# 0034;。
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System. ItemNamePrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf669dd867c8cf60046f226e33dae18f46060cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943626"
---
# <a name="systemitemnameprefix"></a><span data-ttu-id="729a4-103">System. ItemNamePrefix</span><span class="sxs-lookup"><span data-stu-id="729a4-103">System.ItemNamePrefix</span></span>

<span data-ttu-id="729a4-104">專案的前置詞，用於主體開頭為 "Re：" 前置詞的電子郵件訊息。</span><span class="sxs-lookup"><span data-stu-id="729a4-104">The prefix of an item, used for e-mail messages where the subject begins with the prefix "Re:".</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="729a4-105">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="729a4-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="729a4-106">備註</span><span class="sxs-lookup"><span data-stu-id="729a4-106">Remarks</span></span>

<span data-ttu-id="729a4-107">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="729a4-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="729a4-108">如果專案是檔案，則此屬性的值為 VT \_ 空白。</span><span class="sxs-lookup"><span data-stu-id="729a4-108">If the item is a file, then the value of this property is VT\_EMPTY.</span></span> <span data-ttu-id="729a4-109">如果專案是訊息，則這個屬性的值會是轉送或回復首碼 (包括分隔冒號，但不含空白字元) 或 VT 空白（如果沒有 \_ 前置詞）。</span><span class="sxs-lookup"><span data-stu-id="729a4-109">If the item is a message, then the value of this property is the forwarding or reply prefixes (including the delimiting colon, but no whitespace), or VT\_EMPTY if there is no prefix.</span></span>

<span data-ttu-id="729a4-110">範例值：</span><span class="sxs-lookup"><span data-stu-id="729a4-110">Example values:</span></span>



| <span data-ttu-id="729a4-111">System. ItemNamePrefix</span><span class="sxs-lookup"><span data-stu-id="729a4-111">System.ItemNamePrefix</span></span> | <span data-ttu-id="729a4-112">System.servicemodel</span><span class="sxs-lookup"><span data-stu-id="729a4-112">System.ItemName</span></span>  | <span data-ttu-id="729a4-113">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="729a4-113">System.ItemNameDisplay</span></span> |
|-----------------------|------------------|------------------------|
| <span data-ttu-id="729a4-114">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="729a4-114">VT\_EMPTY</span></span>             | <span data-ttu-id="729a4-115">「美好日」</span><span class="sxs-lookup"><span data-stu-id="729a4-115">"Great day"</span></span>      | <span data-ttu-id="729a4-116">「美好日」</span><span class="sxs-lookup"><span data-stu-id="729a4-116">"Great day"</span></span>            |
| <span data-ttu-id="729a4-117">"Re："</span><span class="sxs-lookup"><span data-stu-id="729a4-117">"Re:"</span></span>                 | <span data-ttu-id="729a4-118">「美好日」</span><span class="sxs-lookup"><span data-stu-id="729a4-118">"Great day"</span></span>      | <span data-ttu-id="729a4-119">「Re：很棒的一天」</span><span class="sxs-lookup"><span data-stu-id="729a4-119">"Re: Great day"</span></span>        |
| <span data-ttu-id="729a4-120">"Fwd："</span><span class="sxs-lookup"><span data-stu-id="729a4-120">"Fwd: "</span></span>               | <span data-ttu-id="729a4-121">「每月預算」</span><span class="sxs-lookup"><span data-stu-id="729a4-121">"Monthly budget"</span></span> | <span data-ttu-id="729a4-122">"Fwd：每月預算"</span><span class="sxs-lookup"><span data-stu-id="729a4-122">"Fwd: Monthly budget"</span></span>  |
| <span data-ttu-id="729a4-123">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="729a4-123">VT\_EMPTY</span></span>             | <span data-ttu-id="729a4-124">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="729a4-124">accounts.xls</span></span>     | <span data-ttu-id="729a4-125">accounts.xls</span><span class="sxs-lookup"><span data-stu-id="729a4-125">accounts.xls</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="729a4-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="729a4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="729a4-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="729a4-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="729a4-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="729a4-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="729a4-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="729a4-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="729a4-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="729a4-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="729a4-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="729a4-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="729a4-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="729a4-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="729a4-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="729a4-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="729a4-134">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="729a4-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="729a4-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="729a4-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="729a4-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="729a4-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="729a4-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="729a4-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="729a4-138">editControl</span><span class="sxs-lookup"><span data-stu-id="729a4-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="729a4-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="729a4-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="729a4-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="729a4-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
