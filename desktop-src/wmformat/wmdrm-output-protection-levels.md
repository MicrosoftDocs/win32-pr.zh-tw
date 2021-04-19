---
title: 'WMDRM_OUTPUT_PROTECTION_LEVELS 結構 (Wmdrmsdk .h) '
description: WMDRM \_ 輸出 \_ 保護 \_ 層級結構包含 (OPLs) 的輸出保護層級，以執行各種動作的授權所需。
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- WMDRM_OUTPUT_PROTECTION_LEVELS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d720a8aef42178da188b71a1635d97031b138397
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985557"
---
# <a name="wmdrm_output_protection_levels-structure"></a><span data-ttu-id="d382a-105">WMDRM \_ 輸出 \_ 保護 \_ 層級結構</span><span class="sxs-lookup"><span data-stu-id="d382a-105">WMDRM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="d382a-106">**WMDRM \_ 輸出 \_ 保護 \_ 層級** 結構包含 (OPLs) 的輸出保護層級，以執行各種動作的授權所需。</span><span class="sxs-lookup"><span data-stu-id="d382a-106">The **WMDRM\_OUTPUT\_PROTECTION\_LEVELS** structure contains the output protections levels (OPLs) required by a license to perform various actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d382a-107">語法</span><span class="sxs-lookup"><span data-stu-id="d382a-107">Syntax</span></span>


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
} ;
```



## <a name="members"></a><span data-ttu-id="d382a-108">成員</span><span class="sxs-lookup"><span data-stu-id="d382a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d382a-109">**wCompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="d382a-109">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="d382a-110">接收壓縮數位影片所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="d382a-110">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="d382a-111">**wUncompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="d382a-111">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="d382a-112">接收未壓縮數位影片所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="d382a-112">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="d382a-113">**wAnalogVideo**</span><span class="sxs-lookup"><span data-stu-id="d382a-113">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="d382a-114">接收類比影片所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="d382a-114">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="d382a-115">**wCompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="d382a-115">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="d382a-116">接收壓縮數位音訊所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="d382a-116">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="d382a-117">**wUncompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="d382a-117">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="d382a-118">接收未壓縮數位音訊所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="d382a-118">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="d382a-119">**wMinimumCopyProtectionLevel**</span><span class="sxs-lookup"><span data-stu-id="d382a-119">**wMinimumCopyProtectionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="d382a-120">複製內容所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="d382a-120">Minimum OPL required to copy the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d382a-121">備註</span><span class="sxs-lookup"><span data-stu-id="d382a-121">Remarks</span></span>

<span data-ttu-id="d382a-122">此結構是由 [**IWMDRMLicense：： GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="d382a-122">This structure is used by the [**IWMDRMLicense::GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d382a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d382a-123">Requirements</span></span>



| <span data-ttu-id="d382a-124">需求</span><span class="sxs-lookup"><span data-stu-id="d382a-124">Requirement</span></span> | <span data-ttu-id="d382a-125">值</span><span class="sxs-lookup"><span data-stu-id="d382a-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d382a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d382a-126">Header</span></span><br/> | <dl> <span data-ttu-id="d382a-127"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="d382a-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d382a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d382a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d382a-129">**結構**</span><span class="sxs-lookup"><span data-stu-id="d382a-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





