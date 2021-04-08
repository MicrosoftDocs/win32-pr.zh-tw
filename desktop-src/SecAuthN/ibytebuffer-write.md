---
description: Write 方法會將指定的數位從目前搜尋指標開始的資料流程物件寫入資料流程物件。
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: 'IByteBuffer：： Write 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Write
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b5f9b60a296041a18fbd850f1405088f5b0da2ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851752"
---
# <a name="ibytebufferwrite-method"></a><span data-ttu-id="404cb-103">IByteBuffer：： Write 方法</span><span class="sxs-lookup"><span data-stu-id="404cb-103">IByteBuffer::Write method</span></span>

<span data-ttu-id="404cb-104">\[**Write** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="404cb-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="404cb-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="404cb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="404cb-106">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="404cb-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="404cb-107">**Write** 方法會將指定的數位從目前搜尋指標開始的資料流程物件寫入資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="404cb-107">The **Write** method writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="404cb-108">語法</span><span class="sxs-lookup"><span data-stu-id="404cb-108">Syntax</span></span>


```C++
HRESULT Write(
  [in]  BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="404cb-109">參數</span><span class="sxs-lookup"><span data-stu-id="404cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="404cb-110">*pByte* \[在\]</span><span class="sxs-lookup"><span data-stu-id="404cb-110">*pByte* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="404cb-111">包含要寫入至資料流程之資料的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="404cb-111">Address of the buffer containing the data that is to be written to the stream.</span></span> <span data-ttu-id="404cb-112">即使 *cb* 為零，也必須為此參數提供有效的指標。</span><span class="sxs-lookup"><span data-stu-id="404cb-112">A valid pointer must be provided for this parameter even when *cb* is zero.</span></span>

</dd> <dt>

<span data-ttu-id="404cb-113">*cb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="404cb-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="404cb-114">嘗試寫入資料流程的資料位元組數。</span><span class="sxs-lookup"><span data-stu-id="404cb-114">Number of bytes of data to attempt to write into the stream.</span></span> <span data-ttu-id="404cb-115">這個參數可以是零。</span><span class="sxs-lookup"><span data-stu-id="404cb-115">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="404cb-116">*pcbWritten* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="404cb-116">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="404cb-117">**長** 變數的位址，這個方法會寫入寫入資料流程物件的實際位元組數目。</span><span class="sxs-lookup"><span data-stu-id="404cb-117">Address of a **LONG** variable where this method writes the actual number of bytes written to the stream object.</span></span> <span data-ttu-id="404cb-118">呼叫端可以將 this 指標設為 **Null**，在此情況下，這個方法不會提供實際寫入的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="404cb-118">The caller can set this pointer to **NULL**, in which case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="404cb-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="404cb-119">Return value</span></span>

<span data-ttu-id="404cb-120">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="404cb-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="404cb-121">值為 S \_ OK 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="404cb-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="404cb-122">備註</span><span class="sxs-lookup"><span data-stu-id="404cb-122">Remarks</span></span>

<span data-ttu-id="404cb-123">**IByteBuffer：： Write** 方法會將指定的資料寫入資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="404cb-123">The **IByteBuffer::Write** method writes the specified data to a stream object.</span></span> <span data-ttu-id="404cb-124">搜尋指標會針對實際寫入的位元組數進行調整。</span><span class="sxs-lookup"><span data-stu-id="404cb-124">The seek pointer is adjusted for the number of bytes actually written.</span></span> <span data-ttu-id="404cb-125">實際寫入的位元組數目會在 *pcbWritten* 參數中傳回。</span><span class="sxs-lookup"><span data-stu-id="404cb-125">The number of bytes actually written is returned in the *pcbWritten* parameter.</span></span> <span data-ttu-id="404cb-126">如果位元組計數為零個位元組，則寫入作業不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="404cb-126">If the byte count is zero bytes, the write operation has no effect.</span></span>

<span data-ttu-id="404cb-127">如果 seek 指標目前超過資料流程的結尾，而且位元組計數為非零值，則這個方法會將資料流程的大小增加到 seek 指標，並從 seek 指標開始寫入指定的位元組。</span><span class="sxs-lookup"><span data-stu-id="404cb-127">If the seek pointer is currently past the end of the stream and the byte count is nonzero, this method increases the size of the stream to the seek pointer and writes the specified bytes starting at the seek pointer.</span></span> <span data-ttu-id="404cb-128">寫入資料流程的填滿位元組不會初始化為任何特定的值。</span><span class="sxs-lookup"><span data-stu-id="404cb-128">The fill bytes written to the stream are not initialized to any particular value.</span></span> <span data-ttu-id="404cb-129">這與 MS-DOS FAT 檔案系統中的檔案結尾行為相同。</span><span class="sxs-lookup"><span data-stu-id="404cb-129">This is the same as the end-of-file behavior in the MS-DOS FAT file system.</span></span>

<span data-ttu-id="404cb-130">若使用零位元組計數和超出資料流程結尾的 seek 指標，此方法不會建立填滿位元組來將資料流程增加到 seek 指標。</span><span class="sxs-lookup"><span data-stu-id="404cb-130">With a zero byte count and a seek pointer past the end of the stream, this method does not create the fill bytes to increase the stream to the seek pointer.</span></span> <span data-ttu-id="404cb-131">在此情況下，您必須呼叫 [**IByteBuffer：： SetSize**](ibytebuffer-setsize.md) 方法，以增加資料流程的大小並寫入填滿位元組。</span><span class="sxs-lookup"><span data-stu-id="404cb-131">In this case, you must call the [**IByteBuffer::SetSize**](ibytebuffer-setsize.md) method to increase the size of the stream and write the fill bytes.</span></span>

<span data-ttu-id="404cb-132">*PcbWritten* 參數可以有值（即使發生錯誤）。</span><span class="sxs-lookup"><span data-stu-id="404cb-132">The *pcbWritten* parameter can have a value even if an error occurs.</span></span>

<span data-ttu-id="404cb-133">在 COM 提供的執行中，資料流程物件並不是稀疏的。</span><span class="sxs-lookup"><span data-stu-id="404cb-133">In the COM-provided implementation, stream objects are not sparse.</span></span> <span data-ttu-id="404cb-134">任何填滿的位元組最後都會配置在磁片上，並指派給串流。</span><span class="sxs-lookup"><span data-stu-id="404cb-134">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

## <a name="examples"></a><span data-ttu-id="404cb-135">範例</span><span class="sxs-lookup"><span data-stu-id="404cb-135">Examples</span></span>

<span data-ttu-id="404cb-136">下列範例示範如何將位元組寫入資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="404cb-136">The following example shows writing bytes into the stream object.</span></span>


```C++
LONG     lWrite;
HRESULT  hr;

// Write to the buffer.
// byData is an array of 64 bytes.
hr = pIByteBuff->Write(byData,
                       64,
                       &lWrite);
if (FAILED(hr))
  printf("Failed IByteBuffer::Write\n");
```



## <a name="requirements"></a><span data-ttu-id="404cb-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="404cb-137">Requirements</span></span>



| <span data-ttu-id="404cb-138">需求</span><span class="sxs-lookup"><span data-stu-id="404cb-138">Requirement</span></span> | <span data-ttu-id="404cb-139">值</span><span class="sxs-lookup"><span data-stu-id="404cb-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="404cb-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="404cb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="404cb-141">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="404cb-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="404cb-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="404cb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="404cb-143">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="404cb-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="404cb-144">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="404cb-144">End of client support</span></span><br/>    | <span data-ttu-id="404cb-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="404cb-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="404cb-146">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="404cb-146">End of server support</span></span><br/>    | <span data-ttu-id="404cb-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="404cb-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="404cb-148">標頭</span><span class="sxs-lookup"><span data-stu-id="404cb-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="404cb-149"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="404cb-149"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="404cb-150">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="404cb-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="404cb-151"><dt>Scardssp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="404cb-151"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="404cb-152">DLL</span><span class="sxs-lookup"><span data-stu-id="404cb-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="404cb-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="404cb-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="404cb-154">IID</span><span class="sxs-lookup"><span data-stu-id="404cb-154">IID</span></span><br/>                      | <span data-ttu-id="404cb-155">IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="404cb-155">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

