---
description: 篩選預覽影像。
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: 'IWiaImageFilter：： FilterPreviewImage 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 882aaf0d131ae6fe062c00c0181e2f913a0e1bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970233"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a><span data-ttu-id="f509b-103">IWiaImageFilter：： FilterPreviewImage 方法</span><span class="sxs-lookup"><span data-stu-id="f509b-103">IWiaImageFilter::FilterPreviewImage method</span></span>

<span data-ttu-id="f509b-104">篩選預覽影像。</span><span class="sxs-lookup"><span data-stu-id="f509b-104">Filters the preview image.</span></span>

## <a name="syntax"></a><span data-ttu-id="f509b-105">語法</span><span class="sxs-lookup"><span data-stu-id="f509b-105">Syntax</span></span>


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a><span data-ttu-id="f509b-106">參數</span><span class="sxs-lookup"><span data-stu-id="f509b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f509b-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f509b-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f509b-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="f509b-108">Type: **LONG**</span></span>

<span data-ttu-id="f509b-109">未使用。</span><span class="sxs-lookup"><span data-stu-id="f509b-109">Not used.</span></span> <span data-ttu-id="f509b-110">設定為0。</span><span class="sxs-lookup"><span data-stu-id="f509b-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="f509b-111">*pWiaChildItem2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f509b-111">*pWiaChildItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f509b-112">類型： \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="f509b-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="f509b-113">處理的專案。</span><span class="sxs-lookup"><span data-stu-id="f509b-113">The item that is processed.</span></span>

</dd> <dt>

<span data-ttu-id="f509b-114">_InputImageExtents \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f509b-114">_InputImageExtents\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f509b-115">類型： **RECT**</span><span class="sxs-lookup"><span data-stu-id="f509b-115">Type: **RECT**</span></span>

<span data-ttu-id="f509b-116">座標 (在預覽元件內部快取之影像的實體取得區域) 。</span><span class="sxs-lookup"><span data-stu-id="f509b-116">The coordinates (on the physical acquisition area) of the image that the preview component caches internally.</span></span>

</dd> <dt>

<span data-ttu-id="f509b-117">*pInputStream* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f509b-117">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f509b-118">類型： \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="f509b-118">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="f509b-119">已篩選之快取影像資料的 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="f509b-119">A pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) interface for the cached image data that is filtered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f509b-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="f509b-120">Return value</span></span>

<span data-ttu-id="f509b-121">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f509b-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f509b-122">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f509b-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f509b-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f509b-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f509b-124">備註</span><span class="sxs-lookup"><span data-stu-id="f509b-124">Remarks</span></span>

<span data-ttu-id="f509b-125">請勿直接從您的應用程式呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f509b-125">Do not call this method directly from your application.</span></span>

<span data-ttu-id="f509b-126">*pWiaChildItem2* 必須是傳遞至 [**IWiaImageFilter：： InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md)之 *pWiaItem2* 的子專案。</span><span class="sxs-lookup"><span data-stu-id="f509b-126">*pWiaChildItem2* must be a child item of the *pWiaItem2* that was passed into [**IWiaImageFilter::InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span>

<span data-ttu-id="f509b-127">*InputImageExtents* 是必要的，因為影像處理篩選器會負責從透過 *pInputStream* 傳入的影像資料中，剪下 *pWiaChildItem2* 所代表的影像區域。</span><span class="sxs-lookup"><span data-stu-id="f509b-127">*InputImageExtents* is needed because the image processing filter is responsible for cutting out the image area that *pWiaChildItem2* represents from the image data passed in through *pInputStream*.</span></span>

<span data-ttu-id="f509b-128">應用程式必須確定 *pWiaChildItem2* 具有相同的影像格式 (WIA \_ IPA \_ 格式) 、解析度 (WIA \_ ips \_ XRES 和 WIA \_ IP \_ YRES) 和位深度 (wia \_ IPA \_ 深度) ，因為 *pWiaItem2* 已傳遞至 [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md)。</span><span class="sxs-lookup"><span data-stu-id="f509b-128">An application must ensure that *pWiaChildItem2* has the same image format (WIA\_IPA\_FORMAT), resolution (WIA\_IPS\_XRES and WIA\_IPS\_YRES) and bit depth (WIA\_IPA\_DEPTH) as *pWiaItem2* had when it was passed into [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f509b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="f509b-129">Requirements</span></span>



| <span data-ttu-id="f509b-130">需求</span><span class="sxs-lookup"><span data-stu-id="f509b-130">Requirement</span></span> | <span data-ttu-id="f509b-131">值</span><span class="sxs-lookup"><span data-stu-id="f509b-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f509b-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f509b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f509b-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f509b-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f509b-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f509b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f509b-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f509b-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f509b-136">標頭</span><span class="sxs-lookup"><span data-stu-id="f509b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f509b-137"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="f509b-137"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="f509b-138">Idl</span><span class="sxs-lookup"><span data-stu-id="f509b-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f509b-139"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f509b-139"><dt>Wia.idl</dt></span></span> </dl> |



 

 
