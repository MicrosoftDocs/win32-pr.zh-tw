---
description: 描述 JPEG 量化資料表。
ms.assetid: DE1AAB15-B0B8-4594-BBCE-5F8EE5CE0AF7
title: 'DXGI_JPEG_QUANTIZATION_TABLE 結構 (Dxgitype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_QUANTIZATION_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b0a097cb4c364ecc14e471f7c15f642aa65e912
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985878"
---
# <a name="dxgi_jpeg_quantization_table-structure"></a><span data-ttu-id="73068-103">DXGI \_ JPEG \_ 量化 \_ 資料表結構</span><span class="sxs-lookup"><span data-stu-id="73068-103">DXGI\_JPEG\_QUANTIZATION\_TABLE structure</span></span>

<span data-ttu-id="73068-104">描述 JPEG 量化資料表。</span><span class="sxs-lookup"><span data-stu-id="73068-104">Describes a JPEG quantization table.</span></span>

## <a name="syntax"></a><span data-ttu-id="73068-105">語法</span><span class="sxs-lookup"><span data-stu-id="73068-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_QUANTIZATION_TABLE {
  BYTE Elements[64];
} DXGI_JPEG_QUANTIZATION_TABLE;
```



## <a name="members"></a><span data-ttu-id="73068-106">成員</span><span class="sxs-lookup"><span data-stu-id="73068-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="73068-107">**元素**</span><span class="sxs-lookup"><span data-stu-id="73068-107">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="73068-108">包含量化資料表元素的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="73068-108">An array of bytes containing the elements of the quantization table.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73068-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="73068-109">Requirements</span></span>



| <span data-ttu-id="73068-110">需求</span><span class="sxs-lookup"><span data-stu-id="73068-110">Requirement</span></span> | <span data-ttu-id="73068-111">值</span><span class="sxs-lookup"><span data-stu-id="73068-111">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73068-112">標頭</span><span class="sxs-lookup"><span data-stu-id="73068-112">Header</span></span><br/> | <dl> <span data-ttu-id="73068-113"><dt>Dxgitype。h</dt></span><span class="sxs-lookup"><span data-stu-id="73068-113"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73068-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73068-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73068-115">DXGI 結構</span><span class="sxs-lookup"><span data-stu-id="73068-115">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




