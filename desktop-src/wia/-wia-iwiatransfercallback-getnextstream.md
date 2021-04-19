---
description: 取得指定之專案的新資料流程。
ms.assetid: fe25843c-2051-42fe-8737-eea39f6aeab9
title: 'IWiaTransferCallback：： GetNextStream 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.GetNextStream
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: fb2e92c9cade1dfd48efc3051b617997bf8473e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967144"
---
# <a name="iwiatransfercallbackgetnextstream-method"></a><span data-ttu-id="90aed-103">IWiaTransferCallback：： GetNextStream 方法</span><span class="sxs-lookup"><span data-stu-id="90aed-103">IWiaTransferCallback::GetNextStream method</span></span>

<span data-ttu-id="90aed-104">取得指定之專案的新資料流程。</span><span class="sxs-lookup"><span data-stu-id="90aed-104">Gets a new stream for the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="90aed-105">語法</span><span class="sxs-lookup"><span data-stu-id="90aed-105">Syntax</span></span>


```C++
HRESULT GetNextStream(
  [in]  LONG    lFlags,
  [in]  BSTR    bstrItemName,
  [in]  BSTR    bstrFullItemName,
  [out] IStream **ppDestination
);
```



## <a name="parameters"></a><span data-ttu-id="90aed-106">參數</span><span class="sxs-lookup"><span data-stu-id="90aed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90aed-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90aed-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90aed-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="90aed-108">Type: **LONG**</span></span>

<span data-ttu-id="90aed-109">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="90aed-109">Currently unused.</span></span> <span data-ttu-id="90aed-110">應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="90aed-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="90aed-111">*bstrItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90aed-111">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90aed-112">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="90aed-112">Type: **BSTR**</span></span>

<span data-ttu-id="90aed-113">指定要為其建立資料流程的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="90aed-113">Specifies the name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="90aed-114">*bstrFullItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90aed-114">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90aed-115">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="90aed-115">Type: **BSTR**</span></span>

<span data-ttu-id="90aed-116">指定要為其建立資料流程之專案的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="90aed-116">Specifies the full name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="90aed-117">*ppDestination* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="90aed-117">*ppDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90aed-118">類型： **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span><span class="sxs-lookup"><span data-stu-id="90aed-118">Type: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span></span>

<span data-ttu-id="90aed-119">接收新 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 物件之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="90aed-119">Receives the address of a pointer to the new [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90aed-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="90aed-120">Return value</span></span>

<span data-ttu-id="90aed-121">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="90aed-121">Type: **HRESULT**</span></span>

<span data-ttu-id="90aed-122">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="90aed-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="90aed-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="90aed-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="90aed-124">備註</span><span class="sxs-lookup"><span data-stu-id="90aed-124">Remarks</span></span>

<span data-ttu-id="90aed-125">當此方法是由影像處理篩選器所執行時，Windows 映像取得 (WIA) 2.0 迷你驅動程式會在映射取得期間呼叫它，以從用戶端取得目的地串流。</span><span class="sxs-lookup"><span data-stu-id="90aed-125">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to get the destination stream from the client.</span></span>

<span data-ttu-id="90aed-126">篩選準則的 **IWiaTransferCallback：： GetNextStream** 必須委派給應用程式的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="90aed-126">A filter's **IWiaTransferCallback::GetNextStream** must delegate to the application's callback method.</span></span> <span data-ttu-id="90aed-127">此篩選器會使用應用程式回呼的 **IWiaTransferCallback：： GetNextStream** 執行所傳回的資料流程，建立它自己的串流，以傳回到 WIA 2.0 服務。</span><span class="sxs-lookup"><span data-stu-id="90aed-127">The filter uses the stream returned by the application callback's **IWiaTransferCallback::GetNextStream** implementation to create its own stream that it passes back to the WIA 2.0 service.</span></span> <span data-ttu-id="90aed-128">篩選會在篩選的資料流程呼叫 [IStream：： Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) 方法時完成。</span><span class="sxs-lookup"><span data-stu-id="90aed-128">The filtering is done when the filter's stream calls the [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method.</span></span>

<span data-ttu-id="90aed-129">篩選的資料流程無法在每次寫入時，對寫入它的位元組數目做出任何假設，因為未篩選的影像資料可能來自 WIA 2.0 Preview 元件，而不是驅動程式。</span><span class="sxs-lookup"><span data-stu-id="90aed-129">The filter's stream cannot make any assumptions on the number of bytes that are written to it on each write, since the unfiltered image data may come from the WIA 2.0 Preview Component rather than the driver.</span></span> <span data-ttu-id="90aed-130">WIA 2.0 Preview 元件一律會將整個未篩選的影像資料寫入篩選的資料流程中一次，這表示篩選的資料流程有一個寫入其中的來源。</span><span class="sxs-lookup"><span data-stu-id="90aed-130">The WIA 2.0 Preview Component always writes the whole unfiltered image data into the filter's stream only once, which means that the filter's stream has one source writing into it.</span></span> <span data-ttu-id="90aed-131">如果驅動程式和預覽元件都寫入篩選器的資料流程，則篩選的資料流程無法假設它將會在第一次呼叫 [IStream：： write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) 時收到完整標頭，不過它的對應驅動程式一律會先在一個寫入中寫入標頭資料。</span><span class="sxs-lookup"><span data-stu-id="90aed-131">If both the driver and the preview component write into the filter's stream, the filter's stream cannot assume, for example, that it will receive the full header the first time [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) is called although its corresponding driver always writes the header data first in one write.</span></span> <span data-ttu-id="90aed-132">也不能假設後續的寫入只包含一條掃描行。</span><span class="sxs-lookup"><span data-stu-id="90aed-132">Nor can it assume that a subsequent write contains exactly one scan line.</span></span> <span data-ttu-id="90aed-133">因此，篩選資料流程可能必須計算寫入的位元組數目，以判斷影像資料的開始位置。</span><span class="sxs-lookup"><span data-stu-id="90aed-133">So the filtering stream may have to count the number of bytes written to it to determine, for example, where the image data starts.</span></span>

<span data-ttu-id="90aed-134">影像處理篩選器的 **IWiaTransferCallback：： GetNextStream** 實作為其影像處理所需的屬性（從取得影像的專案）。</span><span class="sxs-lookup"><span data-stu-id="90aed-134">The image processing filter's **IWiaTransferCallback::GetNextStream** implementation should read the properties needed for its image processing from the item for which the image is being acquired.</span></span> <span data-ttu-id="90aed-135">篩選不會直接從傳遞至 [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md)的 *pWiaItem2* 讀取屬性。</span><span class="sxs-lookup"><span data-stu-id="90aed-135">The filter does not read the properties directly from the *pWiaItem2* passed into [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span> <span data-ttu-id="90aed-136">相反地，篩選準則必須在此 WIA 2.0 專案上呼叫 [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) ，才能取得實際的 WIA 2.0 專案。</span><span class="sxs-lookup"><span data-stu-id="90aed-136">Instead the filter must call [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) on this WIA 2.0 item to obtain the actual WIA 2.0 item.</span></span> <span data-ttu-id="90aed-137">這是因為所取得的映射實際上可能是 *pWiaItem2* 的子專案。</span><span class="sxs-lookup"><span data-stu-id="90aed-137">The reason for this is that the image being acquired may actually be a child item of *pWiaItem2*.</span></span> <span data-ttu-id="90aed-138">例如，取得資料夾時，篩選器會使用 *pWiaItem2* 取得 **IWiaTransferCallback：： (GetNextStream** 中 *pWiaItem2* 的子專案。取得資料夾時，驅動程式會傳回 *pWiaItem2*) 的子專案所代表的影像。</span><span class="sxs-lookup"><span data-stu-id="90aed-138">For example, during a folder acquisition the filter uses *pWiaItem2* to obtain *pWiaItem2*'s child items in **IWiaTransferCallback::GetNextStream** (during a folder acquisition the driver returns the images represented by the child items of *pWiaItem2*).</span></span> <span data-ttu-id="90aed-139">當 WIA 2.0 Preview 元件呼叫傳遞子 WIA 2.0 專案的影像處理篩選準則時，也是如此。</span><span class="sxs-lookup"><span data-stu-id="90aed-139">The same is true when the WIA 2.0 Preview Component calls into the image processing filter passing a child WIA 2.0 item.</span></span>

## <a name="requirements"></a><span data-ttu-id="90aed-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="90aed-140">Requirements</span></span>



| <span data-ttu-id="90aed-141">需求</span><span class="sxs-lookup"><span data-stu-id="90aed-141">Requirement</span></span> | <span data-ttu-id="90aed-142">值</span><span class="sxs-lookup"><span data-stu-id="90aed-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90aed-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90aed-143">Minimum supported client</span></span><br/> | <span data-ttu-id="90aed-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90aed-144">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="90aed-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90aed-145">Minimum supported server</span></span><br/> | <span data-ttu-id="90aed-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90aed-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="90aed-147">標頭</span><span class="sxs-lookup"><span data-stu-id="90aed-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="90aed-148"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="90aed-148"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="90aed-149">Idl</span><span class="sxs-lookup"><span data-stu-id="90aed-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90aed-150"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="90aed-150"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="90aed-151">程式庫</span><span class="sxs-lookup"><span data-stu-id="90aed-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="90aed-152"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="90aed-152"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
