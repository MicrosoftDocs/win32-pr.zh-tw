---
description: 描述 JPEG AC huffman 資料表。
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: 'DXGI_JPEG_AC_HUFFMAN_TABLE 結構 (Dxgitype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_AC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 760840822eb6b9411983c72324bc1e86a3208195
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106979872"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a><span data-ttu-id="e6c30-103">DXGI \_ JPEG \_ AC \_ HUFFMAN \_ 資料表結構</span><span class="sxs-lookup"><span data-stu-id="e6c30-103">DXGI\_JPEG\_AC\_HUFFMAN\_TABLE structure</span></span>

<span data-ttu-id="e6c30-104">描述 JPEG AC huffman 資料表。</span><span class="sxs-lookup"><span data-stu-id="e6c30-104">Describes a JPEG AC huffman table.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c30-105">語法</span><span class="sxs-lookup"><span data-stu-id="e6c30-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
```



## <a name="members"></a><span data-ttu-id="e6c30-106">成員</span><span class="sxs-lookup"><span data-stu-id="e6c30-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6c30-107">**CodeCounts**</span><span class="sxs-lookup"><span data-stu-id="e6c30-107">**CodeCounts**</span></span>
</dt> <dd>

<span data-ttu-id="e6c30-108">每個程式碼長度的程式碼數目。</span><span class="sxs-lookup"><span data-stu-id="e6c30-108">The number of codes for each code length.</span></span>

</dd> <dt>

<span data-ttu-id="e6c30-109">**CodeValues**</span><span class="sxs-lookup"><span data-stu-id="e6c30-109">**CodeValues**</span></span>
</dt> <dd>

<span data-ttu-id="e6c30-110">Huffman 代碼值，以增加程式碼長度的順序排列。</span><span class="sxs-lookup"><span data-stu-id="e6c30-110">The Huffman code values, in order of increasing code length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6c30-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6c30-111">Requirements</span></span>



| <span data-ttu-id="e6c30-112">需求</span><span class="sxs-lookup"><span data-stu-id="e6c30-112">Requirement</span></span> | <span data-ttu-id="e6c30-113">值</span><span class="sxs-lookup"><span data-stu-id="e6c30-113">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c30-114">標頭</span><span class="sxs-lookup"><span data-stu-id="e6c30-114">Header</span></span><br/> | <dl> <span data-ttu-id="e6c30-115"><dt>Dxgitype。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6c30-115"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6c30-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6c30-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c30-117">DXGI 結構</span><span class="sxs-lookup"><span data-stu-id="e6c30-117">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




