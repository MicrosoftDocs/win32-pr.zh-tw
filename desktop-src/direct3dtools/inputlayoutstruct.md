---
description: 表示頂點緩衝區的輸入配置欄位，在頂點緩衝區中每個欄位一個。
MS-HAID: vspixengine.InputLayoutStruct
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: InputLayoutStruct 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC7AAC2F-FDB1-4AD8-9B87-A97EE557FEAC
api_name:
- InputLayoutStruct
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1369d80d202682b67eacbb184b215d9da1711874
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973540"
---
# <a name="span-idvspixengineinputlayoutstructspaninputlayoutstruct-structure"></a><span data-ttu-id="c101a-103"><span id="vspixengine.inputlayoutstruct"></span>InputLayoutStruct 結構</span><span class="sxs-lookup"><span data-stu-id="c101a-103"><span id="vspixengine.inputlayoutstruct"></span>InputLayoutStruct structure</span></span>

<span data-ttu-id="c101a-104">表示頂點緩衝區的輸入配置欄位，在頂點緩衝區中每個欄位一個。</span><span class="sxs-lookup"><span data-stu-id="c101a-104">Represents the input layout fields of a vertex buffer, one per field in the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c101a-105">語法</span><span class="sxs-lookup"><span data-stu-id="c101a-105">Syntax</span></span>


```C++
} InputLayoutStruct;
```

## <a name="members"></a><span data-ttu-id="c101a-106">成員</span><span class="sxs-lookup"><span data-stu-id="c101a-106">Members</span></span>

<span data-ttu-id="c101a-107">**SemanticName**</span><span class="sxs-lookup"><span data-stu-id="c101a-107">**SemanticName**</span></span>  
<span data-ttu-id="c101a-108">COM 字串，其中包含相關聯之語義的名稱。</span><span class="sxs-lookup"><span data-stu-id="c101a-108">A COM string containing the name of the associated semantic.</span></span>

<span data-ttu-id="c101a-109">**SemanticIndex**</span><span class="sxs-lookup"><span data-stu-id="c101a-109">**SemanticIndex**</span></span>  
<span data-ttu-id="c101a-110">相關聯之語義的索引。</span><span class="sxs-lookup"><span data-stu-id="c101a-110">The index of the associated semantic.</span></span>

<span data-ttu-id="c101a-111">**格式**</span><span class="sxs-lookup"><span data-stu-id="c101a-111">**Format**</span></span>  
<span data-ttu-id="c101a-112">欄位的格式。</span><span class="sxs-lookup"><span data-stu-id="c101a-112">The format of the field.</span></span> <span data-ttu-id="c101a-113">如需詳細資訊，請參閱 DXGI \_ 格式列舉。</span><span class="sxs-lookup"><span data-stu-id="c101a-113">For more information see the DXGI\_FORMAT enumeration.</span></span>

<span data-ttu-id="c101a-114">**InputSlot**</span><span class="sxs-lookup"><span data-stu-id="c101a-114">**InputSlot**</span></span>  
<span data-ttu-id="c101a-115">相關聯的輸入位置。</span><span class="sxs-lookup"><span data-stu-id="c101a-115">The associated input slot.</span></span>

<span data-ttu-id="c101a-116">**AlignedByteOffset**</span><span class="sxs-lookup"><span data-stu-id="c101a-116">**AlignedByteOffset**</span></span>  

<span data-ttu-id="c101a-117">**InputSlotClass**</span><span class="sxs-lookup"><span data-stu-id="c101a-117">**InputSlotClass**</span></span>  

<span data-ttu-id="c101a-118">**InstanceDataStepRate**</span><span class="sxs-lookup"><span data-stu-id="c101a-118">**InstanceDataStepRate**</span></span>  

## <a name="requirements"></a><span data-ttu-id="c101a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c101a-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c101a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c101a-120">Header</span></span></p></td><td><span data-ttu-id="c101a-121">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="c101a-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



