---
title: 'DRM_INDIVIDUALIZATION_STATUS 列舉 (Drmexternals .h) '
description: 'DRM 的 \_ 個人化 \_ 狀態列舉類型會定義 drm 個人化的有效狀態。 |DRM_INDIVIDUALIZATION_STATUS 列舉 (Drmexternals .h) '
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- DRM_INDIVIDUALIZATION_STATUS 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d59a19c58c775ee22d78e17bc09add2825948e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104386407"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a><span data-ttu-id="1067d-106">DRM_INDIVIDUALIZATION_STATUS 列舉 (Drmexternals .h) </span><span class="sxs-lookup"><span data-stu-id="1067d-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="1067d-107">**Drm 的 \_ 個人化 \_ 狀態** 列舉類型會定義 drm [*個人化*](wmformat-glossary.md)的有效狀態。</span><span class="sxs-lookup"><span data-stu-id="1067d-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM [*individualization*](wmformat-glossary.md).</span></span> <span data-ttu-id="1067d-108">當應用程式透過呼叫 [**IWMDRMReader：：賦予**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize)來啟動「個人化」時，會透過呼叫 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 方法，將「個人化」要求的進度傳達給應用程式。</span><span class="sxs-lookup"><span data-stu-id="1067d-108">When an application initiates individualization with a call to [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), the progress of the individualization request is conveyed to the application through calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="1067d-109">「個人化」狀態訊息將會使用 \_ [**WMT \_ 狀態**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) 列舉類型的 WMT 賦予成員做為 *status* 參數。</span><span class="sxs-lookup"><span data-stu-id="1067d-109">Individualization status messages will all use the WMT\_INDIVIDUALIZE member of the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type as the *Status* parameter.</span></span> <span data-ttu-id="1067d-110">在 *pValue* 參數中，會將個人化的狀態傳遞給 **OnStatus** 。</span><span class="sxs-lookup"><span data-stu-id="1067d-110">The status of the individualization is passed to **OnStatus** in the *pValue* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="1067d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1067d-111">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="1067d-112">常數</span><span class="sxs-lookup"><span data-stu-id="1067d-112">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1067d-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**\_未定義 INDI**</span><span class="sxs-lookup"><span data-stu-id="1067d-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="1067d-114">這個值已保留供未來使用</span><span class="sxs-lookup"><span data-stu-id="1067d-114">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="1067d-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="1067d-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="1067d-116">表示個人化流程的開始。</span><span class="sxs-lookup"><span data-stu-id="1067d-116">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="1067d-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI \_ 成功**</span><span class="sxs-lookup"><span data-stu-id="1067d-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="1067d-118">表示已完成的個人化程式。</span><span class="sxs-lookup"><span data-stu-id="1067d-118">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="1067d-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="1067d-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="1067d-120">表示無法進行的個人化處理。</span><span class="sxs-lookup"><span data-stu-id="1067d-120">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="1067d-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="1067d-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="1067d-122">指出由於呼叫 [**IWMDRMReader：： CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization)而取消的個人化處理常式。</span><span class="sxs-lookup"><span data-stu-id="1067d-122">Indicates that the individualization process was canceled as the result of a call to [**IWMDRMReader::CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).</span></span>

</dd> <dt>

<span data-ttu-id="1067d-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI \_ 下載**</span><span class="sxs-lookup"><span data-stu-id="1067d-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="1067d-124">指出正在下載安全性升級。</span><span class="sxs-lookup"><span data-stu-id="1067d-124">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="1067d-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI \_ 安裝**</span><span class="sxs-lookup"><span data-stu-id="1067d-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="1067d-126">指出正在安裝安全性升級。</span><span class="sxs-lookup"><span data-stu-id="1067d-126">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1067d-127">備註</span><span class="sxs-lookup"><span data-stu-id="1067d-127">Remarks</span></span>

<span data-ttu-id="1067d-128">此列舉是由 [**WM \_ 賦予 \_ 狀態**](wm-individualize-status.md) 結構所使用。</span><span class="sxs-lookup"><span data-stu-id="1067d-128">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1067d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="1067d-129">Requirements</span></span>



| <span data-ttu-id="1067d-130">需求</span><span class="sxs-lookup"><span data-stu-id="1067d-130">Requirement</span></span> | <span data-ttu-id="1067d-131">值</span><span class="sxs-lookup"><span data-stu-id="1067d-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1067d-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1067d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1067d-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1067d-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1067d-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1067d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1067d-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1067d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1067d-136">版本</span><span class="sxs-lookup"><span data-stu-id="1067d-136">Version</span></span><br/>                  | <span data-ttu-id="1067d-137">Windows Media Format 7 SDK 或更新版本的 SDK</span><span class="sxs-lookup"><span data-stu-id="1067d-137">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="1067d-138">標頭</span><span class="sxs-lookup"><span data-stu-id="1067d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1067d-139"><dt>Drmexternals。h</dt></span><span class="sxs-lookup"><span data-stu-id="1067d-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1067d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1067d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1067d-141">**DRM \_ HTTP \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="1067d-141">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="1067d-142">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="1067d-142">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





