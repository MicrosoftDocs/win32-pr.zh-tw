---
description: 表示 debug 符號伺服器的相關資訊。
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SymbolServerInfo 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D57D87E4-BA94-4C6F-9D5F-999C61F4DD6F
api_name:
- SymbolServerInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 65bf07a8ff915668c6c059b831bd049d9a25d9a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108937"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span data-ttu-id="756c0-103"><span id="vspixengine.symbolserverinfo"></span>SymbolServerInfo 結構</span><span class="sxs-lookup"><span data-stu-id="756c0-103"><span id="vspixengine.symbolserverinfo"></span>SymbolServerInfo structure</span></span>

<span data-ttu-id="756c0-104">表示 debug 符號伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="756c0-104">Represents information about the debug symbol server.</span></span>

## <a name="syntax"></a><span data-ttu-id="756c0-105">語法</span><span class="sxs-lookup"><span data-stu-id="756c0-105">Syntax</span></span>


```C++
} SymbolServerInfo;
```

## <a name="members"></a><span data-ttu-id="756c0-106">成員</span><span class="sxs-lookup"><span data-stu-id="756c0-106">Members</span></span>

<span data-ttu-id="756c0-107">**symbolPath**</span><span class="sxs-lookup"><span data-stu-id="756c0-107">**symbolPath**</span></span>  
<span data-ttu-id="756c0-108">包含符號伺服器路徑的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="756c0-108">A COM string containing the path of the symbol server.</span></span>

<span data-ttu-id="756c0-109">**symbolCacheDir**</span><span class="sxs-lookup"><span data-stu-id="756c0-109">**symbolCacheDir**</span></span>  
<span data-ttu-id="756c0-110">COM 字串，其中包含符號伺服器的快取目錄。</span><span class="sxs-lookup"><span data-stu-id="756c0-110">A COM string containing the cache directory of the symbol server.</span></span>

<span data-ttu-id="756c0-111">**publicSymbolServerName**</span><span class="sxs-lookup"><span data-stu-id="756c0-111">**publicSymbolServerName**</span></span>  
<span data-ttu-id="756c0-112">COM 字串，其中包含符號伺服器的公用名稱。</span><span class="sxs-lookup"><span data-stu-id="756c0-112">A COM string containing the public name of the symbol server.</span></span>

<span data-ttu-id="756c0-113">**symbolExcludeList**</span><span class="sxs-lookup"><span data-stu-id="756c0-113">**symbolExcludeList**</span></span>  
<span data-ttu-id="756c0-114">COM 字串，指定要排除的符號清單。</span><span class="sxs-lookup"><span data-stu-id="756c0-114">A COM string that specifies the list of symbols to exclude.</span></span>

<span data-ttu-id="756c0-115">**symbolIncludeList**</span><span class="sxs-lookup"><span data-stu-id="756c0-115">**symbolIncludeList**</span></span>  
<span data-ttu-id="756c0-116">COM 字串，指定要包含的符號清單。</span><span class="sxs-lookup"><span data-stu-id="756c0-116">A COM string that specifies the list of symbols to include.</span></span>

<span data-ttu-id="756c0-117">**useExcludeList**</span><span class="sxs-lookup"><span data-stu-id="756c0-117">**useExcludeList**</span></span>  
<span data-ttu-id="756c0-118">如果忽略排除清單，則為 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="756c0-118">true if the exclude list is ignored; otherwise, false.</span></span>

<span data-ttu-id="756c0-119">**useMSSymbolServer**</span><span class="sxs-lookup"><span data-stu-id="756c0-119">**useMSSymbolServer**</span></span>  
<span data-ttu-id="756c0-120">如果使用 Microsoft 符號伺服器，則為 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="756c0-120">true if using Microsoft symbol server; otherwise, false.</span></span>

## <a name="requirements"></a><span data-ttu-id="756c0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="756c0-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="756c0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="756c0-122">Header</span></span></p></td><td><span data-ttu-id="756c0-123">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="756c0-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



