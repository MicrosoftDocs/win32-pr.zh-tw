---
description: IRTC：： Connect 方法-Connect 方法會使用指定的 NIC 將 NPP 連接到網路，並提供連線的設定資訊。
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: 'IRTC：： Connect 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ba62f3341b18ddfdbf09af4eec701322d901ab79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110742"
---
# <a name="irtcconnect-method"></a><span data-ttu-id="c8d4f-103">IRTC：： Connect 方法</span><span class="sxs-lookup"><span data-stu-id="c8d4f-103">IRTC::Connect method</span></span>

<span data-ttu-id="c8d4f-104">**Connect** 方法會使用指定的 NIC 將 NPP 連接到網路，並提供連線的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8d4f-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8d4f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="c8d4f-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8d4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8d4f-107">*hInputBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8d4f-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d4f-108">BLOB 的控制碼，指定您要連接的 NIC 以及該連接的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="c8d4f-109">*StatusCallbackProc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8d4f-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d4f-110">使用者狀態回呼函式的位址，此函式會接收狀態更新（例如觸發程式）。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-110">Address of the user's status callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="c8d4f-111">這個參數可以設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-111">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c8d4f-112">*FramesCallbackProc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8d4f-112">*FramesCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d4f-113">使用者的框架回呼函式位址，用來接收狀態更新（例如觸發程式）。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-113">Address of the user's frame callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="c8d4f-114">這個參數可以設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-114">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c8d4f-115">*UserCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8d4f-115">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d4f-116">呼叫使用者的狀態和框架回呼函數時傳遞的值。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-116">Value passed when the user's status and frame callback function is called.</span></span> <span data-ttu-id="c8d4f-117">如果同時指定兩個回呼函數，則必須使用相同的使用者內容值。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-117">If both callback functions are specified, they must use the same user-context value.</span></span> <span data-ttu-id="c8d4f-118">這個參數的值通常是 HWND 或 ' this ' 指標。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-118">The value of this parameter is typically either HWND or a 'this' pointer.</span></span>

</dd> <dt>

<span data-ttu-id="c8d4f-119">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c8d4f-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d4f-120">錯誤 BLOB 的控制碼，其中包含其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-120">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="c8d4f-121">請參閱本主題底部的備註，以取得錯誤 BLOB 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-121">See Remarks at the bottom of this topic for information about what is in the error BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8d4f-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8d4f-122">Return value</span></span>

<span data-ttu-id="c8d4f-123">如果此方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-123">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c8d4f-124">如果此方法不成功，則傳回值會是下列其中一個錯誤碼 (其中包含內部 **IRTC：： Configure** 呼叫) 所傳回的錯誤：</span><span class="sxs-lookup"><span data-stu-id="c8d4f-124">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IRTC::Configure** call):</span></span>



| <span data-ttu-id="c8d4f-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c8d4f-125">Return code</span></span>                                                                                                         | <span data-ttu-id="c8d4f-126">Description</span><span class="sxs-lookup"><span data-stu-id="c8d4f-126">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8d4f-127"><dt>**NMERR \_ 已 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="c8d4f-127"><dt>**NMERR\_ALREADY\_CONNECTED**</dt></span></span> </dl>            | <span data-ttu-id="c8d4f-128">NPP COM 物件的這個實例已連線到網路。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-128">This instance of the NPP COM object is already connected to the network.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="c8d4f-129"><dt>**NMERR \_ BLOB \_ 轉換 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="c8d4f-129"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="c8d4f-130">設定 BLOB 已損毀。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-130">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="c8d4f-131">此錯誤是由 **IRTC：： Configure** 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-131">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="c8d4f-132"><dt>**NMERR \_ BLOB \_ 專案 \_ 不 \_ \_ 存在**</dt></span><span class="sxs-lookup"><span data-stu-id="c8d4f-132"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="c8d4f-133">*HInputBlob* 參數所指定的輸入 BLOB 缺少執行這項作業所需的專案。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-133">The input BLOB specified by the *hInputBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="c8d4f-134">此錯誤可能是由 **IRTC：： Connect** 或 **IRTC：： Configure** 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-134">This error may be generated by the **IRTC::Connect** or **IRTC::Configure** call.</span></span> <span data-ttu-id="c8d4f-135">查看 *hErrorBlob* 傳回的錯誤 BLOB，以判斷找不到哪個專案。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-135">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="c8d4f-136"><dt>**NMERR \_ BLOB \_ 未 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="c8d4f-136"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="c8d4f-137">尚未呼叫 **CreateBlob** 函數。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-137">The **CreateBlob** function has not been called.</span></span> <span data-ttu-id="c8d4f-138">此錯誤是由 **IRTC：： Configure** 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-138">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="c8d4f-139"><dt>**NMERR \_ BLOB \_ 字串 \_ 無效**</dt></span><span class="sxs-lookup"><span data-stu-id="c8d4f-139"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="c8d4f-140">字串不是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-140">The string is not null-terminated.</span></span> <span data-ttu-id="c8d4f-141">此錯誤是由 **IRTC：： Configure** 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-141">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="c8d4f-142"><dt>**NMERR 不 \_ 合法的 \_ 觸發程式**</dt></span><span class="sxs-lookup"><span data-stu-id="c8d4f-142"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="c8d4f-143">輸入 BLOB 的觸發程式部分已損毀。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-143">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="c8d4f-144">此錯誤是由 **IRTC：： Configure** 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-144">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="c8d4f-145"><dt>**NMERR \_ 不正確 \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="c8d4f-145"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="c8d4f-146">*HInputBlob* 中指定的物件不是 BLOB。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-146">The object specified in *hInputBlob* is not a BLOB.</span></span> <span data-ttu-id="c8d4f-147">此錯誤是由 **IRTC：： Configure** 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-147">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="c8d4f-148"><dt>**NMERR \_ \_ 記憶體不足 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c8d4f-148"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="c8d4f-149">執行這項作業所需的記憶體無法使用。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-149">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="c8d4f-150">此錯誤是由 **IRTC：： Configure** 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-150">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="c8d4f-151"><dt>**NMERR \_ TIMEOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="c8d4f-151"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="c8d4f-152">要求已超時。此錯誤是由 **IRTC：： Configure** 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-152">The request has timed out. This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="c8d4f-153"><dt>**NMERR \_ 上層 \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="c8d4f-153"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="c8d4f-154">*HInputBlob* 中指定的 BLOB 版本號碼不正確。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-154">The version number of the BLOB specified in *hInputBlob* is incorrect.</span></span> <span data-ttu-id="c8d4f-155">此錯誤是由 **IRTC：： Configure** 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-155">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="c8d4f-156">備註</span><span class="sxs-lookup"><span data-stu-id="c8d4f-156">Remarks</span></span>

<span data-ttu-id="c8d4f-157">呼叫 **Connect** 方法時，NPP 會使用 *hInputBlob* 所提供的 BLOB，自動呼叫 **IRTC：： Configure** 方法。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-157">When the **Connect** method is called, the NPP automatically calls the **IRTC::Configure** method by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="c8d4f-158">請注意， **IRTC：： Configure** 的呼叫所傳回的任何錯誤碼都會回傳，並由 **IRTC：： Connect** 呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-158">Note that any error codes returned by the call to **IRTC::Configure** are passed back and returned by the **IRTC::Connect** call.</span></span>

<span data-ttu-id="c8d4f-159">您必須先呼叫這個方法，才能開始捕獲框架。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-159">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="c8d4f-160">請注意，當您使用這個方法連接到網路時，您必須繼續使用 **IRTC** 介面來捕捉畫面格。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-160">Note that when you connect to the network using this method, you must continue to use the **IRTC** interface to capture frames.</span></span>

<span data-ttu-id="c8d4f-161">呼叫此函式時，您必須指定狀態或框架回呼函式，即使它只作為預留位置。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-161">When calling this function, you must specify a status or frame callback function, even if it only acts as a placeholder.</span></span>

<span data-ttu-id="c8d4f-162">*HInputBlob* 指定的輸入 BLOB 可以藉由呼叫 **GetNPPBlobFromUI**、 **GetNPPBlobTable** 和 **SelectNPPBlobFromTable** 方法來取得。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-162">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="c8d4f-163">*HErrorBlob* 中傳回的錯誤 BLOB 包含開發人員或應用程式可用於進行疑難排解的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-163">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="c8d4f-164">*HErrorBlob* 所傳回的錯誤 BLOB 包含網路監視器無法在 *hInputBlob* 中指定的輸入 BLOB 中瞭解或尋找的專案。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-164">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="c8d4f-165">例如，如果傳回 NMERR \_ BLOB \_ 專案不存在，則會在 \_ \_ \_ 傳回的錯誤 BLOB 中包含網路監視器找不到的專案。</span><span class="sxs-lookup"><span data-stu-id="c8d4f-165">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="c8d4f-166">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="c8d4f-166">For information about</span></span>                          | <span data-ttu-id="c8d4f-167">請參閱</span><span class="sxs-lookup"><span data-stu-id="c8d4f-167">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c8d4f-168">取得代表 NIC 的輸入 BLOB</span><span class="sxs-lookup"><span data-stu-id="c8d4f-168">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="c8d4f-169">選取網路介面卡</span><span class="sxs-lookup"><span data-stu-id="c8d4f-169">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="c8d4f-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8d4f-170">Requirements</span></span>



| <span data-ttu-id="c8d4f-171">需求</span><span class="sxs-lookup"><span data-stu-id="c8d4f-171">Requirement</span></span> | <span data-ttu-id="c8d4f-172">值</span><span class="sxs-lookup"><span data-stu-id="c8d4f-172">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d4f-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8d4f-173">Minimum supported client</span></span><br/> | <span data-ttu-id="c8d4f-174">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8d4f-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c8d4f-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8d4f-175">Minimum supported server</span></span><br/> | <span data-ttu-id="c8d4f-176">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8d4f-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c8d4f-177">標頭</span><span class="sxs-lookup"><span data-stu-id="c8d4f-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8d4f-178"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="c8d4f-178"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c8d4f-179">DLL</span><span class="sxs-lookup"><span data-stu-id="c8d4f-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8d4f-180"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8d4f-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8d4f-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8d4f-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8d4f-182">IRTC</span><span class="sxs-lookup"><span data-stu-id="c8d4f-182">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="c8d4f-183">IRTC：： Configure</span><span class="sxs-lookup"><span data-stu-id="c8d4f-183">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="c8d4f-184">IRTC：:D isconnect</span><span class="sxs-lookup"><span data-stu-id="c8d4f-184">IRTC::Disconnect</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="c8d4f-185">IRTC：： Start</span><span class="sxs-lookup"><span data-stu-id="c8d4f-185">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




