---
description: 初始化篩選。 在每個映射下載之前，Windows 映像取得 (WIA) 2.0 中呼叫。
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'IWiaImageFilter：： InitializeFilter 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a113c9493128a634ce61ccf7c0362bf7a9767f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974689"
---
# <a name="iwiaimagefilterinitializefilter-method"></a><span data-ttu-id="40a40-104">IWiaImageFilter：： InitializeFilter 方法</span><span class="sxs-lookup"><span data-stu-id="40a40-104">IWiaImageFilter::InitializeFilter method</span></span>

<span data-ttu-id="40a40-105">初始化篩選。</span><span class="sxs-lookup"><span data-stu-id="40a40-105">Initializes the filter.</span></span> <span data-ttu-id="40a40-106">在每個映射下載之前，Windows 映像取得 (WIA) 2.0 中呼叫。</span><span class="sxs-lookup"><span data-stu-id="40a40-106">Called by Windows Image Acquisition (WIA) 2.0 before each image download.</span></span>

## <a name="syntax"></a><span data-ttu-id="40a40-107">語法</span><span class="sxs-lookup"><span data-stu-id="40a40-107">Syntax</span></span>


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="40a40-108">參數</span><span class="sxs-lookup"><span data-stu-id="40a40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40a40-109">*pWiaItem2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40a40-109">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40a40-110">類型： \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="40a40-110">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="40a40-111">指定代表預覽影像之 [_ *IWiaItem2* \*](-wia-iwiaitem2.md)專案的指標。</span><span class="sxs-lookup"><span data-stu-id="40a40-111">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item that represents the preview image.</span></span>

</dd> <dt>

<span data-ttu-id="40a40-112">*pWiaTransferCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40a40-112">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40a40-113">類型： \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="40a40-113">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="40a40-114">指定應用程式 [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="40a40-114">Specifies a pointer to the application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40a40-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="40a40-115">Return value</span></span>

<span data-ttu-id="40a40-116">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="40a40-116">Type: **HRESULT**</span></span>

<span data-ttu-id="40a40-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="40a40-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="40a40-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="40a40-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="40a40-119">備註</span><span class="sxs-lookup"><span data-stu-id="40a40-119">Remarks</span></span>

<span data-ttu-id="40a40-120">當應用程式呼叫「 [**下載**](-wia-iwiatransfer-download.md) 」時，以及當應用程式呼叫 WIA 2.0 Preview 元件的函式時，會呼叫這個方法 `GetNewPreview` 。</span><span class="sxs-lookup"><span data-stu-id="40a40-120">This method is called when an application calls [**Download**](-wia-iwiatransfer-download.md) and when an application calls the WIA 2.0 Preview Component's `GetNewPreview` function.</span></span> <span data-ttu-id="40a40-121">**IWiaImageFilter：： InitializeFilter** 會儲存 *pWiaItem2* 和 *pWiaTransferCallback* 的參考，以傳遞至這些函數。</span><span class="sxs-lookup"><span data-stu-id="40a40-121">**IWiaImageFilter::InitializeFilter** stores the references to *pWiaItem2* and *pWiaTransferCallback* to pass into these functions.</span></span> <span data-ttu-id="40a40-122">這兩個介面指標應儲存為成員變數，且應該為每個介面呼叫 [IUnknown：： AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 。</span><span class="sxs-lookup"><span data-stu-id="40a40-122">These two interface pointers should be stored as member variables and [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) should be called for each.</span></span> <span data-ttu-id="40a40-123">在取得映射期間， [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) 和 [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) 的篩選器執行中也需要介面指標。</span><span class="sxs-lookup"><span data-stu-id="40a40-123">The interface pointers are also needed in the filter's implementation of [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) and [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) during image acquisition.</span></span>

## <a name="requirements"></a><span data-ttu-id="40a40-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="40a40-124">Requirements</span></span>



| <span data-ttu-id="40a40-125">需求</span><span class="sxs-lookup"><span data-stu-id="40a40-125">Requirement</span></span> | <span data-ttu-id="40a40-126">值</span><span class="sxs-lookup"><span data-stu-id="40a40-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40a40-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40a40-127">Minimum supported client</span></span><br/> | <span data-ttu-id="40a40-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40a40-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="40a40-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40a40-129">Minimum supported server</span></span><br/> | <span data-ttu-id="40a40-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40a40-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="40a40-131">標頭</span><span class="sxs-lookup"><span data-stu-id="40a40-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="40a40-132"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="40a40-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="40a40-133">Idl</span><span class="sxs-lookup"><span data-stu-id="40a40-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="40a40-134"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="40a40-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 
