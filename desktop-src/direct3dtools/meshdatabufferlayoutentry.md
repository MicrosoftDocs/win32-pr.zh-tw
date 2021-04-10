---
description: 表示網格的緩衝區配置中單一專案的相關資訊。
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MeshDataBufferLayoutEntry 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bce67b8316e9eb9b96e641e2a90260fab6bfdaad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688464"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span data-ttu-id="a1f83-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>MeshDataBufferLayoutEntry 結構</span><span class="sxs-lookup"><span data-stu-id="a1f83-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>MeshDataBufferLayoutEntry structure</span></span>

<span data-ttu-id="a1f83-104">表示網格的緩衝區配置中單一專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1f83-104">Represents information about a single entry in the buffer layout of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f83-105">語法</span><span class="sxs-lookup"><span data-stu-id="a1f83-105">Syntax</span></span>


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a><span data-ttu-id="a1f83-106">成員</span><span class="sxs-lookup"><span data-stu-id="a1f83-106">Members</span></span>

<span data-ttu-id="a1f83-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="a1f83-107">**pName**</span></span>  
<span data-ttu-id="a1f83-108">包含專案名稱的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="a1f83-108">A COM string containing the name of the entry.</span></span>

<span data-ttu-id="a1f83-109">**numComponents**</span><span class="sxs-lookup"><span data-stu-id="a1f83-109">**numComponents**</span></span>  
<span data-ttu-id="a1f83-110">組成此專案)  (值的同質元件數目。</span><span class="sxs-lookup"><span data-stu-id="a1f83-110">The number of homogenous components (values) that make up this entry.</span></span>

<span data-ttu-id="a1f83-111">**isPosition**</span><span class="sxs-lookup"><span data-stu-id="a1f83-111">**isPosition**</span></span>  
<span data-ttu-id="a1f83-112">如果專案是位置，則為 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="a1f83-112">true if the entry is a position; otherwise, false.</span></span>

<span data-ttu-id="a1f83-113">**format**</span><span class="sxs-lookup"><span data-stu-id="a1f83-113">**format**</span></span>  
<span data-ttu-id="a1f83-114">專案 (註冊) 的資料格式。</span><span class="sxs-lookup"><span data-stu-id="a1f83-114">The data format of the entry (register).</span></span> <span data-ttu-id="a1f83-115">如需詳細資訊，請參閱註冊 \_ 格式列舉。</span><span class="sxs-lookup"><span data-stu-id="a1f83-115">For more information, see the REGISTER\_FORMAT enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1f83-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1f83-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a1f83-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a1f83-117">Header</span></span></p></td><td><span data-ttu-id="a1f83-118">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="a1f83-118">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



