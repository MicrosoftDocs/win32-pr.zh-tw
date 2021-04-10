---
description: CopyTo 方法會將指定的位元組數目從物件中目前的搜尋指標複製到另一個物件中目前的搜尋指標。
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: 'IByteBuffer：： CopyTo 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f6b35a2cfa2de459bb5e7acfcb9853e83ae0a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194523"
---
# <a name="ibytebuffercopyto-method"></a><span data-ttu-id="9c477-103">IByteBuffer：： CopyTo 方法</span><span class="sxs-lookup"><span data-stu-id="9c477-103">IByteBuffer::CopyTo method</span></span>

<span data-ttu-id="9c477-104">\[**CopyTo** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="9c477-104">\[The **CopyTo** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9c477-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="9c477-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9c477-106">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="9c477-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="9c477-107">**CopyTo** 方法會將指定的位元組數目從物件中目前的搜尋指標複製到另一個物件中目前的搜尋指標。</span><span class="sxs-lookup"><span data-stu-id="9c477-107">The **CopyTo** method copies a specified number of bytes from the current seek pointer in the object to the current seek pointer in another object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c477-108">語法</span><span class="sxs-lookup"><span data-stu-id="9c477-108">Syntax</span></span>


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="9c477-109">參數</span><span class="sxs-lookup"><span data-stu-id="9c477-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c477-110">*pByteBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9c477-110">*pByteBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c477-111">指向目的地資料流程。</span><span class="sxs-lookup"><span data-stu-id="9c477-111">Points to the destination stream.</span></span> <span data-ttu-id="9c477-112">*PByteBuffer* 所指向的資料流程可以是新的資料流程或來來源資料流的複製。</span><span class="sxs-lookup"><span data-stu-id="9c477-112">The stream pointed to by *pByteBuffer* can be a new stream or a clone of the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="9c477-113">*cb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9c477-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c477-114">要從來來源資料流複製的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="9c477-114">Number of bytes to copy from the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="9c477-115">*pcbRead* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9c477-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c477-116">位置的指標，此方法會寫入從來源讀取的實際位元組數目。</span><span class="sxs-lookup"><span data-stu-id="9c477-116">Pointer to the location where this method writes the actual number of bytes read from the source.</span></span> <span data-ttu-id="9c477-117">您可以將 this 指標設為 **Null** ，表示您對此值不感興趣。</span><span class="sxs-lookup"><span data-stu-id="9c477-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="9c477-118">在此情況下，這個方法不會提供實際讀取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="9c477-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="9c477-119">*pcbWritten* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9c477-119">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c477-120">位置的指標，此方法會寫入寫入目的地的實際位元組數目。</span><span class="sxs-lookup"><span data-stu-id="9c477-120">Pointer to the location where this method writes the actual number of bytes written to the destination.</span></span> <span data-ttu-id="9c477-121">您可以將 this 指標設為 **Null** ，表示您對此值不感興趣。</span><span class="sxs-lookup"><span data-stu-id="9c477-121">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="9c477-122">在此情況下，這個方法不會提供實際寫入的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="9c477-122">In this case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c477-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c477-123">Return value</span></span>

<span data-ttu-id="9c477-124">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="9c477-124">The return value is an **HRESULT**.</span></span> <span data-ttu-id="9c477-125">值為 S \_ OK 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="9c477-125">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c477-126">備註</span><span class="sxs-lookup"><span data-stu-id="9c477-126">Remarks</span></span>

<span data-ttu-id="9c477-127">這個方法會將指定的位元組從某個資料流程複製到另一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="9c477-127">This method copies the specified bytes from one stream to another.</span></span> <span data-ttu-id="9c477-128">它也可以用來將資料流程複製到本身。</span><span class="sxs-lookup"><span data-stu-id="9c477-128">It can also be used to copy a stream to itself.</span></span> <span data-ttu-id="9c477-129">每個資料流程實例中的 seek 指標都會針對讀取或寫入的位元組數進行調整。</span><span class="sxs-lookup"><span data-stu-id="9c477-129">The seek pointer in each stream instance is adjusted for the number of bytes read or written.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c477-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c477-130">Requirements</span></span>



| <span data-ttu-id="9c477-131">需求</span><span class="sxs-lookup"><span data-stu-id="9c477-131">Requirement</span></span> | <span data-ttu-id="9c477-132">值</span><span class="sxs-lookup"><span data-stu-id="9c477-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c477-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c477-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9c477-134">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c477-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9c477-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c477-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9c477-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c477-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c477-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9c477-137">End of client support</span></span><br/>    | <span data-ttu-id="9c477-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9c477-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9c477-139">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9c477-139">End of server support</span></span><br/>    | <span data-ttu-id="9c477-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9c477-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9c477-141">標頭</span><span class="sxs-lookup"><span data-stu-id="9c477-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c477-142"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9c477-142"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c477-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9c477-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="9c477-144"><dt>Scardssp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9c477-144"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9c477-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9c477-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c477-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c477-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9c477-147">IID</span><span class="sxs-lookup"><span data-stu-id="9c477-147">IID</span></span><br/>                      | <span data-ttu-id="9c477-148">IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="9c477-148">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

