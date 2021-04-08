---
description: Connect 方法會使用指定的 NIC 將 NPP 連接到網路，並提供連線的設定資訊。
ms.assetid: 48189b2b-9889-4bd8-8972-26005fb7c341
title: 'IESP：： Connect 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 4fc9c88b0eb4671c61f268c5857dceba3dc500f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112213"
---
# <a name="iespconnect-method"></a><span data-ttu-id="11c22-103">IESP：： Connect 方法</span><span class="sxs-lookup"><span data-stu-id="11c22-103">IESP::Connect method</span></span>

<span data-ttu-id="11c22-104">**Connect** 方法會使用指定的 NIC 將 NPP 連接到網路，並提供連線的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="11c22-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information about the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="11c22-105">語法</span><span class="sxs-lookup"><span data-stu-id="11c22-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB hInputBlob,
  [in]  DWORD StatusCallbackProc,
  [in]  DWORD UserContext,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="11c22-106">參數</span><span class="sxs-lookup"><span data-stu-id="11c22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11c22-107">*hInputBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11c22-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11c22-108">BLOB 的控制碼，指定 NPP 連接的 NIC，以及該連接的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="11c22-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="11c22-109">*StatusCallbackProc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11c22-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11c22-110">使用者回呼函式的位址，此函式會接收狀態更新（例如觸發程式）。</span><span class="sxs-lookup"><span data-stu-id="11c22-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="11c22-111">如果未使用回呼函式，請將此參數和 *UserCoNtext* 參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="11c22-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="11c22-112">*UserCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11c22-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11c22-113">呼叫使用者的回呼函數時傳遞的值。</span><span class="sxs-lookup"><span data-stu-id="11c22-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="11c22-114">這個參數的值通常是 HWND 或 ' this ' 指標。</span><span class="sxs-lookup"><span data-stu-id="11c22-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="11c22-115">如果未指定回呼函數，請將此參數和 *StatusCallbackProc* 參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="11c22-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="11c22-116">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="11c22-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11c22-117">錯誤 BLOB 的控制碼，其中包含其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="11c22-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11c22-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="11c22-118">Return value</span></span>

<span data-ttu-id="11c22-119">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="11c22-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="11c22-120">如果此方法不成功，則傳回值會是下列其中一個錯誤碼 (其中包含內部 **IESP：： Configure** 呼叫) 所傳回的錯誤：</span><span class="sxs-lookup"><span data-stu-id="11c22-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IESP::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11c22-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="11c22-121">Return code</span></span></th>
<th><span data-ttu-id="11c22-122">Description</span><span class="sxs-lookup"><span data-stu-id="11c22-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="11c22-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="11c22-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="11c22-124">NPP COM 物件的這個實例已連線到網路。</span><span class="sxs-lookup"><span data-stu-id="11c22-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="11c22-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="11c22-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="11c22-126">設定 BLOB 已損毀。</span><span class="sxs-lookup"><span data-stu-id="11c22-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="11c22-127">此錯誤是由 <strong>IESP：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="11c22-127">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="11c22-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="11c22-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="11c22-129"><em>HInputBlob</em>參數所指定的輸入 BLOB 缺少執行這項作業所需的專案。</span><span class="sxs-lookup"><span data-stu-id="11c22-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="11c22-130">此錯誤可能是由 <strong>IESP：： Connect</strong> 或 <strong>IESP：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="11c22-130">This error might be generated by the <strong>IESP::Connect</strong> or <strong>IESP::Configure</strong> call.</span></span> <span data-ttu-id="11c22-131">查看 <em>hErrorBlob</em> 傳回的錯誤 BLOB，以判斷找不到哪個專案。</span><span class="sxs-lookup"><span data-stu-id="11c22-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="11c22-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="11c22-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="11c22-133">尚未呼叫 <strong>CreateBlob</strong> 函數。</span><span class="sxs-lookup"><span data-stu-id="11c22-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="11c22-134">此錯誤是由 <strong>IESP：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="11c22-134">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="11c22-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="11c22-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="11c22-136">字串不是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="11c22-136">The string is not null-terminated.</span></span> <span data-ttu-id="11c22-137">此錯誤是由 <strong>IESP：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="11c22-137">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="11c22-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="11c22-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="11c22-139">輸入 BLOB 的觸發程式部分已損毀。</span><span class="sxs-lookup"><span data-stu-id="11c22-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="11c22-140">此錯誤是由 <strong>IESP：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="11c22-140">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="11c22-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="11c22-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="11c22-142"><em>HInputBlob</em>中指定的物件不是 BLOB。</span><span class="sxs-lookup"><span data-stu-id="11c22-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="11c22-143">此錯誤是由 <strong>IESP：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="11c22-143">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="11c22-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="11c22-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="11c22-145">未在登錄中設定預設的 capture 目錄。</span><span class="sxs-lookup"><span data-stu-id="11c22-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="11c22-146">使用下列路徑來設定 capture 目錄。</span><span class="sxs-lookup"><span data-stu-id="11c22-146">Use the following path to set the capture directory.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="11c22-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="11c22-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="11c22-148">執行這項作業所需的記憶體無法使用。</span><span class="sxs-lookup"><span data-stu-id="11c22-148">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="11c22-149">此錯誤是由 <strong>IESP：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="11c22-149">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="11c22-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="11c22-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="11c22-151">要求已超時。此錯誤是由 <strong>IESP：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="11c22-151">The request has timed out. This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="11c22-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="11c22-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="11c22-153"><em>HInputBlob</em>中指定的 BLOB 版本號碼不正確。</span><span class="sxs-lookup"><span data-stu-id="11c22-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="11c22-154">此錯誤是由 <strong>IESP：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="11c22-154">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="11c22-155">備註</span><span class="sxs-lookup"><span data-stu-id="11c22-155">Remarks</span></span>

<span data-ttu-id="11c22-156">呼叫 **Connect** 方法時，網路監視器會使用 *hInputBlob* 參數所提供的 BLOB，自動呼叫 **IESP：： Configure** 。</span><span class="sxs-lookup"><span data-stu-id="11c22-156">When the **Connect** method is called, Network Monitor automatically calls **IESP::Configure** by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="11c22-157">請注意， **IESP：： Configure** 的呼叫所傳回的任何錯誤碼都會回傳，並由 **IESP：： Connect** 呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="11c22-157">Note that any error codes returned by the call to **IESP::Configure** are passed back and returned by the **IESP::Connect** call.</span></span>

<span data-ttu-id="11c22-158">您必須先呼叫這個方法，才能開始捕獲框架。</span><span class="sxs-lookup"><span data-stu-id="11c22-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="11c22-159">請注意，當您使用此方法連接到網路時，您必須繼續使用 **IESP** 介面來捕捉畫面格。</span><span class="sxs-lookup"><span data-stu-id="11c22-159">Note that when you connect to the network by using this method, you must continue to use the **IESP** interface to capture frames.</span></span>

<span data-ttu-id="11c22-160">您可以藉由呼叫 **GetNPPBlobFromUI**、 **GetNPPBlobTable** 和 **SelectNPPBlobFromTable** 來取得 *hInputBlob* 所指定的輸入 BLOB。</span><span class="sxs-lookup"><span data-stu-id="11c22-160">The input BLOB specified by *hInputBlob* can be obtained by calling **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable**.</span></span>

<span data-ttu-id="11c22-161">*HErrorBlob* 所傳回的錯誤 BLOB 包含網路監視器無法在 *hInputBlob* 中指定的輸入 BLOB 中瞭解或尋找的專案。</span><span class="sxs-lookup"><span data-stu-id="11c22-161">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="11c22-162">傳回的錯誤 BLOB 包含應用程式可用於進行疑難排解的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="11c22-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="11c22-163">例如，如果傳回 NMERR \_ BLOB \_ 專案不存在，則會在 \_ 傳回的 \_ \_ 錯誤 BLOB 中包含網路監視器找不到的專案。</span><span class="sxs-lookup"><span data-stu-id="11c22-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="11c22-164">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="11c22-164">For information about</span></span>                          | <span data-ttu-id="11c22-165">請參閱</span><span class="sxs-lookup"><span data-stu-id="11c22-165">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="11c22-166">取得代表 NIC 的輸入 BLOB</span><span class="sxs-lookup"><span data-stu-id="11c22-166">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="11c22-167">選取網路介面卡</span><span class="sxs-lookup"><span data-stu-id="11c22-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="11c22-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="11c22-168">Requirements</span></span>



| <span data-ttu-id="11c22-169">需求</span><span class="sxs-lookup"><span data-stu-id="11c22-169">Requirement</span></span> | <span data-ttu-id="11c22-170">值</span><span class="sxs-lookup"><span data-stu-id="11c22-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c22-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11c22-171">Minimum supported client</span></span><br/> | <span data-ttu-id="11c22-172">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11c22-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="11c22-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11c22-173">Minimum supported server</span></span><br/> | <span data-ttu-id="11c22-174">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11c22-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="11c22-175">標頭</span><span class="sxs-lookup"><span data-stu-id="11c22-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="11c22-176"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="11c22-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="11c22-177">DLL</span><span class="sxs-lookup"><span data-stu-id="11c22-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11c22-178"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11c22-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11c22-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11c22-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c22-180">IESP</span><span class="sxs-lookup"><span data-stu-id="11c22-180">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="11c22-181">IESP：： Configure</span><span class="sxs-lookup"><span data-stu-id="11c22-181">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="11c22-182">IESP：:D isconnect</span><span class="sxs-lookup"><span data-stu-id="11c22-182">IESP::Disconnect</span></span>](iesp-disconnect.md)
</dt> <dt>

[<span data-ttu-id="11c22-183">IESP：： Start</span><span class="sxs-lookup"><span data-stu-id="11c22-183">IESP::Start</span></span>](iesp-start.md)
</dt> </dl>

 

 




