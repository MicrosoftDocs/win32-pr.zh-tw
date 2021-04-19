---
title: 'WMDRMNET_POLICY_MINIMUM_ENVIRONMENT 結構 (Wmdrmsdk .h) '
description: WMDRMNET \_ 原則的 \_ 最小 \_ 環境結構包含網路裝置的 Windows Media DRM 的最低安全性需求。
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf53fdec186a44eff375dd2e9cf9badfe0ba715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995398"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a><span data-ttu-id="14a96-105">WMDRMNET \_ 原則的 \_ 最小 \_ 環境結構</span><span class="sxs-lookup"><span data-stu-id="14a96-105">WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT structure</span></span>

<span data-ttu-id="14a96-106">**WMDRMNET \_ 原則的 \_ 最小 \_ 環境** 結構包含網路裝置的 Windows Media DRM 的最低安全性需求。</span><span class="sxs-lookup"><span data-stu-id="14a96-106">The **WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT** structure contains the minimum security requirements for Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a96-107">語法</span><span class="sxs-lookup"><span data-stu-id="14a96-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a><span data-ttu-id="14a96-108">成員</span><span class="sxs-lookup"><span data-stu-id="14a96-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="14a96-109">**wMinimumSecurityLevel**</span><span class="sxs-lookup"><span data-stu-id="14a96-109">**wMinimumSecurityLevel**</span></span>
</dt> <dd>

<span data-ttu-id="14a96-110">需要的最小應用程式安全性層級。</span><span class="sxs-lookup"><span data-stu-id="14a96-110">Minimum application security level required.</span></span>

</dd> <dt>

<span data-ttu-id="14a96-111">**dwMinimumAppRevocationListVersion**</span><span class="sxs-lookup"><span data-stu-id="14a96-111">**dwMinimumAppRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="14a96-112">需要最基本的應用程式憑證撤銷清單版本。</span><span class="sxs-lookup"><span data-stu-id="14a96-112">Minimum application certificate revocation list version required.</span></span>

</dd> <dt>

<span data-ttu-id="14a96-113">**dwMinimumDeviceRevocationListVersion**</span><span class="sxs-lookup"><span data-stu-id="14a96-113">**dwMinimumDeviceRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="14a96-114">需要最小的裝置憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="14a96-114">Minimum device certificate revocation list required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14a96-115">備註</span><span class="sxs-lookup"><span data-stu-id="14a96-115">Remarks</span></span>

<span data-ttu-id="14a96-116">無。</span><span class="sxs-lookup"><span data-stu-id="14a96-116">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="14a96-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="14a96-117">Requirements</span></span>



| <span data-ttu-id="14a96-118">需求</span><span class="sxs-lookup"><span data-stu-id="14a96-118">Requirement</span></span> | <span data-ttu-id="14a96-119">值</span><span class="sxs-lookup"><span data-stu-id="14a96-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14a96-120">標頭</span><span class="sxs-lookup"><span data-stu-id="14a96-120">Header</span></span><br/> | <dl> <span data-ttu-id="14a96-121"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="14a96-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14a96-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14a96-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a96-123">**結構**</span><span class="sxs-lookup"><span data-stu-id="14a96-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="14a96-124">**WMDRMNET \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="14a96-124">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





