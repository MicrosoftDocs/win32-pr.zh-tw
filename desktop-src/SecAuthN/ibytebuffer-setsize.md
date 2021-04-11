---
description: SetSize 方法會變更資料流程物件的大小。
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: 'IByteBuffer：： SetSize 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.SetSize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 85a6abc11f3e007f3c8d1057cb5c8785c8519ebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945040"
---
# <a name="ibytebuffersetsize-method"></a><span data-ttu-id="bf3ae-103">IByteBuffer：： SetSize 方法</span><span class="sxs-lookup"><span data-stu-id="bf3ae-103">IByteBuffer::SetSize method</span></span>

<span data-ttu-id="bf3ae-104">\[**SetSize** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="bf3ae-104">\[The **SetSize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bf3ae-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="bf3ae-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bf3ae-106">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="bf3ae-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="bf3ae-107">**SetSize** 方法會變更資料流程物件的大小。</span><span class="sxs-lookup"><span data-stu-id="bf3ae-107">The **SetSize** method changes the size of the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf3ae-108">語法</span><span class="sxs-lookup"><span data-stu-id="bf3ae-108">Syntax</span></span>


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a><span data-ttu-id="bf3ae-109">參數</span><span class="sxs-lookup"><span data-stu-id="bf3ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf3ae-110">*libNewSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf3ae-110">*libNewSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf3ae-111">資料流程的新大小，以位元組數表示</span><span class="sxs-lookup"><span data-stu-id="bf3ae-111">New size of the stream as a number of bytes</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf3ae-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf3ae-112">Return value</span></span>

<span data-ttu-id="bf3ae-113">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bf3ae-113">The return value is an **HRESULT**.</span></span> <span data-ttu-id="bf3ae-114">值為 S \_ OK 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="bf3ae-114">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf3ae-115">備註</span><span class="sxs-lookup"><span data-stu-id="bf3ae-115">Remarks</span></span>

<span data-ttu-id="bf3ae-116">**IByteBuffer：： SetSize** 方法會變更資料流程物件的大小。</span><span class="sxs-lookup"><span data-stu-id="bf3ae-116">The **IByteBuffer::SetSize** method changes the size of the stream object.</span></span> <span data-ttu-id="bf3ae-117">呼叫這個方法來預先配置資料流程的空間。</span><span class="sxs-lookup"><span data-stu-id="bf3ae-117">Call this method to preallocate space for the stream.</span></span> <span data-ttu-id="bf3ae-118">如果 *libNewSize* 參數大於目前的資料流程大小，則會以位元組的未定義值填滿中間的空間，將資料流程延伸至指定的大小。</span><span class="sxs-lookup"><span data-stu-id="bf3ae-118">If the *libNewSize* parameter is larger than the current stream size, the stream is extended to the indicated size by filling the intervening space with bytes of undefined value.</span></span> <span data-ttu-id="bf3ae-119">如果 seek 指標超過目前的資料流程結尾，則這項作業類似于 [**IByteBuffer：： Write**](ibytebuffer-write.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="bf3ae-119">This operation is similar to the [**IByteBuffer::Write**](ibytebuffer-write.md) method if the seek pointer is past the current end-of-stream.</span></span>

<span data-ttu-id="bf3ae-120">如果 *libNewSize* 參數小於目前的資料流程，則資料流程會截斷為指定的大小。</span><span class="sxs-lookup"><span data-stu-id="bf3ae-120">If the *libNewSize* parameter is smaller than the current stream, then the stream is truncated to the indicated size.</span></span>

<span data-ttu-id="bf3ae-121">搜尋指標不受資料流程大小變更的影響。</span><span class="sxs-lookup"><span data-stu-id="bf3ae-121">The seek pointer is not affected by the change in stream size.</span></span>

<span data-ttu-id="bf3ae-122">呼叫 **IByteBuffer：： SetSize** 可能是嘗試取得大型連續空間區塊的有效方式。</span><span class="sxs-lookup"><span data-stu-id="bf3ae-122">Calling **IByteBuffer::SetSize** can be an effective way of trying to obtain a large chunk of contiguous space.</span></span>

## <a name="examples"></a><span data-ttu-id="bf3ae-123">範例</span><span class="sxs-lookup"><span data-stu-id="bf3ae-123">Examples</span></span>

<span data-ttu-id="bf3ae-124">下列範例會示範如何設定緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="bf3ae-124">The following example shows setting the buffer size.</span></span>


```C++
LONG     lNewSize = 256;
HRESULT  hr;

// Change the buffer size.
hr = pIByteBuff->SetSize(lNewSize);
if (FAILED(hr))
  printf("Failed IByteBuffer::SetSize\n");
```



## <a name="requirements"></a><span data-ttu-id="bf3ae-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf3ae-125">Requirements</span></span>



| <span data-ttu-id="bf3ae-126">需求</span><span class="sxs-lookup"><span data-stu-id="bf3ae-126">Requirement</span></span> | <span data-ttu-id="bf3ae-127">值</span><span class="sxs-lookup"><span data-stu-id="bf3ae-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf3ae-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf3ae-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bf3ae-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf3ae-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bf3ae-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf3ae-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bf3ae-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf3ae-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf3ae-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="bf3ae-132">End of client support</span></span><br/>    | <span data-ttu-id="bf3ae-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf3ae-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="bf3ae-134">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="bf3ae-134">End of server support</span></span><br/>    | <span data-ttu-id="bf3ae-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf3ae-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="bf3ae-136">標頭</span><span class="sxs-lookup"><span data-stu-id="bf3ae-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf3ae-137"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf3ae-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf3ae-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bf3ae-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf3ae-139"><dt>Scardssp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bf3ae-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bf3ae-140">DLL</span><span class="sxs-lookup"><span data-stu-id="bf3ae-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf3ae-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf3ae-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf3ae-142">IID</span><span class="sxs-lookup"><span data-stu-id="bf3ae-142">IID</span></span><br/>                      | <span data-ttu-id="bf3ae-143">IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="bf3ae-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

