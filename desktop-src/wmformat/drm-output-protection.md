---
title: 'DRM_OUTPUT_PROTECTION 結構 (Wmdrmsdk .h) '
description: DRM \_ 輸出 \_ 保護結構會保存輸出保護技術的相關資訊。
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- DRM_OUTPUT_PROTECTION 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978748"
---
# <a name="drm_output_protection-structure"></a><span data-ttu-id="deda1-105">DRM \_ 輸出 \_ 保護結構</span><span class="sxs-lookup"><span data-stu-id="deda1-105">DRM\_OUTPUT\_PROTECTION structure</span></span>

<span data-ttu-id="deda1-106">**DRM \_ 輸出 \_ 保護** 結構會保存輸出保護技術的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="deda1-106">The **DRM\_OUTPUT\_PROTECTION** structure holds information about an output protection technology.</span></span>

## <a name="syntax"></a><span data-ttu-id="deda1-107">語法</span><span class="sxs-lookup"><span data-stu-id="deda1-107">Syntax</span></span>


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a><span data-ttu-id="deda1-108">成員</span><span class="sxs-lookup"><span data-stu-id="deda1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="deda1-109">**guidId**</span><span class="sxs-lookup"><span data-stu-id="deda1-109">**guidId**</span></span>
</dt> <dd>

<span data-ttu-id="deda1-110">識別輸出保護技術的 GUID。</span><span class="sxs-lookup"><span data-stu-id="deda1-110">GUID identifying the output protection technology.</span></span>

</dd> <dt>

<span data-ttu-id="deda1-111">**bConfigData**</span><span class="sxs-lookup"><span data-stu-id="deda1-111">**bConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="deda1-112">技術的設定資料。</span><span class="sxs-lookup"><span data-stu-id="deda1-112">Configuration data for the technology.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="deda1-113">備註</span><span class="sxs-lookup"><span data-stu-id="deda1-113">Remarks</span></span>

<span data-ttu-id="deda1-114">**DRM \_音訊 \_ 輸出 \_ 保護** 和 **drm \_ 影片 \_ 輸出 \_ 保護** 都會定義為 **typedef** 語句中的 **DRM \_ 輸出 \_ 保護**。</span><span class="sxs-lookup"><span data-stu-id="deda1-114">**DRM\_AUDIO\_OUTPUT\_PROTECTION** and **DRM\_VIDEO\_OUTPUT\_PROTECTION** are both defined as **DRM\_OUTPUT\_PROTECTION** in **typedef** statements.</span></span>

## <a name="requirements"></a><span data-ttu-id="deda1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="deda1-115">Requirements</span></span>



| <span data-ttu-id="deda1-116">需求</span><span class="sxs-lookup"><span data-stu-id="deda1-116">Requirement</span></span> | <span data-ttu-id="deda1-117">值</span><span class="sxs-lookup"><span data-stu-id="deda1-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="deda1-118">標頭</span><span class="sxs-lookup"><span data-stu-id="deda1-118">Header</span></span><br/> | <dl> <span data-ttu-id="deda1-119"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="deda1-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deda1-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="deda1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deda1-121">**DRM \_ 輸出 \_ 保護， \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="deda1-121">**DRM\_OUTPUT\_PROTECTION\_EX**</span></span>](drm-output-protection-ex.md)
</dt> <dt>

[<span data-ttu-id="deda1-122">**結構**</span><span class="sxs-lookup"><span data-stu-id="deda1-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





