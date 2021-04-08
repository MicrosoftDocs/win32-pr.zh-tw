---
description: Seek 方法會將搜尋指標變更為相對於緩衝區開頭、緩衝區結尾或目前搜尋指標的新位置。
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: 'IByteBuffer：： Seek 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Seek
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eacfedc3ed23a7a4cf1f60e6c6ac21936c3c94f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851755"
---
# <a name="ibytebufferseek-method"></a><span data-ttu-id="29a1f-103">IByteBuffer：： Seek 方法</span><span class="sxs-lookup"><span data-stu-id="29a1f-103">IByteBuffer::Seek method</span></span>

<span data-ttu-id="29a1f-104">\[**Seek** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="29a1f-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="29a1f-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="29a1f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="29a1f-106">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="29a1f-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="29a1f-107">**Seek** 方法會將搜尋指標變更為相對於緩衝區開頭、緩衝區結尾或目前搜尋指標的新位置。</span><span class="sxs-lookup"><span data-stu-id="29a1f-107">The **Seek** method changes the seek pointer to a new location relative to the beginning of the buffer, to the end of the buffer, or to the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="29a1f-108">語法</span><span class="sxs-lookup"><span data-stu-id="29a1f-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in]  LONG dlibMove,
  [in]  LONG dwOrigin,
  [out] LONG *plibNewPosition
);
```



## <a name="parameters"></a><span data-ttu-id="29a1f-109">參數</span><span class="sxs-lookup"><span data-stu-id="29a1f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29a1f-110">*dlibMove* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29a1f-110">*dlibMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29a1f-111">要加入至 *>dworigin* 所指示之位置的位移。</span><span class="sxs-lookup"><span data-stu-id="29a1f-111">Displacement to be added to the location indicated by *dwOrigin*.</span></span> <span data-ttu-id="29a1f-112">如果 *>dworigin* 是資料流程 \_ 搜尋 \_ 集，這會被視為不帶正負號的值而非正負號。</span><span class="sxs-lookup"><span data-stu-id="29a1f-112">If *dwOrigin* is STREAM\_SEEK\_SET, this is interpreted as an unsigned value rather than signed.</span></span>

</dd> <dt>

<span data-ttu-id="29a1f-113">*>dworigin* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29a1f-113">*dwOrigin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29a1f-114">指定 *dlibMove* 中指定之位移的原點。</span><span class="sxs-lookup"><span data-stu-id="29a1f-114">Specifies the origin for the displacement specified in *dlibMove*.</span></span> <span data-ttu-id="29a1f-115">來源可以是下表中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="29a1f-115">The origin can be one of the values in the following table.</span></span>



| <span data-ttu-id="29a1f-116">值</span><span class="sxs-lookup"><span data-stu-id="29a1f-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="29a1f-117">意義</span><span class="sxs-lookup"><span data-stu-id="29a1f-117">Meaning</span></span>                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <span data-ttu-id="29a1f-118"><dt>**串流 \_ 搜尋 \_ 集合**</dt></span><span class="sxs-lookup"><span data-stu-id="29a1f-118"><dt>**STREAM\_SEEK\_SET**</dt></span></span> </dl> | <span data-ttu-id="29a1f-119">新的 seek 指標是相對於資料流程開頭的位移。</span><span class="sxs-lookup"><span data-stu-id="29a1f-119">The new seek pointer is an offset relative to the beginning of the stream.</span></span> <span data-ttu-id="29a1f-120">在此情況下， *dlibMove* 參數是相對於資料流程開頭的新搜尋位置。</span><span class="sxs-lookup"><span data-stu-id="29a1f-120">In this case, the *dlibMove* parameter is the new seek position relative to the beginning of the stream.</span></span><br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <span data-ttu-id="29a1f-121"><dt>**串流 \_ 搜尋的 \_ 當前**</dt></span><span class="sxs-lookup"><span data-stu-id="29a1f-121"><dt>**STREAM\_SEEK\_CUR**</dt></span></span> </dl> | <span data-ttu-id="29a1f-122">新的 seek 指標是相對於目前搜尋指標位置的位移。</span><span class="sxs-lookup"><span data-stu-id="29a1f-122">The new seek pointer is an offset relative to the current seek pointer location.</span></span> <span data-ttu-id="29a1f-123">在此情況下， *dlibMove* 參數是來自目前搜尋位置的帶正負號的位移。</span><span class="sxs-lookup"><span data-stu-id="29a1f-123">In this case, the *dlibMove* parameter is the signed displacement from the current seek position.</span></span><br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <span data-ttu-id="29a1f-124"><dt>**資料流程 \_ 搜尋 \_ 結束**</dt></span><span class="sxs-lookup"><span data-stu-id="29a1f-124"><dt>**STREAM\_SEEK\_END**</dt></span></span> </dl> | <span data-ttu-id="29a1f-125">新的 seek 指標是相對於資料流程結尾的位移。</span><span class="sxs-lookup"><span data-stu-id="29a1f-125">The new seek pointer is an offset relative to the end of the stream.</span></span> <span data-ttu-id="29a1f-126">在此情況下， *dlibMove* 參數是相對於資料流程結尾的新搜尋位置。</span><span class="sxs-lookup"><span data-stu-id="29a1f-126">In this case, the *dlibMove* parameter is the new seek position relative to the end of the stream.</span></span><br/>             |



 

</dd> <dt>

<span data-ttu-id="29a1f-127">*plibNewPosition* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="29a1f-127">*plibNewPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29a1f-128">位置的指標，這個方法會從資料流程的開頭處寫入新 seek 指標的值。</span><span class="sxs-lookup"><span data-stu-id="29a1f-128">Pointer to the location where this method writes the value of the new seek pointer from the beginning of the stream.</span></span> <span data-ttu-id="29a1f-129">您可以將 this 指標設為 **Null** ，表示您對此值不感興趣。</span><span class="sxs-lookup"><span data-stu-id="29a1f-129">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="29a1f-130">在此情況下，這個方法不會提供新的 seek 指標。</span><span class="sxs-lookup"><span data-stu-id="29a1f-130">In this case, this method does not provide the new seek pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29a1f-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="29a1f-131">Return value</span></span>

<span data-ttu-id="29a1f-132">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="29a1f-132">The return value is an **HRESULT**.</span></span> <span data-ttu-id="29a1f-133">值為 S \_ OK 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="29a1f-133">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="29a1f-134">備註</span><span class="sxs-lookup"><span data-stu-id="29a1f-134">Remarks</span></span>

<span data-ttu-id="29a1f-135">**Seek** 方法會變更 Seek 指標，讓後續的讀取和寫入作業可以在資料流程物件中的不同位置進行。</span><span class="sxs-lookup"><span data-stu-id="29a1f-135">The **Seek** method changes the seek pointer so subsequent read and write operations can take place at a different location in the stream object.</span></span> <span data-ttu-id="29a1f-136">在資料流程的開頭之前搜尋是一項錯誤。</span><span class="sxs-lookup"><span data-stu-id="29a1f-136">It is an error to seek before the beginning of the stream.</span></span> <span data-ttu-id="29a1f-137">但是，它並不是搜尋超過資料流程結尾的錯誤。</span><span class="sxs-lookup"><span data-stu-id="29a1f-137">It is not, however, an error to seek past the end of the stream.</span></span> <span data-ttu-id="29a1f-138">搜尋超過資料流程的結尾適用于後續的寫入作業，因為資料流程將會在寫入作業完成之前，立即延伸至搜尋位置。</span><span class="sxs-lookup"><span data-stu-id="29a1f-138">Seeking past the end of the stream is useful for subsequent write operations, as the stream will at that time be extended to the seek position immediately before the write operation is done.</span></span>

<span data-ttu-id="29a1f-139">您也可以使用這個方法來取得 seek 指標的目前值，方法是呼叫這個方法，並將 *>dworigin* 參數設定為 [串流 \_ 搜尋] \_ ，並將 *dlibMove* 參數設為零，讓 seek 指標不會變更。</span><span class="sxs-lookup"><span data-stu-id="29a1f-139">You can also use this method to obtain the current value of the seek pointer by calling this method with the *dwOrigin* parameter set to STREAM\_SEEK\_CUR and the *dlibMove* parameter set to zero so the seek pointer is not changed.</span></span> <span data-ttu-id="29a1f-140">目前的 seek 指標會在 *plibNewPosition* 參數中傳回。</span><span class="sxs-lookup"><span data-stu-id="29a1f-140">The current seek pointer is returned in the *plibNewPosition* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="29a1f-141">範例</span><span class="sxs-lookup"><span data-stu-id="29a1f-141">Examples</span></span>

<span data-ttu-id="29a1f-142">下列範例顯示如何將搜尋指標定位至新位置。</span><span class="sxs-lookup"><span data-stu-id="29a1f-142">The following example shows positioning the seek pointer to a new location.</span></span>


```C++
LONG     lNewPos;
HRESULT  hr;

// Change the seek pointer.
hr = pIByteBuff->Seek(5, STREAM_SEEK_SET, &lNewPos);
if (FAILED(hr))
  printf("Failed IByteBuffer::Seek\n");
else
  printf("New position is %x\n", lNewPos);
```



## <a name="requirements"></a><span data-ttu-id="29a1f-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="29a1f-143">Requirements</span></span>



| <span data-ttu-id="29a1f-144">需求</span><span class="sxs-lookup"><span data-stu-id="29a1f-144">Requirement</span></span> | <span data-ttu-id="29a1f-145">值</span><span class="sxs-lookup"><span data-stu-id="29a1f-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29a1f-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29a1f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="29a1f-147">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29a1f-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="29a1f-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29a1f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="29a1f-149">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29a1f-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="29a1f-150">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="29a1f-150">End of client support</span></span><br/>    | <span data-ttu-id="29a1f-151">Windows XP</span><span class="sxs-lookup"><span data-stu-id="29a1f-151">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="29a1f-152">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="29a1f-152">End of server support</span></span><br/>    | <span data-ttu-id="29a1f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29a1f-153">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="29a1f-154">標頭</span><span class="sxs-lookup"><span data-stu-id="29a1f-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="29a1f-155"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="29a1f-155"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="29a1f-156">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="29a1f-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="29a1f-157"><dt>Scardssp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="29a1f-157"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="29a1f-158">DLL</span><span class="sxs-lookup"><span data-stu-id="29a1f-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29a1f-159"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29a1f-159"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="29a1f-160">IID</span><span class="sxs-lookup"><span data-stu-id="29a1f-160">IID</span></span><br/>                      | <span data-ttu-id="29a1f-161">IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="29a1f-161">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

