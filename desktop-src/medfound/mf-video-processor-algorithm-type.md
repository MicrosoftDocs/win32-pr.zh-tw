---
description: 定義用於 MF \_ 視頻處理器演算法的視頻處理器演算法 \_ \_ 。
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: MF_VIDEO_PROCESSOR_ALGORITHM_TYPE 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 604fee61ae4b6a34d876de8c2863ee6dddad73d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972277"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a><span data-ttu-id="d67bb-103">MF \_ 視頻 \_ 處理器 \_ 演算法 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="d67bb-103">MF\_VIDEO\_PROCESSOR\_ALGORITHM\_TYPE enumeration</span></span>

<span data-ttu-id="d67bb-104">定義用於 [MF \_ 視頻 \_ 處理器 \_ 演算法](mf-video-processor-algorithm.md)的視頻處理器演算法。</span><span class="sxs-lookup"><span data-stu-id="d67bb-104">Defines algorithms for the video processor which is use by [MF\_VIDEO\_PROCESSOR\_ALGORITHM](mf-video-processor-algorithm.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d67bb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d67bb-105">Syntax</span></span>


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a><span data-ttu-id="d67bb-106">常數</span><span class="sxs-lookup"><span data-stu-id="d67bb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d67bb-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**MF \_ 視頻 \_ 處理器 \_ 演算法 \_ 預設**</span><span class="sxs-lookup"><span data-stu-id="d67bb-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="d67bb-108">預設模式優先于品質與速度的平衡</span><span class="sxs-lookup"><span data-stu-id="d67bb-108">default mode favors a balance of quality and speed</span></span>

</dd> <dt>

<span data-ttu-id="d67bb-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**MF \_ 視頻 \_ 處理器 \_ 演算法 \_ .mrf \_ CRF \_ 444**</span><span class="sxs-lookup"><span data-stu-id="d67bb-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_MRF\_CRF\_444**</span></span>
</dt> <dd>

<span data-ttu-id="d67bb-110">影片處理器一律會在內部處理 AYUV，並使用高品質的篩選。</span><span class="sxs-lookup"><span data-stu-id="d67bb-110">The video processor will always internally process in AYUV and use high quality filters.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d67bb-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d67bb-111">Requirements</span></span>



| <span data-ttu-id="d67bb-112">需求</span><span class="sxs-lookup"><span data-stu-id="d67bb-112">Requirement</span></span> | <span data-ttu-id="d67bb-113">值</span><span class="sxs-lookup"><span data-stu-id="d67bb-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d67bb-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d67bb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d67bb-115">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d67bb-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d67bb-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d67bb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d67bb-117">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d67bb-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d67bb-118">Idl</span><span class="sxs-lookup"><span data-stu-id="d67bb-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d67bb-119"><dt>Mfidl .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d67bb-119"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d67bb-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d67bb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d67bb-121">媒體基礎列舉</span><span class="sxs-lookup"><span data-stu-id="d67bb-121">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




