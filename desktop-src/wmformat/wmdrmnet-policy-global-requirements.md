---
title: 'WMDRMNET_POLICY_GLOBAL_REQUIREMENTS 結構 (Wmdrmsdk .h) '
description: WMDRMNET \_ 原則的 \_ 全域 \_ 需求結構具有適用于網路裝置之 Windows Media DRM 的全域需求。
ms.assetid: 140b3a6f-ccba-4735-b48a-2e990f5ec570
keywords:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ccf13c881c9696d970a00ac902f3f8d08f13c58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000695"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a><span data-ttu-id="cba15-105">WMDRMNET \_ 原則的 \_ 全域 \_ 需求結構</span><span class="sxs-lookup"><span data-stu-id="cba15-105">WMDRMNET\_POLICY\_GLOBAL\_REQUIREMENTS structure</span></span>

<span data-ttu-id="cba15-106">**WMDRMNET \_ 原則的 \_ 全域 \_ 需求** 結構具有適用于網路裝置之 Windows Media DRM 的全域需求。</span><span class="sxs-lookup"><span data-stu-id="cba15-106">The **WMDRMNET\_POLICY\_GLOBAL\_REQUIREMENTS** structure holds global requirements for Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="cba15-107">語法</span><span class="sxs-lookup"><span data-stu-id="cba15-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_GLOBAL_REQUIREMENTS {
  WMDRMNET_POLICY_MINIMUM_ENVIRONMENT MinimumEnvironment;
} ;
```



## <a name="members"></a><span data-ttu-id="cba15-108">成員</span><span class="sxs-lookup"><span data-stu-id="cba15-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cba15-109">**MinimumEnvironment**</span><span class="sxs-lookup"><span data-stu-id="cba15-109">**MinimumEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="cba15-110">[**WMDRMNET \_原則 \_ 最小 \_ 環境**](wmdrmnet-policy-minimum-environment.md) 結構，其中包含網路裝置的 Windows Media DRM 的最低安全性需求。</span><span class="sxs-lookup"><span data-stu-id="cba15-110">[**WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT**](wmdrmnet-policy-minimum-environment.md) structure containing the minimum security requirements for Windows Media DRM for Network Devices.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cba15-111">備註</span><span class="sxs-lookup"><span data-stu-id="cba15-111">Remarks</span></span>

<span data-ttu-id="cba15-112">無。</span><span class="sxs-lookup"><span data-stu-id="cba15-112">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="cba15-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cba15-113">Requirements</span></span>



| <span data-ttu-id="cba15-114">需求</span><span class="sxs-lookup"><span data-stu-id="cba15-114">Requirement</span></span> | <span data-ttu-id="cba15-115">值</span><span class="sxs-lookup"><span data-stu-id="cba15-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cba15-116">標頭</span><span class="sxs-lookup"><span data-stu-id="cba15-116">Header</span></span><br/> | <dl> <span data-ttu-id="cba15-117"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="cba15-117"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cba15-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cba15-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba15-119">**結構**</span><span class="sxs-lookup"><span data-stu-id="cba15-119">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="cba15-120">**WMDRMNET \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="cba15-120">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





