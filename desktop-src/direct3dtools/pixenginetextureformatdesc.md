---
description: 代表材質格式的描述。
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineTextureFormatDesc 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 685DC746-544D-4ACB-AB1F-9FA62C5CF416
api_name:
- PixEngineTextureFormatDesc
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 960186f0c28be88805c1df65f1a517c4ce4a4c64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935873"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span data-ttu-id="f0997-103"><span id="vspixengine.pixenginetextureformatdesc"></span>PixEngineTextureFormatDesc 結構</span><span class="sxs-lookup"><span data-stu-id="f0997-103"><span id="vspixengine.pixenginetextureformatdesc"></span>PixEngineTextureFormatDesc structure</span></span>

<span data-ttu-id="f0997-104">代表材質格式的描述。</span><span class="sxs-lookup"><span data-stu-id="f0997-104">Represents a description of a texture format.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0997-105">語法</span><span class="sxs-lookup"><span data-stu-id="f0997-105">Syntax</span></span>


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a><span data-ttu-id="f0997-106">成員</span><span class="sxs-lookup"><span data-stu-id="f0997-106">Members</span></span>

<span data-ttu-id="f0997-107">**dxgiFormat**</span><span class="sxs-lookup"><span data-stu-id="f0997-107">**dxgiFormat**</span></span>  
<span data-ttu-id="f0997-108">材質的 DXGI 格式。</span><span class="sxs-lookup"><span data-stu-id="f0997-108">The DXGI format of the texture.</span></span>

<span data-ttu-id="f0997-109">**dataFormat**</span><span class="sxs-lookup"><span data-stu-id="f0997-109">**dataFormat**</span></span>  
<span data-ttu-id="f0997-110">材質的資料格式。</span><span class="sxs-lookup"><span data-stu-id="f0997-110">The data format of the texture.</span></span>

<span data-ttu-id="f0997-111">**blockBytes**</span><span class="sxs-lookup"><span data-stu-id="f0997-111">**blockBytes**</span></span>  
<span data-ttu-id="f0997-112">資料區塊中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="f0997-112">The number of bytes in a data block.</span></span>

<span data-ttu-id="f0997-113">**blockHeight**</span><span class="sxs-lookup"><span data-stu-id="f0997-113">**blockHeight**</span></span>  
<span data-ttu-id="f0997-114">在區塊的 Y 軸) 中，高度 (數位樣本。</span><span class="sxs-lookup"><span data-stu-id="f0997-114">The height (number samples in the Y axis) of the block.</span></span>

<span data-ttu-id="f0997-115">**blockWidth**</span><span class="sxs-lookup"><span data-stu-id="f0997-115">**blockWidth**</span></span>  
<span data-ttu-id="f0997-116">區塊 X 軸) 中的樣本 (數目。</span><span class="sxs-lookup"><span data-stu-id="f0997-116">The width (number of samples in the X axis) of the block.</span></span>

<span data-ttu-id="f0997-117">**channelX**</span><span class="sxs-lookup"><span data-stu-id="f0997-117">**channelX**</span></span>  
<span data-ttu-id="f0997-118">描述 X 通道的屬性。</span><span class="sxs-lookup"><span data-stu-id="f0997-118">Describes properties of the X channel.</span></span> <span data-ttu-id="f0997-119">如需詳細資訊，請參閱 PixEngineChannelDescription 結構。</span><span class="sxs-lookup"><span data-stu-id="f0997-119">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="f0997-120">**channelY**</span><span class="sxs-lookup"><span data-stu-id="f0997-120">**channelY**</span></span>  
<span data-ttu-id="f0997-121">描述 Y 通道的屬性。</span><span class="sxs-lookup"><span data-stu-id="f0997-121">Describes properties of the Y channel.</span></span> <span data-ttu-id="f0997-122">如需詳細資訊，請參閱 PixEngineChannelDescription 結構。</span><span class="sxs-lookup"><span data-stu-id="f0997-122">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="f0997-123">**channelZ**</span><span class="sxs-lookup"><span data-stu-id="f0997-123">**channelZ**</span></span>  
<span data-ttu-id="f0997-124">描述 Z 通道的屬性。</span><span class="sxs-lookup"><span data-stu-id="f0997-124">Describes properties of the Z channel.</span></span> <span data-ttu-id="f0997-125">如需詳細資訊，請參閱 PixEngineChannelDescription 結構。</span><span class="sxs-lookup"><span data-stu-id="f0997-125">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="f0997-126">**channelW**</span><span class="sxs-lookup"><span data-stu-id="f0997-126">**channelW**</span></span>  
<span data-ttu-id="f0997-127">描述 W 通道的屬性。</span><span class="sxs-lookup"><span data-stu-id="f0997-127">Describes properties of the W channel.</span></span> <span data-ttu-id="f0997-128">如需詳細資訊，請參閱 PixEngineChannelDescription 結構。</span><span class="sxs-lookup"><span data-stu-id="f0997-128">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="f0997-129">**swizzle**</span><span class="sxs-lookup"><span data-stu-id="f0997-129">**swizzle**</span></span>  
<span data-ttu-id="f0997-130">描述套用至範例的 swizzle (通道交換) 。</span><span class="sxs-lookup"><span data-stu-id="f0997-130">Describes the swizzle (channel-swapping) applied to the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0997-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0997-131">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f0997-132">標頭</span><span class="sxs-lookup"><span data-stu-id="f0997-132">Header</span></span></p></td><td><span data-ttu-id="f0997-133">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="f0997-133">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



