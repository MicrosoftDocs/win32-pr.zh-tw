---
title: 'DRM_HTTP_STATUS 列舉 (Wmdrmsdk .h) '
description: DRM \_ HTTP \_ 狀態列舉類型會定義 drm 要求的 HTTP 狀態範圍。
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- DRM_HTTP_STATUS 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c5a40af45fd573f7f5033b9be3b037079cb30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001620"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="b21d4-105">DRM_HTTP_STATUS 列舉 (Wmdrmsdk .h) </span><span class="sxs-lookup"><span data-stu-id="b21d4-105">DRM_HTTP_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="b21d4-106">**Drm \_ HTTP \_ 狀態** 列舉類型會定義 drm 要求的 HTTP 狀態範圍。</span><span class="sxs-lookup"><span data-stu-id="b21d4-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of HTTP states for a DRM request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b21d4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b21d4-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="b21d4-108">常數</span><span class="sxs-lookup"><span data-stu-id="b21d4-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b21d4-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP \_ NOTINITIATED**</span><span class="sxs-lookup"><span data-stu-id="b21d4-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="b21d4-110">尚未起始 HTTP 作業。</span><span class="sxs-lookup"><span data-stu-id="b21d4-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="b21d4-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="b21d4-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="b21d4-112">正在建立連接。</span><span class="sxs-lookup"><span data-stu-id="b21d4-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="b21d4-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="b21d4-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="b21d4-114">正在要求資料。</span><span class="sxs-lookup"><span data-stu-id="b21d4-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="b21d4-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP \_ 接收**</span><span class="sxs-lookup"><span data-stu-id="b21d4-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="b21d4-116">正在接收資料。</span><span class="sxs-lookup"><span data-stu-id="b21d4-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="b21d4-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ 已完成**</span><span class="sxs-lookup"><span data-stu-id="b21d4-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="b21d4-118">HTTP 作業已完成。</span><span class="sxs-lookup"><span data-stu-id="b21d4-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b21d4-119">備註</span><span class="sxs-lookup"><span data-stu-id="b21d4-119">Remarks</span></span>

<span data-ttu-id="b21d4-120">此列舉是由 [**WM \_ 賦予 \_ 狀態**](drmwm-individualize-status.md) 結構所使用。</span><span class="sxs-lookup"><span data-stu-id="b21d4-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b21d4-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b21d4-121">Requirements</span></span>



| <span data-ttu-id="b21d4-122">需求</span><span class="sxs-lookup"><span data-stu-id="b21d4-122">Requirement</span></span> | <span data-ttu-id="b21d4-123">值</span><span class="sxs-lookup"><span data-stu-id="b21d4-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b21d4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b21d4-124">Header</span></span><br/> | <dl> <span data-ttu-id="b21d4-125"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="b21d4-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b21d4-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b21d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b21d4-127">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="b21d4-127">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





