---
title: 'WM_INDIVIDUALIZE_STATUS 結構 (Wmdrmsdk .h) '
description: WM \_ 賦予 \_ 狀態結構會保存有關暫止的個人化程式的資訊。
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- WM_INDIVIDUALIZE_STATUS 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef7617fe6dcddf3397ab1a123132e843f0b1461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997763"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a><span data-ttu-id="d9a76-104">WM_INDIVIDUALIZE_STATUS 結構 (Wmdrmsdk .h) </span><span class="sxs-lookup"><span data-stu-id="d9a76-104">WM_INDIVIDUALIZE_STATUS structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="d9a76-105">**WM \_ 賦予 \_ 狀態** 結構會保存有關暫止的個人化程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="d9a76-105">The **WM\_INDIVIDUALIZE\_STATUS** structure holds information about a pending individualization process.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a76-106">語法</span><span class="sxs-lookup"><span data-stu-id="d9a76-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="d9a76-107">成員</span><span class="sxs-lookup"><span data-stu-id="d9a76-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d9a76-108">**小時**</span><span class="sxs-lookup"><span data-stu-id="d9a76-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="d9a76-109">**HRESULT** 傳回碼。</span><span class="sxs-lookup"><span data-stu-id="d9a76-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="d9a76-110">**enIndiStatus**</span><span class="sxs-lookup"><span data-stu-id="d9a76-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="d9a76-111">[**DRM [ \_ \_ 狀態**](drmdrm-individualization-status.md)] 列舉類型中的值，指出目前的個人化處理狀態。</span><span class="sxs-lookup"><span data-stu-id="d9a76-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drmdrm-individualization-status.md) enumeration type that indicates the current status of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="d9a76-112">**pszIndiRespUrl**</span><span class="sxs-lookup"><span data-stu-id="d9a76-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="d9a76-113">以 null 結束的字串指標，其中包含了「個人化回應 URL」。</span><span class="sxs-lookup"><span data-stu-id="d9a76-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="d9a76-114">**dwHTTPRequest**</span><span class="sxs-lookup"><span data-stu-id="d9a76-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="d9a76-115">已完成的個人化服務的 HTTP 往返次數。</span><span class="sxs-lookup"><span data-stu-id="d9a76-115">The number of HTTP round trips to the individualization service that have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="d9a76-116">**enHTTPStatus**</span><span class="sxs-lookup"><span data-stu-id="d9a76-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="d9a76-117">[**DRM \_ HTTP \_ 狀態**](drmdrm-http-status.md)列舉類型的值。</span><span class="sxs-lookup"><span data-stu-id="d9a76-117">Value from the [**DRM\_HTTP\_STATUS**](drmdrm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="d9a76-118">**dwHTTPReadProgress**</span><span class="sxs-lookup"><span data-stu-id="d9a76-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="d9a76-119">已下載的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="d9a76-119">The number of bytes downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="d9a76-120">**dwHTTPReadTotal**</span><span class="sxs-lookup"><span data-stu-id="d9a76-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="d9a76-121">要下載的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="d9a76-121">The total number of bytes to be downloaded.</span></span> <span data-ttu-id="d9a76-122">您可以使用此值和 **dwHTTPReadProgress** 來顯示使用者介面，指出已完成的下載數量，以及剩餘的時間。</span><span class="sxs-lookup"><span data-stu-id="d9a76-122">You can use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9a76-123">備註</span><span class="sxs-lookup"><span data-stu-id="d9a76-123">Remarks</span></span>

<span data-ttu-id="d9a76-124">當您呼叫 [**IWMDRMIndividualizationStatus：： GetStatus**](iwmdrmindividualizationstatus-getstatus.md) 方法時，就會收到此結構。</span><span class="sxs-lookup"><span data-stu-id="d9a76-124">This structure is received when you call the [**IWMDRMIndividualizationStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md) method.</span></span> <span data-ttu-id="d9a76-125">它包含呼叫時暫止的個人化處理常式的狀態。</span><span class="sxs-lookup"><span data-stu-id="d9a76-125">It contains the status of the pending individualization process at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9a76-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9a76-126">Requirements</span></span>



| <span data-ttu-id="d9a76-127">需求</span><span class="sxs-lookup"><span data-stu-id="d9a76-127">Requirement</span></span> | <span data-ttu-id="d9a76-128">值</span><span class="sxs-lookup"><span data-stu-id="d9a76-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a76-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d9a76-129">Header</span></span><br/> | <dl> <span data-ttu-id="d9a76-130"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="d9a76-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9a76-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9a76-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a76-132">**結構**</span><span class="sxs-lookup"><span data-stu-id="d9a76-132">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





