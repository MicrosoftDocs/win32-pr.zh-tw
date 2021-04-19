---
title: 'WM_INDIVIDUALIZE_STATUS 結構 (Drmexternals .h) '
description: WM \_ 賦予 \_ 狀態結構會記錄個人化處理常式的狀態。
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- WM_INDIVIDUALIZE_STATUS 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec51fbdfecd407a68b3e168a82af449decce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991310"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a><span data-ttu-id="71baf-104">WM_INDIVIDUALIZE_STATUS 結構 (Drmexternals .h) </span><span class="sxs-lookup"><span data-stu-id="71baf-104">WM_INDIVIDUALIZE_STATUS structure (Drmexternals.h)</span></span>

<span data-ttu-id="71baf-105">**WM \_ 賦予 \_ 狀態** 結構會記錄 [*個人化*](wmformat-glossary.md)處理常式的狀態。</span><span class="sxs-lookup"><span data-stu-id="71baf-105">The **WM\_INDIVIDUALIZE\_STATUS** structure records the status of the [*individualization*](wmformat-glossary.md) process.</span></span>

## <a name="syntax"></a><span data-ttu-id="71baf-106">語法</span><span class="sxs-lookup"><span data-stu-id="71baf-106">Syntax</span></span>


```C++
typedef struct _WMIndividualizeStatus {
  HRESULT                      hr;
  DRM_INDIVIDUALIZATION_STATUS enIndiStatus;
  LPSTR                        pszIndiRespUrl;
  DWORD                        dwHTTPRequest;
  DRM_HTTP_STATUS              enHTTPStatus;
  DWORD                        dwHTTPReadProgress;
  DWORD                        dwHTTPReadTotal;
} WM_INDIVIDUALIZE_STATUS;
```



## <a name="members"></a><span data-ttu-id="71baf-107">成員</span><span class="sxs-lookup"><span data-stu-id="71baf-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="71baf-108">**小時**</span><span class="sxs-lookup"><span data-stu-id="71baf-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="71baf-109">**HRESULT** 傳回碼。</span><span class="sxs-lookup"><span data-stu-id="71baf-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="71baf-110">**enIndiStatus**</span><span class="sxs-lookup"><span data-stu-id="71baf-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="71baf-111">[**DRM 的 \_ 個人化 \_ 狀態**](drm-individualization-status.md)列舉類型的值。</span><span class="sxs-lookup"><span data-stu-id="71baf-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drm-individualization-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="71baf-112">**pszIndiRespUrl**</span><span class="sxs-lookup"><span data-stu-id="71baf-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="71baf-113">以 null 結束的字串指標，其中包含了「個人化回應 URL」。</span><span class="sxs-lookup"><span data-stu-id="71baf-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="71baf-114">**dwHTTPRequest**</span><span class="sxs-lookup"><span data-stu-id="71baf-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="71baf-115">**DWORD** ，指出已完成的個人化服務的 HTTP 往返次數。</span><span class="sxs-lookup"><span data-stu-id="71baf-115">**DWORD** that indicates the number of HTTP round trips to the individualization service that have been completed..</span></span>

</dd> <dt>

<span data-ttu-id="71baf-116">**enHTTPStatus**</span><span class="sxs-lookup"><span data-stu-id="71baf-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="71baf-117">[**DRM \_ HTTP \_ 狀態**](drm-http-status.md)列舉類型的值。</span><span class="sxs-lookup"><span data-stu-id="71baf-117">Value from the [**DRM\_HTTP\_STATUS**](drm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="71baf-118">**dwHTTPReadProgress**</span><span class="sxs-lookup"><span data-stu-id="71baf-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="71baf-119">**DWORD** ，包含到現在為止下載的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="71baf-119">**DWORD** containing the number of bytes downloaded until now..</span></span>

</dd> <dt>

<span data-ttu-id="71baf-120">**dwHTTPReadTotal**</span><span class="sxs-lookup"><span data-stu-id="71baf-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="71baf-121">**DWORD** ，包含要下載的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="71baf-121">**DWORD** containing the total number of bytes to be downloaded.</span></span> <span data-ttu-id="71baf-122">您可以使用此值和 **dwHTTPReadProgress** 來顯示使用者介面，指出已完成的下載數量，以及剩餘的時間。</span><span class="sxs-lookup"><span data-stu-id="71baf-122">Use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71baf-123">備註</span><span class="sxs-lookup"><span data-stu-id="71baf-123">Remarks</span></span>

<span data-ttu-id="71baf-124">當事件等於 WMT 賦予時，DRM 執行時間元件會填入此結構，並將其傳送至應用程式 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)方法的 *pValue* 參數中的應用程式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="71baf-124">This structure is filled in by the DRM run-time components and is sent to applications in the *pValue* parameter of the applications [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method when the event equals WMT\_INDIVIDUALIZE.</span></span> <span data-ttu-id="71baf-125">應用程式會在下載過程中多次收到此事件。</span><span class="sxs-lookup"><span data-stu-id="71baf-125">The application receives this event multiple times during the download process.</span></span>

## <a name="requirements"></a><span data-ttu-id="71baf-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="71baf-126">Requirements</span></span>



| <span data-ttu-id="71baf-127">需求</span><span class="sxs-lookup"><span data-stu-id="71baf-127">Requirement</span></span> | <span data-ttu-id="71baf-128">值</span><span class="sxs-lookup"><span data-stu-id="71baf-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="71baf-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71baf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="71baf-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71baf-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="71baf-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71baf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="71baf-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71baf-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="71baf-133">版本</span><span class="sxs-lookup"><span data-stu-id="71baf-133">Version</span></span><br/>                  | <span data-ttu-id="71baf-134">Windows Media Format 7 SDK 或更新版本的 SDK</span><span class="sxs-lookup"><span data-stu-id="71baf-134">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="71baf-135">標頭</span><span class="sxs-lookup"><span data-stu-id="71baf-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="71baf-136"><dt>Drmexternals。h</dt></span><span class="sxs-lookup"><span data-stu-id="71baf-136"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71baf-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71baf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71baf-138">**DRM \_ HTTP \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="71baf-138">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="71baf-139">**結構**</span><span class="sxs-lookup"><span data-stu-id="71baf-139">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





