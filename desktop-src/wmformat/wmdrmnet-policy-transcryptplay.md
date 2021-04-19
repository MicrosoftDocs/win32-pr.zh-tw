---
title: 'WMDRMNET_POLICY_TRANSCRYPTPLAY 結構 (Wmdrmsdk .h) '
description: WMDRMNET \_ POLICY \_ TRANSCRYPTPLAY 結構包含使用 WINDOWS Media DRM 為網路裝置播放內容的原則資訊。
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- WMDRMNET_POLICY_TRANSCRYPTPLAY 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982915"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a><span data-ttu-id="e6067-105">WMDRMNET \_ 原則 \_ TRANSCRYPTPLAY 結構</span><span class="sxs-lookup"><span data-stu-id="e6067-105">WMDRMNET\_POLICY\_TRANSCRYPTPLAY structure</span></span>

<span data-ttu-id="e6067-106">**WMDRMNET \_ POLICY \_ TRANSCRYPTPLAY** 結構包含使用 Windows Media DRM 為網路裝置播放內容的原則資訊。</span><span class="sxs-lookup"><span data-stu-id="e6067-106">The **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure holds the policy information for playing content using Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6067-107">語法</span><span class="sxs-lookup"><span data-stu-id="e6067-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a><span data-ttu-id="e6067-108">成員</span><span class="sxs-lookup"><span data-stu-id="e6067-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6067-109">**globals**</span><span class="sxs-lookup"><span data-stu-id="e6067-109">**globals**</span></span>
</dt> <dd>

<span data-ttu-id="e6067-110">全域原則結構。</span><span class="sxs-lookup"><span data-stu-id="e6067-110">Global policy structure.</span></span>

</dd> <dt>

<span data-ttu-id="e6067-111">**playOPLs**</span><span class="sxs-lookup"><span data-stu-id="e6067-111">**playOPLs**</span></span>
</dt> <dd>

<span data-ttu-id="e6067-112">輸出保護層級以供播放。</span><span class="sxs-lookup"><span data-stu-id="e6067-112">Output protection levels for playback.</span></span> <span data-ttu-id="e6067-113">**WMDRMNET \_原則 \_ 播放 \_ OPL** 是定義為 [**DRM \_ PLAY \_ OPL \_**](drm-play-opl-ex.md)的類型，例如</span><span class="sxs-lookup"><span data-stu-id="e6067-113">**WMDRMNET\_POLICY\_PLAY\_OPL** is a type defined as [**DRM\_PLAY\_OPL\_EX**](drm-play-opl-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6067-114">備註</span><span class="sxs-lookup"><span data-stu-id="e6067-114">Remarks</span></span>

<span data-ttu-id="e6067-115">無。</span><span class="sxs-lookup"><span data-stu-id="e6067-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6067-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6067-116">Requirements</span></span>



| <span data-ttu-id="e6067-117">需求</span><span class="sxs-lookup"><span data-stu-id="e6067-117">Requirement</span></span> | <span data-ttu-id="e6067-118">值</span><span class="sxs-lookup"><span data-stu-id="e6067-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6067-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e6067-119">Header</span></span><br/> | <dl> <span data-ttu-id="e6067-120"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6067-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6067-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6067-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6067-122">**結構**</span><span class="sxs-lookup"><span data-stu-id="e6067-122">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="e6067-123">**WMDRMNET \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="e6067-123">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





