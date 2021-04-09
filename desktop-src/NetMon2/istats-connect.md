---
description: Connect 方法會使用指定的 NIC 將 NPP 連接到網路，並提供連線的設定資訊。
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: 'IStats：： Connect 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7705600c3ce68b719014c928ac4d02c62cba64cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853120"
---
# <a name="istatsconnect-method"></a><span data-ttu-id="bc469-103">IStats：： Connect 方法</span><span class="sxs-lookup"><span data-stu-id="bc469-103">IStats::Connect method</span></span>

<span data-ttu-id="bc469-104">**Connect** 方法會使用指定的 NIC 將 NPP 連接到網路，並提供連線的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="bc469-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc469-105">語法</span><span class="sxs-lookup"><span data-stu-id="bc469-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="bc469-106">參數</span><span class="sxs-lookup"><span data-stu-id="bc469-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc469-107">*hInputBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc469-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc469-108">BLOB 的控制碼，指定 NPP 連接的 NIC，以及該連接的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="bc469-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="bc469-109">*StatusCallbackProc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc469-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc469-110">使用者回呼函式的位址，此函式會接收狀態更新（例如觸發程式）。</span><span class="sxs-lookup"><span data-stu-id="bc469-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="bc469-111">如果未使用回呼函式，請將此參數和 *UserCoNtext* 參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bc469-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bc469-112">*UserCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc469-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc469-113">呼叫使用者的回呼函數時傳遞的值。</span><span class="sxs-lookup"><span data-stu-id="bc469-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="bc469-114">這個參數的值通常是 HWND 或 ' this ' 指標。</span><span class="sxs-lookup"><span data-stu-id="bc469-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="bc469-115">如果未指定回呼函數，請將此參數和 *StatusCallbackProc* 參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bc469-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bc469-116">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bc469-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc469-117">錯誤 BLOB 的控制碼，其中包含其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="bc469-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc469-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc469-118">Return value</span></span>

<span data-ttu-id="bc469-119">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="bc469-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bc469-120">如果此方法不成功，則傳回值會是下列其中一個錯誤碼 (其中包含內部 **IStats：： Configure** 呼叫) 所傳回的錯誤：</span><span class="sxs-lookup"><span data-stu-id="bc469-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IStats::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc469-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bc469-121">Return code</span></span></th>
<th><span data-ttu-id="bc469-122">Description</span><span class="sxs-lookup"><span data-stu-id="bc469-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="bc469-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="bc469-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="bc469-124">NPP COM 物件的這個實例已連線到網路。</span><span class="sxs-lookup"><span data-stu-id="bc469-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="bc469-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="bc469-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="bc469-126">設定 BLOB 已損毀。</span><span class="sxs-lookup"><span data-stu-id="bc469-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="bc469-127">此錯誤是由 <strong>IStats：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="bc469-127">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="bc469-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="bc469-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="bc469-129"><em>HInputBlob</em>參數所指定的輸入 BLOB 缺少執行這項作業所需的專案。</span><span class="sxs-lookup"><span data-stu-id="bc469-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="bc469-130">此錯誤可能是由 <strong>IStats：： Connect</strong> 或 <strong>IStats：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="bc469-130">This error might be generated by the <strong>IStats::Connect</strong> or <strong>IStats::Configure</strong> call.</span></span> <span data-ttu-id="bc469-131">查看 <em>hErrorBlob</em> 傳回的錯誤 BLOB，以判斷找不到哪個專案。</span><span class="sxs-lookup"><span data-stu-id="bc469-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="bc469-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="bc469-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="bc469-133">尚未呼叫 <strong>CreateBlob</strong> 函數。</span><span class="sxs-lookup"><span data-stu-id="bc469-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="bc469-134">此錯誤是由 <strong>IStats：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="bc469-134">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="bc469-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="bc469-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="bc469-136">字串不是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="bc469-136">The string is not null-terminated.</span></span> <span data-ttu-id="bc469-137">此錯誤是由 <strong>IStats：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="bc469-137">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="bc469-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="bc469-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="bc469-139">輸入 BLOB 的觸發程式部分已損毀。</span><span class="sxs-lookup"><span data-stu-id="bc469-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="bc469-140">此錯誤是由 <strong>IStats：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="bc469-140">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="bc469-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="bc469-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="bc469-142"><em>HInputBlob</em>中指定的物件不是 BLOB。</span><span class="sxs-lookup"><span data-stu-id="bc469-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="bc469-143">此錯誤是由 <strong>IStats：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="bc469-143">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="bc469-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="bc469-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="bc469-145">未在登錄中設定預設的 capture 目錄。</span><span class="sxs-lookup"><span data-stu-id="bc469-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="bc469-146">若要設定 capture 目錄，請使用下列路徑。</span><span class="sxs-lookup"><span data-stu-id="bc469-146">To set the capture directory, use the following path.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="bc469-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="bc469-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="bc469-148">無法使用執行此作業所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="bc469-148">The memory required to perform this operation was unavailable.</span></span> <span data-ttu-id="bc469-149">此錯誤是由 <strong>IStats：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="bc469-149">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="bc469-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="bc469-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="bc469-151">要求已超時。此錯誤是由 <strong>IStats：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="bc469-151">The request has timed out. This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="bc469-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="bc469-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="bc469-153"><em>HInputBlob</em>中指定的 BLOB 版本號碼不正確。</span><span class="sxs-lookup"><span data-stu-id="bc469-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="bc469-154">此錯誤是由 <strong>IStats：： Configure</strong> 呼叫所產生。</span><span class="sxs-lookup"><span data-stu-id="bc469-154">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="bc469-155">備註</span><span class="sxs-lookup"><span data-stu-id="bc469-155">Remarks</span></span>

<span data-ttu-id="bc469-156">呼叫 **Connect** 方法時，網路監視器會使用 *hInputBlob* 參數所提供的 BLOB，自動呼叫 **IStats：： Configure** 方法。</span><span class="sxs-lookup"><span data-stu-id="bc469-156">When the **Connect** method is called, Network Monitor automatically calls the **IStats::Configure** method by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="bc469-157">請注意， **IStats：： Configure** 的呼叫所傳回的任何錯誤碼都會回傳，並由 **IStats：： Connect** 呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="bc469-157">Note that any error codes returned by the call to **IStats::Configure** are passed back and returned by the **IStats::Connect** call.</span></span>

<span data-ttu-id="bc469-158">您必須先呼叫這個方法，才能開始捕獲框架。</span><span class="sxs-lookup"><span data-stu-id="bc469-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="bc469-159">請注意，當您使用此方法連接到網路時，您必須繼續使用 **IStats** 介面來捕捉畫面格。</span><span class="sxs-lookup"><span data-stu-id="bc469-159">Note that when you connect to the network by using this method, you must continue to use the **IStats** interface to capture frames.</span></span>

<span data-ttu-id="bc469-160">*HInputBlob* 指定的輸入 BLOB 可以藉由呼叫 **GetNPPBlobFromUI**、 **GetNPPBlobTable** 和 **SelectNPPBlobFromTable** 方法來取得。</span><span class="sxs-lookup"><span data-stu-id="bc469-160">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="bc469-161">*HErrorBlob* 參數所傳回的錯誤 BLOB 包含網路監視器無法在 *hInputBlob* 中指定的輸入 BLOB 中瞭解或尋找的專案。</span><span class="sxs-lookup"><span data-stu-id="bc469-161">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="bc469-162">傳回的錯誤 BLOB 包含應用程式可用於進行疑難排解的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="bc469-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="bc469-163">例如，如果傳回 NMERR \_ BLOB \_ 專案不存在，則會在 \_ 傳回的 \_ \_ 錯誤 BLOB 中包含網路監視器找不到的專案。</span><span class="sxs-lookup"><span data-stu-id="bc469-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="bc469-164">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="bc469-164">For information about</span></span>                                             | <span data-ttu-id="bc469-165">請參閱</span><span class="sxs-lookup"><span data-stu-id="bc469-165">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bc469-166">取得代表網路介面卡的輸入 BLOB</span><span class="sxs-lookup"><span data-stu-id="bc469-166">Obtaining the input BLOB that represents a network interface card</span></span> | [<span data-ttu-id="bc469-167">選取網路介面卡</span><span class="sxs-lookup"><span data-stu-id="bc469-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="bc469-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc469-168">Requirements</span></span>



| <span data-ttu-id="bc469-169">需求</span><span class="sxs-lookup"><span data-stu-id="bc469-169">Requirement</span></span> | <span data-ttu-id="bc469-170">值</span><span class="sxs-lookup"><span data-stu-id="bc469-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc469-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc469-171">Minimum supported client</span></span><br/> | <span data-ttu-id="bc469-172">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc469-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="bc469-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc469-173">Minimum supported server</span></span><br/> | <span data-ttu-id="bc469-174">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc469-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="bc469-175">標頭</span><span class="sxs-lookup"><span data-stu-id="bc469-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc469-176"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="bc469-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="bc469-177">DLL</span><span class="sxs-lookup"><span data-stu-id="bc469-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc469-178"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc469-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc469-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc469-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc469-180">IStats</span><span class="sxs-lookup"><span data-stu-id="bc469-180">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="bc469-181">IStats：： Configure</span><span class="sxs-lookup"><span data-stu-id="bc469-181">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="bc469-182">IStats：:D isconnect</span><span class="sxs-lookup"><span data-stu-id="bc469-182">IStats::Disconnect</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="bc469-183">網路監視器 BLOB</span><span class="sxs-lookup"><span data-stu-id="bc469-183">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




