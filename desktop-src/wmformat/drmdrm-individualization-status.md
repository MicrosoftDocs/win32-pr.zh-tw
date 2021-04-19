---
title: 'DRM_INDIVIDUALIZATION_STATUS 列舉 (Wmdrmsdk .h) '
description: 'DRM 的 \_ 個人化 \_ 狀態列舉類型會定義 drm 個人化的有效狀態。 |DRM_INDIVIDUALIZATION_STATUS 列舉 (Wmdrmsdk .h) '
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- DRM_INDIVIDUALIZATION_STATUS 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b395d3ad4271ccef9964f0d39c74a1e0ba158257
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999677"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="9fce5-106">DRM_INDIVIDUALIZATION_STATUS 列舉 (Wmdrmsdk .h) </span><span class="sxs-lookup"><span data-stu-id="9fce5-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="9fce5-107">**Drm 的 \_ 個人化 \_ 狀態** 列舉類型會定義 drm 個人化的有效狀態。</span><span class="sxs-lookup"><span data-stu-id="9fce5-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM individualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fce5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fce5-108">Syntax</span></span>


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a><span data-ttu-id="9fce5-109">常數</span><span class="sxs-lookup"><span data-stu-id="9fce5-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9fce5-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**\_未定義 INDI**</span><span class="sxs-lookup"><span data-stu-id="9fce5-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="9fce5-111">這個值已保留供未來使用</span><span class="sxs-lookup"><span data-stu-id="9fce5-111">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="9fce5-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="9fce5-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="9fce5-113">表示個人化流程的開始。</span><span class="sxs-lookup"><span data-stu-id="9fce5-113">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="9fce5-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI \_ 成功**</span><span class="sxs-lookup"><span data-stu-id="9fce5-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="9fce5-115">表示已完成的個人化程式。</span><span class="sxs-lookup"><span data-stu-id="9fce5-115">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="9fce5-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="9fce5-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="9fce5-117">表示無法進行的個人化處理。</span><span class="sxs-lookup"><span data-stu-id="9fce5-117">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="9fce5-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="9fce5-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="9fce5-119">表示應用程式已取消了「個人化」進程。</span><span class="sxs-lookup"><span data-stu-id="9fce5-119">Indicates that the individualization process was canceled by the application.</span></span>

</dd> <dt>

<span data-ttu-id="9fce5-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI \_ 下載**</span><span class="sxs-lookup"><span data-stu-id="9fce5-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="9fce5-121">指出正在下載安全性升級。</span><span class="sxs-lookup"><span data-stu-id="9fce5-121">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="9fce5-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI \_ 安裝**</span><span class="sxs-lookup"><span data-stu-id="9fce5-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="9fce5-123">指出正在安裝安全性升級。</span><span class="sxs-lookup"><span data-stu-id="9fce5-123">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fce5-124">備註</span><span class="sxs-lookup"><span data-stu-id="9fce5-124">Remarks</span></span>

<span data-ttu-id="9fce5-125">此列舉是由 [**WM \_ 賦予 \_ 狀態**](drmwm-individualize-status.md) 結構所使用。</span><span class="sxs-lookup"><span data-stu-id="9fce5-125">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fce5-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fce5-126">Requirements</span></span>



| <span data-ttu-id="9fce5-127">需求</span><span class="sxs-lookup"><span data-stu-id="9fce5-127">Requirement</span></span> | <span data-ttu-id="9fce5-128">值</span><span class="sxs-lookup"><span data-stu-id="9fce5-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fce5-129">標頭</span><span class="sxs-lookup"><span data-stu-id="9fce5-129">Header</span></span><br/> | <dl> <span data-ttu-id="9fce5-130"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="9fce5-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fce5-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fce5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fce5-132">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="9fce5-132">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





