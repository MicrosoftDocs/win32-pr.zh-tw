---
description: 代表材質配量的描述。
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineTextureSliceDescriptor 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1A183AFB-0BEF-4474-A60C-DBCFA4B34604
api_name:
- PixEngineTextureSliceDescriptor
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b80a23a5ec3340b775c314f66651926743249ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108821"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span data-ttu-id="63eff-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>PixEngineTextureSliceDescriptor 結構</span><span class="sxs-lookup"><span data-stu-id="63eff-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>PixEngineTextureSliceDescriptor structure</span></span>

<span data-ttu-id="63eff-104">代表材質配量的描述。</span><span class="sxs-lookup"><span data-stu-id="63eff-104">Represents a description of a texture slice.</span></span>

## <a name="syntax"></a><span data-ttu-id="63eff-105">語法</span><span class="sxs-lookup"><span data-stu-id="63eff-105">Syntax</span></span>


```C++
} PixEngineTextureSliceDescriptor;
```

## <a name="members"></a><span data-ttu-id="63eff-106">成員</span><span class="sxs-lookup"><span data-stu-id="63eff-106">Members</span></span>

<span data-ttu-id="63eff-107">**width** (寬度)</span><span class="sxs-lookup"><span data-stu-id="63eff-107">**width**</span></span>  
<span data-ttu-id="63eff-108">配量 (X 軸) 中的樣本數目。</span><span class="sxs-lookup"><span data-stu-id="63eff-108">The width (number of samples in the X axis) of the slice.</span></span>

<span data-ttu-id="63eff-109">**height** (高度)</span><span class="sxs-lookup"><span data-stu-id="63eff-109">**height**</span></span>  
<span data-ttu-id="63eff-110">在配量的 Y 軸) 中，高度 (樣本數。</span><span class="sxs-lookup"><span data-stu-id="63eff-110">The height (number of samples in the Y axis) of the slice.</span></span>

<span data-ttu-id="63eff-111">**blockRowBytes**</span><span class="sxs-lookup"><span data-stu-id="63eff-111">**blockRowBytes**</span></span>  
<span data-ttu-id="63eff-112">每個區塊中每個資料列的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="63eff-112">The number of bytes per row in each block.</span></span>

<span data-ttu-id="63eff-113">**offset**</span><span class="sxs-lookup"><span data-stu-id="63eff-113">**offset**</span></span>  
<span data-ttu-id="63eff-114">整個材質內配量的位移。</span><span class="sxs-lookup"><span data-stu-id="63eff-114">The offset of the slice within the whole texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="63eff-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="63eff-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="63eff-116">標頭</span><span class="sxs-lookup"><span data-stu-id="63eff-116">Header</span></span></p></td><td><span data-ttu-id="63eff-117">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="63eff-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



