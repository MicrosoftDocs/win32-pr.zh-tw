---
description: 由容器 IFilter 針對容器內的每個子 URL 發出。 如果子系是在範圍內，則索引子最後會將子系編目。
ms.assetid: e864b3fa-6d43-40fe-9556-474953098947
title: UrlToIndex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4832279237cb7a3659b37d6502bd853caff113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982475"
---
# <a name="systemsearchurltoindex"></a><span data-ttu-id="1d171-104">UrlToIndex</span><span class="sxs-lookup"><span data-stu-id="1d171-104">System.Search.UrlToIndex</span></span>

<span data-ttu-id="1d171-105">由容器 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 針對容器內的每個子 URL 發出。</span><span class="sxs-lookup"><span data-stu-id="1d171-105">Emitted by a container [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) for each child URL within the container.</span></span> <span data-ttu-id="1d171-106">如果子系是在範圍內，則索引子最後會將子系編目。</span><span class="sxs-lookup"><span data-stu-id="1d171-106">The children are eventually crawled by the indexer if they are within scope.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="1d171-107">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本</span><span class="sxs-lookup"><span data-stu-id="1d171-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.UrlToIndex
   shellPKey = PKEY_Search_UrlToIndex
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
```

## <a name="remarks"></a><span data-ttu-id="1d171-108">備註</span><span class="sxs-lookup"><span data-stu-id="1d171-108">Remarks</span></span>

<span data-ttu-id="1d171-109">此屬性包含 URL，而且是由通訊協定處理常式針對目前 URL 下的每個子 URL 或 packageroot 目錄發出。</span><span class="sxs-lookup"><span data-stu-id="1d171-109">This property contains a URL and is emitted by a protocol handler for each child URL or directoy under the current URL.</span></span> <span data-ttu-id="1d171-110">索引子會回呼至通訊協定處理常式，並要求該檔進行索引。</span><span class="sxs-lookup"><span data-stu-id="1d171-110">The indexer calls back into the protocol handler, and asks for that document to be indexed.</span></span> <span data-ttu-id="1d171-111">[](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) \_ \_ 在舊版 Windows 作業系統中，UrlToIndex 稱為 PID GTHR DIRLINK。</span><span class="sxs-lookup"><span data-stu-id="1d171-111">[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) was called PID\_GTHR\_DIRLINK in earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="1d171-112">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="1d171-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d171-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d171-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d171-114">UrlToIndexWithModificationTime</span><span class="sxs-lookup"><span data-stu-id="1d171-114">System.Search.UrlToIndexWithModificationTime</span></span>](./props-system-search-urltoindexwithmodificationtime.md)
</dt> <dt>

[<span data-ttu-id="1d171-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="1d171-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1d171-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="1d171-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1d171-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="1d171-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1d171-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="1d171-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1d171-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1d171-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1d171-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="1d171-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1d171-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="1d171-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1d171-122">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="1d171-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1d171-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1d171-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1d171-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="1d171-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1d171-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="1d171-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1d171-126">editControl</span><span class="sxs-lookup"><span data-stu-id="1d171-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1d171-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="1d171-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1d171-128">queryControl</span><span class="sxs-lookup"><span data-stu-id="1d171-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
