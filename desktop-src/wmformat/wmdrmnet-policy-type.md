---
title: 'WMDRMNET_POLICY_TYPE 列舉 (Wmdrmsdk .h) '
description: WMDRMNET \_ 原則 \_ 類型列舉類型會列出可用於網路裝置作業之 WINDOWS Media DRM 的原則類型。
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- WMDRMNET_POLICY_TYPE 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964a3e938caa312f02f21074f046f3cf88d72de6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993458"
---
# <a name="wmdrmnet_policy_type-enumeration"></a><span data-ttu-id="1f333-105">WMDRMNET \_ 原則 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="1f333-105">WMDRMNET\_POLICY\_TYPE enumeration</span></span>

<span data-ttu-id="1f333-106">**WMDRMNET \_ 原則 \_ 類型** 列舉類型會列出可用於網路裝置作業之 Windows Media DRM 的原則類型。</span><span class="sxs-lookup"><span data-stu-id="1f333-106">The **WMDRMNET\_POLICY\_TYPE** enumeration type lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f333-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f333-107">Syntax</span></span>


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a><span data-ttu-id="1f333-108">常數</span><span class="sxs-lookup"><span data-stu-id="1f333-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1f333-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**WMDRMNET \_ 原則 \_ 類型 \_ 未定義**</span><span class="sxs-lookup"><span data-stu-id="1f333-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**WMDRMNET\_POLICY\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="1f333-110">不支援未定義的原則類型。</span><span class="sxs-lookup"><span data-stu-id="1f333-110">Undefined policy types are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1f333-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**WMDRMNET \_ 原則 \_ 類型 \_ TRANSCRYPTPLAY**</span><span class="sxs-lookup"><span data-stu-id="1f333-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**</span></span>
</dt> <dd>

<span data-ttu-id="1f333-112">此原則可讓您將受 Windows Media DRM 保護的內容轉換為網路裝置資料的受保護 Windows Media DRM，並在網路裝置上播放。</span><span class="sxs-lookup"><span data-stu-id="1f333-112">The policy governs the ability to convert content protected by Windows Media DRM into protected Windows Media DRM for Network Devices data and play it back on a networked device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f333-113">備註</span><span class="sxs-lookup"><span data-stu-id="1f333-113">Remarks</span></span>

<span data-ttu-id="1f333-114">無。</span><span class="sxs-lookup"><span data-stu-id="1f333-114">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f333-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f333-115">Requirements</span></span>



| <span data-ttu-id="1f333-116">需求</span><span class="sxs-lookup"><span data-stu-id="1f333-116">Requirement</span></span> | <span data-ttu-id="1f333-117">值</span><span class="sxs-lookup"><span data-stu-id="1f333-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f333-118">標頭</span><span class="sxs-lookup"><span data-stu-id="1f333-118">Header</span></span><br/> | <dl> <span data-ttu-id="1f333-119"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f333-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f333-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f333-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f333-121">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="1f333-121">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="1f333-122">**WMDRMNET \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="1f333-122">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





