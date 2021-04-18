---
description: 由容器專案發出為 TRUE，表示如果容器專案自上次增量索引驗證編目之後未變更，索引子就不需要列舉其子專案。
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: IsClosedDirectory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971558"
---
# <a name="systemsearchiscloseddirectory"></a><span data-ttu-id="5a653-103">IsClosedDirectory</span><span class="sxs-lookup"><span data-stu-id="5a653-103">System.Search.IsClosedDirectory</span></span>

<span data-ttu-id="5a653-104">由容器專案發出為 **TRUE** ，表示如果容器專案自上次增量索引驗證編目之後未變更，索引子就不需要列舉其子專案。</span><span class="sxs-lookup"><span data-stu-id="5a653-104">Emitted as **TRUE** by a container item to indicate that its child items do not need to be enumerated by an indexer if the container item has not changed since the last incremental index verification crawl.</span></span> <span data-ttu-id="5a653-105">這有助於優化索引子效能。</span><span class="sxs-lookup"><span data-stu-id="5a653-105">This contributes to the optimization of indexer performance.</span></span> <span data-ttu-id="5a653-106">在這些容器案例中 (範例是包含附件的電子郵件，或副檔名為 .zip 的壓縮檔) ，子專案會從其父專案分不開。</span><span class="sxs-lookup"><span data-stu-id="5a653-106">In these container cases (examples are an e-mail with attachments or a compressed file with a .zip name extension), child items are inseparable from their parent item.</span></span> <span data-ttu-id="5a653-107">例如，如果包含專案的 [DateModified](./props-system-datemodified.md) 屬性變更，則容器的 DateModified 值會變更為 [符合]。</span><span class="sxs-lookup"><span data-stu-id="5a653-107">For instance, if the [System.DateModified](./props-system-datemodified.md) property of a contained item changes, then the System.DateModified value of the container changes to match.</span></span> <span data-ttu-id="5a653-108">此外，如果刪除父代專案，也會一併刪除所有子專案。</span><span class="sxs-lookup"><span data-stu-id="5a653-108">Also, if a parent item is deleted, all of the child items are deleted as well.</span></span> <span data-ttu-id="5a653-109">因此，如果容器未變更，索引子就會知道其中沒有任何專案已變更，且不需要開啟容器來個別檢查內容。</span><span class="sxs-lookup"><span data-stu-id="5a653-109">Therefore, if the container has not changed, the indexer knows that nothing within it has changed and does not need to open the container to examine the contents individually.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="5a653-110">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="5a653-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="5a653-111">備註</span><span class="sxs-lookup"><span data-stu-id="5a653-111">Remarks</span></span>

<span data-ttu-id="5a653-112">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="5a653-112">PKEY values are defined in Propkey.h.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a653-113">如果專案在這個屬性中發出 **TRUE** ，每個子專案都必須發出 [IsFullyContained](./props-system-search-isfullycontained.md) 屬性為 **true** ，以防止從索引中刪除這些專案。</span><span class="sxs-lookup"><span data-stu-id="5a653-113">If an item emits **TRUE** for this property, each of its child items must emit the [System.Search.IsFullyContained](./props-system-search-isfullycontained.md) property as **TRUE** to prevent those items from being deleted from the index.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5a653-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a653-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a653-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="5a653-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="5a653-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="5a653-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="5a653-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="5a653-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="5a653-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="5a653-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="5a653-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="5a653-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="5a653-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="5a653-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="5a653-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="5a653-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="5a653-122">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="5a653-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="5a653-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5a653-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="5a653-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="5a653-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="5a653-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="5a653-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="5a653-126">editControl</span><span class="sxs-lookup"><span data-stu-id="5a653-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="5a653-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="5a653-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="5a653-128">queryControl</span><span class="sxs-lookup"><span data-stu-id="5a653-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
