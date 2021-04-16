---
description: Read 方法會從緩衝區物件中，將指定的位元組數目從目前的 seek 指標開始讀取到記憶體中。
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: 'IByteBuffer：： Read 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Read
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0574fb640d60fd8af824ff54abce5d109675ba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194518"
---
# <a name="ibytebufferread-method"></a><span data-ttu-id="ab7ad-103">IByteBuffer：： Read 方法</span><span class="sxs-lookup"><span data-stu-id="ab7ad-103">IByteBuffer::Read method</span></span>

<span data-ttu-id="ab7ad-104">\[**Read** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ab7ad-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ab7ad-106">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="ab7ad-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="ab7ad-107">**Read** 方法會從緩衝區物件中，將指定的位元組數目從目前的 seek 指標開始讀取到記憶體中。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-107">The **Read** method reads a specified number of bytes from the buffer object into memory starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab7ad-108">語法</span><span class="sxs-lookup"><span data-stu-id="ab7ad-108">Syntax</span></span>


```C++
HRESULT Read(
  [out] BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="ab7ad-109">參數</span><span class="sxs-lookup"><span data-stu-id="ab7ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab7ad-110">*pByte* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ab7ad-110">*pByte* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab7ad-111">指向讀取資料流程資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-111">Points to the buffer into which the stream data is read.</span></span> <span data-ttu-id="ab7ad-112">如果發生錯誤，此值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-112">If an error occurs, this value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ab7ad-113">*cb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab7ad-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab7ad-114">嘗試從資料流程物件讀取的資料位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-114">Number of bytes of data to attempt to read from the stream object.</span></span>

</dd> <dt>

<span data-ttu-id="ab7ad-115">*pcbRead* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ab7ad-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab7ad-116">**長** 變數的位址，此變數會接收從資料流程物件讀取的實際位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-116">Address of a **LONG** variable that receives the actual number of bytes read from the stream object.</span></span> <span data-ttu-id="ab7ad-117">您可以將 this 指標設為 **Null** ，表示您對此值不感興趣。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="ab7ad-118">在此情況下，這個方法不會提供實際讀取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab7ad-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab7ad-119">Return value</span></span>

<span data-ttu-id="ab7ad-120">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="ab7ad-121">值為 S \_ OK 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab7ad-122">備註</span><span class="sxs-lookup"><span data-stu-id="ab7ad-122">Remarks</span></span>

<span data-ttu-id="ab7ad-123">這個方法會將此資料流程物件的位元組讀入記憶體中。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-123">This method reads bytes from this stream object into memory.</span></span> <span data-ttu-id="ab7ad-124">資料流程物件必須以 STGM \_ 讀取模式開啟。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-124">The stream object must be opened in STGM\_READ mode.</span></span> <span data-ttu-id="ab7ad-125">這個方法會以讀取的實際位元組數目來調整 seek 指標。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-125">This method adjusts the seek pointer by the actual number of bytes read.</span></span>

<span data-ttu-id="ab7ad-126">實際讀取的位元組數目也會在 *pcbRead* 參數中傳回。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-126">The number of bytes actually read is also returned in the *pcbRead* parameter.</span></span>

<span data-ttu-id="ab7ad-127">給呼叫者的注意事項</span><span class="sxs-lookup"><span data-stu-id="ab7ad-127">Notes to Callers</span></span>

<span data-ttu-id="ab7ad-128">如果發生錯誤，或是在讀取作業期間到達資料流程的結尾，則讀取的實際位元組數目可能會少於所要求的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-128">The actual number of bytes read can be fewer than the number of bytes requested if an error occurs or if the end of the stream is reached during the read operation.</span></span>

<span data-ttu-id="ab7ad-129">如果在讀取期間到達資料流程的結尾，某些可能會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-129">Some implementations might return an error if the end of the stream is reached during the read.</span></span> <span data-ttu-id="ab7ad-130">您必須準備好處理資料流程讀取結束時的錯誤傳回或 S \_ OK 傳回值。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-130">You must be prepared to deal with the error return or S\_OK return values on end of stream reads.</span></span>

## <a name="examples"></a><span data-ttu-id="ab7ad-131">範例</span><span class="sxs-lookup"><span data-stu-id="ab7ad-131">Examples</span></span>

<span data-ttu-id="ab7ad-132">下列範例會示範如何讀取緩衝區中的位元組。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-132">The following example shows reading bytes from the buffer.</span></span>


```C++
BYTE     byAtr[32];
long     lBytesRead, i;
HRESULT  hr;

// pAtr is a pointer to a previously instantiated IByteBuffer.
// It was used in an earlier call by ISCard::get_Atr.
// Use IByteBuffer::Read to access the retrieved ATR bytes.
hr = pAtr->Read(byAtr, 32, &lBytesRead);
// Use the ATR value. (This example merely displays the bytes.)
for ( i = 0; i < lBytesRead; i++)
    printf("%c", *(byAtr + i));
printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="ab7ad-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab7ad-133">Requirements</span></span>



| <span data-ttu-id="ab7ad-134">需求</span><span class="sxs-lookup"><span data-stu-id="ab7ad-134">Requirement</span></span> | <span data-ttu-id="ab7ad-135">值</span><span class="sxs-lookup"><span data-stu-id="ab7ad-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab7ad-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab7ad-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ab7ad-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab7ad-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ab7ad-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab7ad-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ab7ad-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab7ad-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ab7ad-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ab7ad-140">End of client support</span></span><br/>    | <span data-ttu-id="ab7ad-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ab7ad-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ab7ad-142">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ab7ad-142">End of server support</span></span><br/>    | <span data-ttu-id="ab7ad-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ab7ad-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ab7ad-144">標頭</span><span class="sxs-lookup"><span data-stu-id="ab7ad-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab7ad-145"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab7ad-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ab7ad-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ab7ad-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="ab7ad-147"><dt>Scardssp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ab7ad-147"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ab7ad-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ab7ad-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab7ad-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab7ad-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ab7ad-150">IID</span><span class="sxs-lookup"><span data-stu-id="ab7ad-150">IID</span></span><br/>                      | <span data-ttu-id="ab7ad-151">IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="ab7ad-151">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

