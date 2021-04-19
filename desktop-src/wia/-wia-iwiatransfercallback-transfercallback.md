---
description: 提供傳輸期間的進度和其他通知。
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: 'IWiaTransferCallback：： TransferCallback 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.TransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: f1e2f939a7a3d768fc744c0603563b0a088e08f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972233"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a><span data-ttu-id="9a3eb-103">IWiaTransferCallback：： TransferCallback 方法</span><span class="sxs-lookup"><span data-stu-id="9a3eb-103">IWiaTransferCallback::TransferCallback method</span></span>

<span data-ttu-id="9a3eb-104">提供傳輸期間的進度和其他通知。</span><span class="sxs-lookup"><span data-stu-id="9a3eb-104">Provides progress and other notifications during a transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a3eb-105">語法</span><span class="sxs-lookup"><span data-stu-id="9a3eb-105">Syntax</span></span>


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a><span data-ttu-id="9a3eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="9a3eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a3eb-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a3eb-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a3eb-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="9a3eb-108">Type: **LONG**</span></span>

<span data-ttu-id="9a3eb-109">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="9a3eb-109">Currently unused.</span></span> <span data-ttu-id="9a3eb-110">應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="9a3eb-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="9a3eb-111">*pWiaTransferParams* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a3eb-111">*pWiaTransferParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a3eb-112">類型： \**[**WiaTransferParams**](-wia-wiatransferparams.md) \** _</span><span class="sxs-lookup"><span data-stu-id="9a3eb-112">Type: \**[**WiaTransferParams**](-wia-wiatransferparams.md)\** _</span></span>

<span data-ttu-id="9a3eb-113">指定 [_ *WiaTransferParams* \*](-wia-wiatransferparams.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9a3eb-113">Specifies a pointer to a [_ *WiaTransferParams*\*](-wia-wiatransferparams.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a3eb-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a3eb-114">Return value</span></span>

<span data-ttu-id="9a3eb-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9a3eb-115">Type: **HRESULT**</span></span>

<span data-ttu-id="9a3eb-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9a3eb-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a3eb-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9a3eb-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a3eb-118">備註</span><span class="sxs-lookup"><span data-stu-id="9a3eb-118">Remarks</span></span>

<span data-ttu-id="9a3eb-119">當此方法是由影像處理篩選器所執行時，Windows 映像取得 (WIA) 2.0 迷你驅動程式會在映射取得期間呼叫它，以將進度訊息傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="9a3eb-119">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to send progress messages back to the application.</span></span>

<span data-ttu-id="9a3eb-120">篩選準則的 **IWiaTransferCallback：： TransferCallback** 必須委派給應用程式回呼的 **IWiaTransferCallback：： TransferCallback** 方法。</span><span class="sxs-lookup"><span data-stu-id="9a3eb-120">A filter's **IWiaTransferCallback::TransferCallback** must delegate to the application callback's **IWiaTransferCallback::TransferCallback** method.</span></span> <span data-ttu-id="9a3eb-121">篩選資料流程通常會篩選傳遞給它的資料，並將篩選過的資料直接寫入應用程式提供的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9a3eb-121">Usually, the filter stream filters the data passed to it and writes the filtered data directly to the application provided stream.</span></span> <span data-ttu-id="9a3eb-122">當影像處理篩選在其 [IStream：： Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write)方法的呼叫之間儲存資料時，它也必須修改 [**WiaTransferParams**](-wia-wiatransferparams.md)結構中的 *lPercentComplete* 和 *ulBytesWrittenToCurrentStream* 值。</span><span class="sxs-lookup"><span data-stu-id="9a3eb-122">When image processing filter stores data between calls to its [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method, it must also modify the *lPercentComplete* and *ulBytesWrittenToCurrentStream* values in the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a3eb-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a3eb-123">Requirements</span></span>



| <span data-ttu-id="9a3eb-124">需求</span><span class="sxs-lookup"><span data-stu-id="9a3eb-124">Requirement</span></span> | <span data-ttu-id="9a3eb-125">值</span><span class="sxs-lookup"><span data-stu-id="9a3eb-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a3eb-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a3eb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9a3eb-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a3eb-127">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9a3eb-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a3eb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9a3eb-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a3eb-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9a3eb-130">標頭</span><span class="sxs-lookup"><span data-stu-id="9a3eb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a3eb-131"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="9a3eb-131"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="9a3eb-132">Idl</span><span class="sxs-lookup"><span data-stu-id="9a3eb-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a3eb-133"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a3eb-133"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="9a3eb-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="9a3eb-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a3eb-135"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a3eb-135"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
