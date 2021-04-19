---
title: 'WMDRMNET_POLICY 結構 (Wmdrmsdk .h) '
description: WMDRMNET \_ 原則結構包含用於網路裝置作業之 Windows MEDIA DRM 的原則。
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- WMDRMNET_POLICY 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986181"
---
# <a name="wmdrmnet_policy-structure"></a><span data-ttu-id="c083a-105">WMDRMNET \_ 原則結構</span><span class="sxs-lookup"><span data-stu-id="c083a-105">WMDRMNET\_POLICY structure</span></span>

<span data-ttu-id="c083a-106">**WMDRMNET \_ 原則** 結構包含用於網路裝置作業之 Windows Media DRM 的原則。</span><span class="sxs-lookup"><span data-stu-id="c083a-106">The **WMDRMNET\_POLICY** structure contains the policy to be used for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="c083a-107">語法</span><span class="sxs-lookup"><span data-stu-id="c083a-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a><span data-ttu-id="c083a-108">成員</span><span class="sxs-lookup"><span data-stu-id="c083a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c083a-109">**ePolicyType**</span><span class="sxs-lookup"><span data-stu-id="c083a-109">**ePolicyType**</span></span>
</dt> <dd>

<span data-ttu-id="c083a-110">指定原則類型之 [**WMDRMNET \_ 原則 \_ 類型**](wmdrmnet-policy-type.md) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="c083a-110">Member of the [**WMDRMNET\_POLICY\_TYPE**](wmdrmnet-policy-type.md) enumeration that specifies the type of policy.</span></span>

</dd> <dt>

<span data-ttu-id="c083a-111">**pbPolicy**</span><span class="sxs-lookup"><span data-stu-id="c083a-111">**pbPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="c083a-112">包含原則的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c083a-112">Buffer containing the policy.</span></span> <span data-ttu-id="c083a-113">目前唯一支援的原則類型是 **WMDRMNET \_ 原則 \_ 類型 \_ TRANSCRYPTPLAY**。</span><span class="sxs-lookup"><span data-stu-id="c083a-113">The only type of policy currently supported is **WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**.</span></span> <span data-ttu-id="c083a-114">此成員是 **WMDRMNET \_ 原則 \_ TRANSCRYPTPLAY** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c083a-114">This member is a pointer to a **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c083a-115">備註</span><span class="sxs-lookup"><span data-stu-id="c083a-115">Remarks</span></span>

<span data-ttu-id="c083a-116">此結構是用來做為 [**IWMDRMNetTransmitter：： GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) 方法的參數。</span><span class="sxs-lookup"><span data-stu-id="c083a-116">This structure is used as a parameter for the [**IWMDRMNetTransmitter::GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c083a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c083a-117">Requirements</span></span>



| <span data-ttu-id="c083a-118">需求</span><span class="sxs-lookup"><span data-stu-id="c083a-118">Requirement</span></span> | <span data-ttu-id="c083a-119">值</span><span class="sxs-lookup"><span data-stu-id="c083a-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c083a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c083a-120">Header</span></span><br/> | <dl> <span data-ttu-id="c083a-121"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="c083a-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c083a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c083a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c083a-123">**結構**</span><span class="sxs-lookup"><span data-stu-id="c083a-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="c083a-124">**WMDRMNET \_ 原則的 \_ 全域 \_ 需求**</span><span class="sxs-lookup"><span data-stu-id="c083a-124">**WMDRMNET\_POLICY\_GLOBAL\_REQUIREMENTS**</span></span>](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[<span data-ttu-id="c083a-125">**WMDRMNET \_ 原則的 \_ 最小 \_ 環境**</span><span class="sxs-lookup"><span data-stu-id="c083a-125">**WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT**</span></span>](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[<span data-ttu-id="c083a-126">**WMDRMNET \_ 原則 \_ TRANSCRYPTPLAY**</span><span class="sxs-lookup"><span data-stu-id="c083a-126">**WMDRMNET\_POLICY\_TRANSCRYPTPLAY**</span></span>](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[<span data-ttu-id="c083a-127">**WMDRMNET \_ 原則 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="c083a-127">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





