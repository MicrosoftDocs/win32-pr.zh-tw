---
description: 這個屬性與 UrlToIndex 相同，不同之處在于它包含上次修改 URL 的時間。
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fcc83b9796ae2375f10235a08ba0db313fb1958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975866"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a><span data-ttu-id="227cc-103">UrlToIndexWithModificationTime</span><span class="sxs-lookup"><span data-stu-id="227cc-103">System.Search.UrlToIndexWithModificationTime</span></span>

<span data-ttu-id="227cc-104">這個屬性與 [**UrlToIndex**](props-system-search-urltoindex.md) 相同，不同之處在于它包含上次修改 URL 的時間。</span><span class="sxs-lookup"><span data-stu-id="227cc-104">This property is the same as [**System.Search.UrlToIndex**](props-system-search-urltoindex.md) except that it includes the time that the URL was last modified.</span></span> <span data-ttu-id="227cc-105">這是索引子的優化，因此不需要回呼至通訊協定處理常式來要求這項資訊，以判斷是否需要重新編制內容的索引。</span><span class="sxs-lookup"><span data-stu-id="227cc-105">This is an optimization for the indexer so that it does not have to call back into the protocol handler to ask for this information to determine whether the content needs to be indexed again.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="227cc-106">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="227cc-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a><span data-ttu-id="227cc-107">備註</span><span class="sxs-lookup"><span data-stu-id="227cc-107">Remarks</span></span>

<span data-ttu-id="227cc-108">此 [UrlToIndexWithModificationTime]() 屬性與 [UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) 屬性相同，不同之處在于您也會傳入檔的上次修改時間。</span><span class="sxs-lookup"><span data-stu-id="227cc-108">This [System.Search.UrlToIndexWithModificationTime]() property is the same as the [System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) property, except that you also pass in the last modified time of the document.</span></span> <span data-ttu-id="227cc-109">如果上次修改時間相符，則索引子會假設檔已編制索引，並擲回通知。</span><span class="sxs-lookup"><span data-stu-id="227cc-109">If the last modified time matches, the indexer assumes that the document is already indexed and throws away the notification.</span></span> <span data-ttu-id="227cc-110">這個屬性是具有兩個元素的向量，包含 URL 的 **vt \_ LPWSTR** 值，以及包含上次修改時間的 **vt \_ FILETIME** 值。</span><span class="sxs-lookup"><span data-stu-id="227cc-110">This property is a vector with two elements, a **VT\_LPWSTR** value that contains the URL and a **VT\_FILETIME** value that contains the last modified time.</span></span>

<span data-ttu-id="227cc-111">[UrlToIndexWithModificationTime]() \_ \_ \_ \_ 在舊版 WINDOWS 作業系統中的時間稱為 PID GTHR DIRLINK。</span><span class="sxs-lookup"><span data-stu-id="227cc-111">[System.Search.UrlToIndexWithModificationTime]() was called PID\_GTHR\_DIRLINK\_WITH\_TIME in earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="227cc-112">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="227cc-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="227cc-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="227cc-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="227cc-114">[UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="227cc-114">[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="227cc-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="227cc-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="227cc-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="227cc-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="227cc-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="227cc-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="227cc-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="227cc-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="227cc-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="227cc-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="227cc-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="227cc-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="227cc-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="227cc-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="227cc-122">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="227cc-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="227cc-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="227cc-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="227cc-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="227cc-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="227cc-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="227cc-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="227cc-126">editControl</span><span class="sxs-lookup"><span data-stu-id="227cc-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="227cc-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="227cc-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="227cc-128">queryControl</span><span class="sxs-lookup"><span data-stu-id="227cc-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
