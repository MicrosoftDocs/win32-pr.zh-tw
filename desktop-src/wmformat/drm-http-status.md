---
title: 'DRM_HTTP_STATUS 列舉 (Drmexternals .h) '
description: DRM \_ HTTP \_ 狀態列舉類型會定義 drm 要求的狀態範圍。
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- DRM_HTTP_STATUS 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d61803cab6cb80932402e429e77228a1611fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968978"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a><span data-ttu-id="6c064-105">DRM_HTTP_STATUS 列舉 (Drmexternals .h) </span><span class="sxs-lookup"><span data-stu-id="6c064-105">DRM_HTTP_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="6c064-106">**Drm \_ HTTP \_ 狀態** 列舉類型會定義 [*drm*](wmformat-glossary.md)要求的狀態範圍。</span><span class="sxs-lookup"><span data-stu-id="6c064-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of states for a [*DRM*](wmformat-glossary.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c064-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c064-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="6c064-108">常數</span><span class="sxs-lookup"><span data-stu-id="6c064-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6c064-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP \_ NOTINITIATED**</span><span class="sxs-lookup"><span data-stu-id="6c064-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="6c064-110">尚未起始 HTTP 作業。</span><span class="sxs-lookup"><span data-stu-id="6c064-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="6c064-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="6c064-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="6c064-112">正在建立連接。</span><span class="sxs-lookup"><span data-stu-id="6c064-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="6c064-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="6c064-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="6c064-114">正在要求資料。</span><span class="sxs-lookup"><span data-stu-id="6c064-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="6c064-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP \_ 接收**</span><span class="sxs-lookup"><span data-stu-id="6c064-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="6c064-116">正在接收資料。</span><span class="sxs-lookup"><span data-stu-id="6c064-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="6c064-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ 已完成**</span><span class="sxs-lookup"><span data-stu-id="6c064-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="6c064-118">HTTP 作業已完成。</span><span class="sxs-lookup"><span data-stu-id="6c064-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c064-119">備註</span><span class="sxs-lookup"><span data-stu-id="6c064-119">Remarks</span></span>

<span data-ttu-id="6c064-120">此列舉是由 [**WM \_ 賦予 \_ 狀態**](wm-individualize-status.md) 結構所使用。</span><span class="sxs-lookup"><span data-stu-id="6c064-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c064-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c064-121">Requirements</span></span>



| <span data-ttu-id="6c064-122">需求</span><span class="sxs-lookup"><span data-stu-id="6c064-122">Requirement</span></span> | <span data-ttu-id="6c064-123">值</span><span class="sxs-lookup"><span data-stu-id="6c064-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c064-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c064-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c064-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c064-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6c064-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c064-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c064-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c064-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6c064-128">版本</span><span class="sxs-lookup"><span data-stu-id="6c064-128">Version</span></span><br/>                  | <span data-ttu-id="6c064-129">Windows Media Format 7 SDK 或更新版本的 SDK</span><span class="sxs-lookup"><span data-stu-id="6c064-129">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="6c064-130">標頭</span><span class="sxs-lookup"><span data-stu-id="6c064-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c064-131"><dt>Drmexternals。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c064-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c064-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c064-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c064-133">**DRM 的 \_ 個人化 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="6c064-133">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drm-individualization-status.md)
</dt> <dt>

[<span data-ttu-id="6c064-134">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="6c064-134">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





