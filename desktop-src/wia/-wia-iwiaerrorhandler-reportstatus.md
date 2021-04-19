---
description: 處理影像資料傳輸期間的狀態和錯誤訊息，並將其顯示給使用者。
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: 'IWiaErrorHandler：： ReportStatus 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 30a082502d4c7bc5b789fd1ec19fdb76f63d8fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974284"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a><span data-ttu-id="ea384-103">IWiaErrorHandler：： ReportStatus 方法</span><span class="sxs-lookup"><span data-stu-id="ea384-103">IWiaErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="ea384-104">處理影像資料傳輸期間的狀態和錯誤訊息，並將其顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="ea384-104">Handles status and error messages during image data transfers and displays them to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea384-105">語法</span><span class="sxs-lookup"><span data-stu-id="ea384-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] HWND     hwndParent,
  [in] IUnknown *punkItem,
  [in] HRESULT  hrStatus,
  [in] LONG     cbResLength,
  [in] BYTE     *pbData
);
```



## <a name="parameters"></a><span data-ttu-id="ea384-106">參數</span><span class="sxs-lookup"><span data-stu-id="ea384-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea384-107">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ea384-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea384-108">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="ea384-108">Type: **HWND**</span></span>

<span data-ttu-id="ea384-109">**HWND** ，也就是訊息視窗的父視窗。</span><span class="sxs-lookup"><span data-stu-id="ea384-109">**HWND** that is the parent window for the message window.</span></span>

</dd> <dt>

<span data-ttu-id="ea384-110">*punkItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ea384-110">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea384-111">類型： \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="ea384-111">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="ea384-112">要傳送之專案的 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="ea384-112">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the item being transferred.</span></span> <span data-ttu-id="ea384-113">此物件至少會執行 [_ *IWiaItem2* \*](-wia-iwiaitem2.md)和 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)。</span><span class="sxs-lookup"><span data-stu-id="ea384-113">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="ea384-114">*hrStatus* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ea384-114">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea384-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ea384-115">Type: **HRESULT**</span></span>

<span data-ttu-id="ea384-116">**HRESULT** ，這是 [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)所接收的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="ea384-116">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="ea384-117">*cbResLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ea384-117">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea384-118">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="ea384-118">Type: **LONG**</span></span>

<span data-ttu-id="ea384-119">**LONG** 是 *>pbdata* 所參考的資料大小。</span><span class="sxs-lookup"><span data-stu-id="ea384-119">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="ea384-120">*>pbdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ea384-120">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea384-121">類型： \**BYTE \** _</span><span class="sxs-lookup"><span data-stu-id="ea384-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="ea384-122">[_ *BandedDataCallback* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)所接收之資料緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="ea384-122">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea384-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea384-123">Return value</span></span>

<span data-ttu-id="ea384-124">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ea384-124">Type: **HRESULT**</span></span>

<span data-ttu-id="ea384-125">如果無法從復原錯誤，則傳回 *hrStatus* 。</span><span class="sxs-lookup"><span data-stu-id="ea384-125">Returns *hrStatus* if the error cannot be recovered from.</span></span> <span data-ttu-id="ea384-126">否則，它會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ea384-126">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="ea384-127">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ea384-127">Return code</span></span>                                                                             | <span data-ttu-id="ea384-128">Description</span><span class="sxs-lookup"><span data-stu-id="ea384-128">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ea384-129"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ea384-129"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ea384-130">已採取適當的動作來修正錯誤，而且可以繼續傳送。</span><span class="sxs-lookup"><span data-stu-id="ea384-130">The appropriate action was taken to correct the error and the transfer can continue.</span></span> <br/> |
| <dl> <span data-ttu-id="ea384-131"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="ea384-131"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ea384-132">未採取任何動作來處理使用者的錯誤或報告狀態。</span><span class="sxs-lookup"><span data-stu-id="ea384-132">No action was taken to handle the error or report status to the user.</span></span> <br/>                |
| <dl> <span data-ttu-id="ea384-133"><dt>**E \_ 中止**</dt></span><span class="sxs-lookup"><span data-stu-id="ea384-133"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="ea384-134">使用者選擇中止傳送以回應所顯示的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ea384-134">The user chose to abort the transfer in response to the displayed dialog box.</span></span> <br/>        |



 

## <a name="remarks"></a><span data-ttu-id="ea384-135">備註</span><span class="sxs-lookup"><span data-stu-id="ea384-135">Remarks</span></span>

<span data-ttu-id="ea384-136">Windows 映像取得 (WIA) 2.0 會在驅動程式將 **IT \_ MSG \_ 裝置 \_ 狀態** 消息傳送至 [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)時呼叫 **IWiaErrorHandler：： ReportStatus** 。</span><span class="sxs-lookup"><span data-stu-id="ea384-136">Windows Image Acquisition (WIA) 2.0 calls **IWiaErrorHandler::ReportStatus** when the driver sends an **IT\_MSG\_DEVICE\_STATUS** message to [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span> <span data-ttu-id="ea384-137">這個方法會處理訊息，並向使用者顯示狀態或錯誤的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ea384-137">This method handles the message and displays information to the user about the status or error.</span></span> <span data-ttu-id="ea384-138">如果訊息是關於錯誤，則方法可讓使用者選擇（可能的話），是否嘗試從錯誤中復原並繼續傳送或中止。</span><span class="sxs-lookup"><span data-stu-id="ea384-138">If the message is about an error, the method lets the user choose, if possible, whether to try to recover from the error and continue the transfer or to abort.</span></span>

<span data-ttu-id="ea384-139">*hrStatus* 設定為 WIA \_ 狀態 \_ 傳輸 \_ 開始，以通知處理常式已開始傳送。</span><span class="sxs-lookup"><span data-stu-id="ea384-139">*hrStatus* is set to WIA\_STATUS\_TRANSFER\_BEGIN to inform the handler a transfer has started.</span></span> <span data-ttu-id="ea384-140">當傳送完成時，它會設定為 WIA \_ 狀態 \_ 傳輸 \_ 結束。</span><span class="sxs-lookup"><span data-stu-id="ea384-140">It is set to WIA\_STATUS\_TRANSFER\_END when the transfer is complete.</span></span>

<span data-ttu-id="ea384-141">如果 *hrStatus* 為嚴重性 \_ 成功，則應允許使用者取消傳輸。</span><span class="sxs-lookup"><span data-stu-id="ea384-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea384-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea384-142">Requirements</span></span>



| <span data-ttu-id="ea384-143">需求</span><span class="sxs-lookup"><span data-stu-id="ea384-143">Requirement</span></span> | <span data-ttu-id="ea384-144">值</span><span class="sxs-lookup"><span data-stu-id="ea384-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea384-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea384-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ea384-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea384-146">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ea384-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea384-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ea384-148">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea384-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ea384-149">標頭</span><span class="sxs-lookup"><span data-stu-id="ea384-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea384-150"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="ea384-150"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="ea384-151">Idl</span><span class="sxs-lookup"><span data-stu-id="ea384-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea384-152"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea384-152"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="ea384-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="ea384-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea384-154"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea384-154"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
