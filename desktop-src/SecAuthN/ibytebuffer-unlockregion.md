---
description: 移除先前使用 IByteBuffer：： LockRegion 限制之位元組範圍的存取限制。
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: 'IByteBuffer：： UnlockRegion 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92e49ba000177326ad14d3b83002613a15e96e18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945039"
---
# <a name="ibytebufferunlockregion-method"></a><span data-ttu-id="db565-103">IByteBuffer：： UnlockRegion 方法</span><span class="sxs-lookup"><span data-stu-id="db565-103">IByteBuffer::UnlockRegion method</span></span>

<span data-ttu-id="db565-104">\[**UnlockRegion** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="db565-104">\[The **UnlockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="db565-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="db565-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="db565-106">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="db565-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="db565-107">**UnlockRegion** 方法會移除先前使用 [**IByteBuffer：： LockRegion**](ibytebuffer-lockregion.md)限制之位元組範圍的存取限制。</span><span class="sxs-lookup"><span data-stu-id="db565-107">The **UnlockRegion** method removes the access restriction on a range of bytes previously restricted by using [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="db565-108">語法</span><span class="sxs-lookup"><span data-stu-id="db565-108">Syntax</span></span>


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="db565-109">參數</span><span class="sxs-lookup"><span data-stu-id="db565-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db565-110">*libOffset* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db565-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db565-111">範圍開頭的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="db565-111">Byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="db565-112">*cb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db565-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db565-113">要限制的範圍長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="db565-113">Length, in bytes, of the range to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="db565-114">*dwLockType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db565-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db565-115">先前放置於範圍內的存取限制。</span><span class="sxs-lookup"><span data-stu-id="db565-115">Access restrictions previously placed on the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db565-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="db565-116">Return value</span></span>

<span data-ttu-id="db565-117">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="db565-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="db565-118">值為 S \_ OK 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="db565-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="db565-119">備註</span><span class="sxs-lookup"><span data-stu-id="db565-119">Remarks</span></span>

<span data-ttu-id="db565-120">**IByteBuffer：： UnlockRegion** 方法會解除鎖定先前使用 [**IByteBuffer：： LockRegion**](ibytebuffer-lockregion.md)方法鎖定的區域。</span><span class="sxs-lookup"><span data-stu-id="db565-120">The **IByteBuffer::UnlockRegion** method unlocks a region previously locked by using the [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md) method.</span></span> <span data-ttu-id="db565-121">您稍後必須使用與 *libOffset*、 *cb* 和 *dwLockType* 參數完全相同的值來呼叫 **IByteBuffer：： UnlockRegion** ，以明確解除鎖定區域的鎖定。</span><span class="sxs-lookup"><span data-stu-id="db565-121">Locked regions must later be explicitly unlocked by calling **IByteBuffer::UnlockRegion** with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="db565-122">區域必須在串流發行之前解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="db565-122">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="db565-123">兩個連續的區域不能個別鎖定，然後使用單一解除鎖定呼叫來解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="db565-123">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="db565-124">範例</span><span class="sxs-lookup"><span data-stu-id="db565-124">Examples</span></span>

<span data-ttu-id="db565-125">下列範例顯示解除鎖定某個範圍的位元組。</span><span class="sxs-lookup"><span data-stu-id="db565-125">The following example shows unlocking a range of bytes.</span></span>


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="db565-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="db565-126">Requirements</span></span>



| <span data-ttu-id="db565-127">需求</span><span class="sxs-lookup"><span data-stu-id="db565-127">Requirement</span></span> | <span data-ttu-id="db565-128">值</span><span class="sxs-lookup"><span data-stu-id="db565-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db565-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db565-129">Minimum supported client</span></span><br/> | <span data-ttu-id="db565-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db565-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="db565-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db565-131">Minimum supported server</span></span><br/> | <span data-ttu-id="db565-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db565-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db565-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="db565-133">End of client support</span></span><br/>    | <span data-ttu-id="db565-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="db565-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="db565-135">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="db565-135">End of server support</span></span><br/>    | <span data-ttu-id="db565-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="db565-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="db565-137">標頭</span><span class="sxs-lookup"><span data-stu-id="db565-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="db565-138"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="db565-138"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="db565-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="db565-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="db565-140"><dt>Scardssp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="db565-140"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="db565-141">DLL</span><span class="sxs-lookup"><span data-stu-id="db565-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db565-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db565-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="db565-143">IID</span><span class="sxs-lookup"><span data-stu-id="db565-143">IID</span></span><br/>                      | <span data-ttu-id="db565-144">IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="db565-144">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

