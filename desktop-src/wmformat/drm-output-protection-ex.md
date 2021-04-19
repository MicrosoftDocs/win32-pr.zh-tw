---
title: 'DRM_OUTPUT_PROTECTION_EX 結構 (Wmdrmsdk .h) '
description: DRM \_ 輸出 \_ 保護的 \_ EX 結構會保存輸出保護技術的相關資訊。 此結構會藉 \_ \_ 由新增版本號碼來擴充 DRM 輸出保護。
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- DRM_OUTPUT_PROTECTION_EX 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001188"
---
# <a name="drm_output_protection_ex-structure"></a><span data-ttu-id="27b0d-106">DRM \_ 輸出 \_ 保護 \_ EX 結構</span><span class="sxs-lookup"><span data-stu-id="27b0d-106">DRM\_OUTPUT\_PROTECTION\_EX structure</span></span>

<span data-ttu-id="27b0d-107">**DRM \_ 輸出保護 \_ 的 \_ EX** 結構會保存輸出保護技術的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="27b0d-107">The **DRM\_OUTPUT\_PROTECTION\_EX** structure holds information about an output protection technology.</span></span> <span data-ttu-id="27b0d-108">此結構會藉由新增版本號碼來擴充 **DRM \_ 輸出 \_ 保護** 。</span><span class="sxs-lookup"><span data-stu-id="27b0d-108">This structure extends **DRM\_OUTPUT\_PROTECTION** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="27b0d-109">語法</span><span class="sxs-lookup"><span data-stu-id="27b0d-109">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="27b0d-110">成員</span><span class="sxs-lookup"><span data-stu-id="27b0d-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="27b0d-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="27b0d-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="27b0d-112">版本號碼。</span><span class="sxs-lookup"><span data-stu-id="27b0d-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="27b0d-113">**guidId**</span><span class="sxs-lookup"><span data-stu-id="27b0d-113">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="27b0d-114">識別輸出保護技術的 GUID。</span><span class="sxs-lookup"><span data-stu-id="27b0d-114">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="27b0d-115">**dwConfigData**</span><span class="sxs-lookup"><span data-stu-id="27b0d-115">**dwConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="27b0d-116">技術的設定資料。</span><span class="sxs-lookup"><span data-stu-id="27b0d-116">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27b0d-117">備註</span><span class="sxs-lookup"><span data-stu-id="27b0d-117">Remarks</span></span>

<span data-ttu-id="27b0d-118">**DRM \_音訊 \_ 輸出 \_ 保護 \_** （例如和 **drm \_ 影片 \_ 輸出 \_ 保護 \_** ）在 **typedef** 語句中定義為 **DRM \_ 輸出 \_ 保護**。</span><span class="sxs-lookup"><span data-stu-id="27b0d-118">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** and **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="27b0d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="27b0d-119">Requirements</span></span>



| <span data-ttu-id="27b0d-120">需求</span><span class="sxs-lookup"><span data-stu-id="27b0d-120">Requirement</span></span> | <span data-ttu-id="27b0d-121">值</span><span class="sxs-lookup"><span data-stu-id="27b0d-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27b0d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="27b0d-122">Header</span></span><br/> | <dl> <span data-ttu-id="27b0d-123"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="27b0d-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27b0d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27b0d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27b0d-125">**DRM \_ 輸出 \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="27b0d-125">**DRM\_OUTPUT\_PROTECTION**</span></span>](drm-output-protection.md)
</dt> <dt>

[<span data-ttu-id="27b0d-126">**結構**</span><span class="sxs-lookup"><span data-stu-id="27b0d-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





