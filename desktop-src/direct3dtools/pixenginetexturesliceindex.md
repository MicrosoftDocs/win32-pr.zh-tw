---
description: 表示紋理配量的索引。
MS-HAID: vspixengine.PixEngineTextureSliceIndex
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineTextureSliceIndex 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 127765F7-4EBF-4B66-9491-A6FE9DC673C8
api_name:
- PixEngineTextureSliceIndex
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0fd954b5ba9d4dd20f35245350857352bc9b8ae3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973547"
---
# <a name="span-idvspixenginepixenginetexturesliceindexspanpixenginetexturesliceindex-structure"></a><span data-ttu-id="cb741-103"><span id="vspixengine.pixenginetexturesliceindex"></span>PixEngineTextureSliceIndex 結構</span><span class="sxs-lookup"><span data-stu-id="cb741-103"><span id="vspixengine.pixenginetexturesliceindex"></span>PixEngineTextureSliceIndex structure</span></span>

<span data-ttu-id="cb741-104">代表材質配量的索引</span><span class="sxs-lookup"><span data-stu-id="cb741-104">Represents the index of a texture slice</span></span>

## <a name="syntax"></a><span data-ttu-id="cb741-105">語法</span><span class="sxs-lookup"><span data-stu-id="cb741-105">Syntax</span></span>


```C++
} PixEngineTextureSliceIndex;
```

## <a name="members"></a><span data-ttu-id="cb741-106">成員</span><span class="sxs-lookup"><span data-stu-id="cb741-106">Members</span></span>

<span data-ttu-id="cb741-107">**arrayIndex**</span><span class="sxs-lookup"><span data-stu-id="cb741-107">**arrayIndex**</span></span>  
<span data-ttu-id="cb741-108">當材質是材質陣列時，即為配量的陣列索引。</span><span class="sxs-lookup"><span data-stu-id="cb741-108">When the texture is a texture array, the array index of the slice.</span></span>

<span data-ttu-id="cb741-109">**mipmapLevel**</span><span class="sxs-lookup"><span data-stu-id="cb741-109">**mipmapLevel**</span></span>  
<span data-ttu-id="cb741-110">配量的 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="cb741-110">The mipmap level of the slice.</span></span>

<span data-ttu-id="cb741-111">**sampleIndex**</span><span class="sxs-lookup"><span data-stu-id="cb741-111">**sampleIndex**</span></span>  
<span data-ttu-id="cb741-112">配量的範例索引。</span><span class="sxs-lookup"><span data-stu-id="cb741-112">The sample index of the slice.</span></span>

<span data-ttu-id="cb741-113">**zSlice**</span><span class="sxs-lookup"><span data-stu-id="cb741-113">**zSlice**</span></span>  
<span data-ttu-id="cb741-114">配量的深度 (z) 。</span><span class="sxs-lookup"><span data-stu-id="cb741-114">The depth (z) of the slice.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb741-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb741-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cb741-116">標頭</span><span class="sxs-lookup"><span data-stu-id="cb741-116">Header</span></span></p></td><td><span data-ttu-id="cb741-117">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="cb741-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



