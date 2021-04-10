---
description: 限制存取緩衝區物件中指定的位元組範圍。
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: 'IByteBuffer：： LockRegion 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.LockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae227d11892b604ab1382cb328dc492e4596f278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194520"
---
# <a name="ibytebufferlockregion-method"></a><span data-ttu-id="29bc3-103">IByteBuffer：： LockRegion 方法</span><span class="sxs-lookup"><span data-stu-id="29bc3-103">IByteBuffer::LockRegion method</span></span>

<span data-ttu-id="29bc3-104">\[**LockRegion** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="29bc3-104">\[The **LockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="29bc3-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="29bc3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="29bc3-106">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="29bc3-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="29bc3-107">**LockRegion** 方法會限制存取緩衝區物件中指定的位元組範圍。</span><span class="sxs-lookup"><span data-stu-id="29bc3-107">The **LockRegion** method restricts access to a specified range of bytes in the buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="29bc3-108">語法</span><span class="sxs-lookup"><span data-stu-id="29bc3-108">Syntax</span></span>


```C++
HRESULT LockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="29bc3-109">參數</span><span class="sxs-lookup"><span data-stu-id="29bc3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29bc3-110">*libOffset* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29bc3-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29bc3-111">整數，指定範圍開頭的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="29bc3-111">Integer that specifies the byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="29bc3-112">*cb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29bc3-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29bc3-113">整數，指定要限制的範圍長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="29bc3-113">Integer that specifies the length of the range, in bytes, to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="29bc3-114">*dwLockType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29bc3-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29bc3-115">指定存取範圍時所要求的限制。</span><span class="sxs-lookup"><span data-stu-id="29bc3-115">Specifies the restrictions being requested on accessing the range.</span></span> <span data-ttu-id="29bc3-116">這可以是下表中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="29bc3-116">This can be one of the values in the following table.</span></span>



| <span data-ttu-id="29bc3-117">值</span><span class="sxs-lookup"><span data-stu-id="29bc3-117">Value</span></span>                                                                                                                                                            | <span data-ttu-id="29bc3-118">意義</span><span class="sxs-lookup"><span data-stu-id="29bc3-118">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <span data-ttu-id="29bc3-119"><dt>**鎖定 \_ 寫入**</dt></span><span class="sxs-lookup"><span data-stu-id="29bc3-119"><dt>**LOCK\_WRITE**</dt></span></span> </dl>             | <span data-ttu-id="29bc3-120">您可以開啟指定的位元組範圍並讀取任意次數，但除非授與此鎖定的擁有者，否則不允許寫入鎖定範圍。</span><span class="sxs-lookup"><span data-stu-id="29bc3-120">The specified range of bytes can be opened and read any number of times, but writing to the locked range is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <span data-ttu-id="29bc3-121"><dt>**\_獨佔鎖定**</dt></span><span class="sxs-lookup"><span data-stu-id="29bc3-121"><dt>**LOCK\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="29bc3-122">除了授與此鎖定的擁有者之外，禁止寫入至指定的位元組範圍。</span><span class="sxs-lookup"><span data-stu-id="29bc3-122">Writing to the specified range of bytes is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <span data-ttu-id="29bc3-123"><dt>**鎖定 \_ ONLYONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="29bc3-123"><dt>**LOCK\_ONLYONCE**</dt></span></span> </dl>    | <span data-ttu-id="29bc3-124">如果授與此鎖定，就不能 \_ 取得範圍的其他鎖定 ONLYONCE 鎖定。</span><span class="sxs-lookup"><span data-stu-id="29bc3-124">If this lock is granted, no other LOCK\_ONLYONCE lock can be obtained on the range.</span></span> <span data-ttu-id="29bc3-125">此鎖定類型通常是某些其他鎖定類型的別名。</span><span class="sxs-lookup"><span data-stu-id="29bc3-125">Usually this lock type is an alias for some other lock type.</span></span> <span data-ttu-id="29bc3-126">因此，特定的執行可以有與此鎖定類型相關聯的其他行為。</span><span class="sxs-lookup"><span data-stu-id="29bc3-126">Thus, specific implementations can have additional behavior associated with this lock type.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29bc3-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="29bc3-127">Return value</span></span>

<span data-ttu-id="29bc3-128">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="29bc3-128">The return value is an **HRESULT**.</span></span> <span data-ttu-id="29bc3-129">值為 S \_ OK 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="29bc3-129">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="29bc3-130">備註</span><span class="sxs-lookup"><span data-stu-id="29bc3-130">Remarks</span></span>

<span data-ttu-id="29bc3-131">位元組範圍可延伸超過資料流程的目前結尾。</span><span class="sxs-lookup"><span data-stu-id="29bc3-131">The byte range can extend past the current end of the stream.</span></span> <span data-ttu-id="29bc3-132">鎖定超過資料流程的結尾，會因為資料流程的不同實例之間的通訊方法而有所説明，而不會變更實際上是資料流程一部分的資料。</span><span class="sxs-lookup"><span data-stu-id="29bc3-132">Locking beyond the end of a stream is useful as a method of communication between different instances of the stream without changing data that is actually part of the stream.</span></span>

<span data-ttu-id="29bc3-133">可支援三種類型的鎖定：鎖定以排除其他寫入器、鎖定排除其他讀取器或寫入器，以及只允許一個要求者取得指定範圍的鎖定，這通常是其他兩種鎖定類型之一的別名。</span><span class="sxs-lookup"><span data-stu-id="29bc3-133">Three types of locking can be supported: locking to exclude other writers, locking to exclude other readers or writers, and locking that allows only one requester to obtain a lock on the given range, which is usually an alias for one of the other two lock types.</span></span> <span data-ttu-id="29bc3-134">給定的資料流程實例可能會支援前兩種類型的其中一種，或兩者都支援。</span><span class="sxs-lookup"><span data-stu-id="29bc3-134">A given stream instance might support either of the first two types, or both.</span></span> <span data-ttu-id="29bc3-135">鎖定類型是由 *dwLockType* 所指定，並使用 [**LOCKTYPE**](/windows/win32/api/objidl/ne-objidl-locktype) 列舉中的值。</span><span class="sxs-lookup"><span data-stu-id="29bc3-135">The lock type is specified by *dwLockType*, using a value from the [**LOCKTYPE**](/windows/win32/api/objidl/ne-objidl-locktype) enumeration.</span></span>

<span data-ttu-id="29bc3-136">使用 **LockRegion** 鎖定的任何區域，稍後都必須使用與 *libOffset*、 *cb* 和 *dwLockType* 參數完全相同的值來呼叫 [**IByteBuffer：： UnlockRegion**](ibytebuffer-unlockregion.md) ，以明確解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="29bc3-136">Any region locked with **LockRegion** must later be explicitly unlocked by calling [**IByteBuffer::UnlockRegion**](ibytebuffer-unlockregion.md) with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="29bc3-137">區域必須在串流發行之前解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="29bc3-137">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="29bc3-138">兩個連續的區域不能個別鎖定，然後使用單一解除鎖定呼叫來解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="29bc3-138">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="29bc3-139">範例</span><span class="sxs-lookup"><span data-stu-id="29bc3-139">Examples</span></span>

<span data-ttu-id="29bc3-140">下列範例顯示限制對位元組範圍的存取。</span><span class="sxs-lookup"><span data-stu-id="29bc3-140">The following example shows restricting access to a range of bytes.</span></span>


```C++
HRESULT  hr;

// Lock a region.
hr = pIByteBuff->LockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::LockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="29bc3-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="29bc3-141">Requirements</span></span>



| <span data-ttu-id="29bc3-142">需求</span><span class="sxs-lookup"><span data-stu-id="29bc3-142">Requirement</span></span> | <span data-ttu-id="29bc3-143">值</span><span class="sxs-lookup"><span data-stu-id="29bc3-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29bc3-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29bc3-144">Minimum supported client</span></span><br/> | <span data-ttu-id="29bc3-145">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29bc3-145">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="29bc3-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29bc3-146">Minimum supported server</span></span><br/> | <span data-ttu-id="29bc3-147">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29bc3-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="29bc3-148">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="29bc3-148">End of client support</span></span><br/>    | <span data-ttu-id="29bc3-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="29bc3-149">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="29bc3-150">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="29bc3-150">End of server support</span></span><br/>    | <span data-ttu-id="29bc3-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29bc3-151">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="29bc3-152">標頭</span><span class="sxs-lookup"><span data-stu-id="29bc3-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="29bc3-153"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="29bc3-153"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="29bc3-154">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="29bc3-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="29bc3-155"><dt>Scardssp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="29bc3-155"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="29bc3-156">DLL</span><span class="sxs-lookup"><span data-stu-id="29bc3-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29bc3-157"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29bc3-157"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="29bc3-158">IID</span><span class="sxs-lookup"><span data-stu-id="29bc3-158">IID</span></span><br/>                      | <span data-ttu-id="29bc3-159">IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="29bc3-159">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

