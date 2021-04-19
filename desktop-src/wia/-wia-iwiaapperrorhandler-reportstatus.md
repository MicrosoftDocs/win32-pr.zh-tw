---
description: 處理影像資料傳輸期間的裝置狀態和錯誤訊息，並向使用者顯示訊息。
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: 'IWiaAppErrorHandler：： ReportStatus 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1285b5391014919d7108f207917b0c44c03fa360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971043"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a><span data-ttu-id="f04d7-103">IWiaAppErrorHandler：： ReportStatus 方法</span><span class="sxs-lookup"><span data-stu-id="f04d7-103">IWiaAppErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="f04d7-104">處理影像資料傳輸期間的裝置狀態和錯誤訊息，並向使用者顯示訊息。</span><span class="sxs-lookup"><span data-stu-id="f04d7-104">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="f04d7-105">語法</span><span class="sxs-lookup"><span data-stu-id="f04d7-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaItem2,
  [in] HRESULT   hrStatus,
  [in] LONG      lPercentComplete
);
```



## <a name="parameters"></a><span data-ttu-id="f04d7-106">參數</span><span class="sxs-lookup"><span data-stu-id="f04d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f04d7-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f04d7-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04d7-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="f04d7-108">Type: **LONG**</span></span>

<span data-ttu-id="f04d7-109">未使用。</span><span class="sxs-lookup"><span data-stu-id="f04d7-109">Not used.</span></span> <span data-ttu-id="f04d7-110">設定為0。</span><span class="sxs-lookup"><span data-stu-id="f04d7-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="f04d7-111">*pWiaItem2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f04d7-111">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04d7-112">類型： \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="f04d7-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="f04d7-113">要傳送之專案的指標。</span><span class="sxs-lookup"><span data-stu-id="f04d7-113">Pointer to the item being transferred.</span></span>

</dd> <dt>

<span data-ttu-id="f04d7-114">_hrStatus \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f04d7-114">_hrStatus\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04d7-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f04d7-115">Type: **HRESULT**</span></span>

<span data-ttu-id="f04d7-116">裝置狀態碼。</span><span class="sxs-lookup"><span data-stu-id="f04d7-116">Device status code.</span></span>

</dd> <dt>

<span data-ttu-id="f04d7-117">*lPercentComplete* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f04d7-117">*lPercentComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04d7-118">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="f04d7-118">Type: **LONG**</span></span>

<span data-ttu-id="f04d7-119">目前作業已完成的百分比。</span><span class="sxs-lookup"><span data-stu-id="f04d7-119">Percentage completed of current operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f04d7-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="f04d7-120">Return value</span></span>

<span data-ttu-id="f04d7-121">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f04d7-121">Type: **HRESULT**</span></span>

<span data-ttu-id="f04d7-122">如果不可能從錯誤復原，則會傳回 *hrStatus* 。</span><span class="sxs-lookup"><span data-stu-id="f04d7-122">Returns *hrStatus* if recovery from the error is not possible.</span></span> <span data-ttu-id="f04d7-123">否則，它會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f04d7-123">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="f04d7-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f04d7-124">Return code</span></span>                                                                                              | <span data-ttu-id="f04d7-125">Description</span><span class="sxs-lookup"><span data-stu-id="f04d7-125">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f04d7-126"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f04d7-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="f04d7-127">如果 *hrStatus* 是錯誤，則會採取適當的動作來更正錯誤，而且可以繼續傳送。</span><span class="sxs-lookup"><span data-stu-id="f04d7-127">If *hrStatus* is an error, the appropriate action was taken to correct the error, and the transfer can continue.</span></span> <span data-ttu-id="f04d7-128">如果 *hrStatus* 是參考資訊，使用者就會收到非強制回應對話方塊的通知，並選擇不要取消傳送。</span><span class="sxs-lookup"><span data-stu-id="f04d7-128">If *hrStatus* is informational, the user was informed with a modeless dialog box and chose not to cancel the transfer.</span></span><br/> |
| <dl> <span data-ttu-id="f04d7-129"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="f04d7-129"><dt>**S\_FALSE**</dt></span></span> </dl>                  | <span data-ttu-id="f04d7-130">使用者取消了從錯誤處理常式非強制回應對話方塊的傳送。</span><span class="sxs-lookup"><span data-stu-id="f04d7-130">The user cancelled the transfer from the error handler modeless dialog box.</span></span> <span data-ttu-id="f04d7-131">無論 *hrStatus* 為何，都可以在任何時間點傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="f04d7-131">This value can be returned at any point no matter what *hrStatus* is.</span></span> <br/>                                                                                      |
| <dl> <span data-ttu-id="f04d7-132"><dt>**\_ \_ 未處理 WIA \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="f04d7-132"><dt>**WIA\_STATUS\_NOT\_HANDLED**</dt></span></span> </dl> | <span data-ttu-id="f04d7-133">未採取任何動作;亦即，不會對使用者顯示任何對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f04d7-133">No action was taken; that is, no dialog box was presented to the user.</span></span> <span data-ttu-id="f04d7-134">將會叫用下一個錯誤處理常式。</span><span class="sxs-lookup"><span data-stu-id="f04d7-134">The next error handler will be invoked.</span></span> <span data-ttu-id="f04d7-135">錯誤處理常式的順序如下：應用程式、驅動程式和系統預設值。</span><span class="sxs-lookup"><span data-stu-id="f04d7-135">The order of error handlers is: application, driver, and system default.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="f04d7-136">備註</span><span class="sxs-lookup"><span data-stu-id="f04d7-136">Remarks</span></span>

<span data-ttu-id="f04d7-137">*LPercentComplete* 參數可讓 [錯誤處理常式] 視窗顯示進度。</span><span class="sxs-lookup"><span data-stu-id="f04d7-137">The *lPercentComplete* parameter enables an error handler window to show progress.</span></span> <span data-ttu-id="f04d7-138">例如，驅動程式可能會提供「準備」所需時間的估計。</span><span class="sxs-lookup"><span data-stu-id="f04d7-138">For example, a driver might provide an estimate of how long "warming up" takes.</span></span> <span data-ttu-id="f04d7-139">傳遞至 **IWiaAppErrorHandler：： ReportStatus** 的 *lPercentComplete* 參數，與驅動程式設定為 [**WiaTransferParams**](-wia-wiatransferparams.md)結構的 **lPercentComplete** 值相同。</span><span class="sxs-lookup"><span data-stu-id="f04d7-139">The *lPercentComplete* parameter passed into **IWiaAppErrorHandler::ReportStatus** is the same value as the **lPercentComplete** that the driver sets into the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

<span data-ttu-id="f04d7-140">錯誤處理常式可以使用成功和失敗的宏，以找出 *hrStatus* 的嚴重性 \_ 錯誤或嚴重性 \_ 是否成功。</span><span class="sxs-lookup"><span data-stu-id="f04d7-140">An error handler can use the SUCCEEDED and FAILED macros to find out if *hrStatus* has SEVERITY\_ERROR or SEVERITY\_SUCCESS.</span></span>

<span data-ttu-id="f04d7-141">如果 *hrStatus* 為嚴重性 \_ 成功，則應允許使用者取消傳輸。</span><span class="sxs-lookup"><span data-stu-id="f04d7-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

<span data-ttu-id="f04d7-142">如果 *hrStatus* 是嚴重性 \_ 錯誤，則錯誤處理常式應該會顯示應用程式父視窗所擁有的強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f04d7-142">If *hrStatus* is SEVERITY\_ERROR, the error handler should display a modal dialog box owned by the application parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="f04d7-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="f04d7-143">Requirements</span></span>



| <span data-ttu-id="f04d7-144">需求</span><span class="sxs-lookup"><span data-stu-id="f04d7-144">Requirement</span></span> | <span data-ttu-id="f04d7-145">值</span><span class="sxs-lookup"><span data-stu-id="f04d7-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f04d7-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f04d7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f04d7-147">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f04d7-147">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f04d7-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f04d7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f04d7-149">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f04d7-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f04d7-150">標頭</span><span class="sxs-lookup"><span data-stu-id="f04d7-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="f04d7-151"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="f04d7-151"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="f04d7-152">Idl</span><span class="sxs-lookup"><span data-stu-id="f04d7-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f04d7-153"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f04d7-153"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="f04d7-154">程式庫</span><span class="sxs-lookup"><span data-stu-id="f04d7-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="f04d7-155"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f04d7-155"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




