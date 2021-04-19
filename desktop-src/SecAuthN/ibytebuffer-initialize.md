---
description: Initialize 方法會準備要使用的 IByteBuffer 物件。 在呼叫 IByteBuffer 介面中的任何其他方法之前，必須先呼叫這個方法。
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: 'IByteBuffer：： Initialize 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 245f9282174ddeef66b130597f0f20ddf21ededc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990410"
---
# <a name="ibytebufferinitialize-method"></a><span data-ttu-id="8831a-104">IByteBuffer：： Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="8831a-104">IByteBuffer::Initialize method</span></span>

<span data-ttu-id="8831a-105">\[**Initialize** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="8831a-105">\[The **Initialize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8831a-106">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="8831a-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later.</span></span> <span data-ttu-id="8831a-107">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="8831a-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="8831a-108">**Initialize** 方法會準備要使用的 [**IByteBuffer**](ibytebuffer.md)物件。</span><span class="sxs-lookup"><span data-stu-id="8831a-108">The **Initialize** method prepares the [**IByteBuffer**](ibytebuffer.md) object for use.</span></span> <span data-ttu-id="8831a-109">在呼叫 **IByteBuffer** 介面中的任何其他方法之前，必須先呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="8831a-109">This method must be called prior to calling any other methods in the **IByteBuffer** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8831a-110">語法</span><span class="sxs-lookup"><span data-stu-id="8831a-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a><span data-ttu-id="8831a-111">參數</span><span class="sxs-lookup"><span data-stu-id="8831a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8831a-112">*lSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8831a-112">*lSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8831a-113">資料流程所要包含之資料的初始大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8831a-113">Initial size, in bytes, of the data the stream is to contain.</span></span>

</dd> <dt>

<span data-ttu-id="8831a-114">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8831a-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8831a-115">如果不是 **Null**，則為要寫入資料流程的初始資料。</span><span class="sxs-lookup"><span data-stu-id="8831a-115">If not **NULL**, the initial data to write to the stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8831a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8831a-116">Return value</span></span>

<span data-ttu-id="8831a-117">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="8831a-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="8831a-118">值為 S \_ OK 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="8831a-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8831a-119">備註</span><span class="sxs-lookup"><span data-stu-id="8831a-119">Remarks</span></span>

<span data-ttu-id="8831a-120">使用新的 [**IByteBuffer**](ibytebuffer.md) 資料流程時，請在使用任何其他 **IByteBuffer** 方法之前呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="8831a-120">When using a new [**IByteBuffer**](ibytebuffer.md) stream, call this method prior to using any of the other **IByteBuffer** methods.</span></span>

## <a name="examples"></a><span data-ttu-id="8831a-121">範例</span><span class="sxs-lookup"><span data-stu-id="8831a-121">Examples</span></span>

<span data-ttu-id="8831a-122">下列範例示範如何初始化 [**IByteBuffer**](ibytebuffer.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="8831a-122">The following example shows initializing the [**IByteBuffer**](ibytebuffer.md) object.</span></span>


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
```



## <a name="requirements"></a><span data-ttu-id="8831a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="8831a-123">Requirements</span></span>



| <span data-ttu-id="8831a-124">需求</span><span class="sxs-lookup"><span data-stu-id="8831a-124">Requirement</span></span> | <span data-ttu-id="8831a-125">值</span><span class="sxs-lookup"><span data-stu-id="8831a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8831a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8831a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8831a-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8831a-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8831a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8831a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8831a-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8831a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8831a-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8831a-130">End of client support</span></span><br/>    | <span data-ttu-id="8831a-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8831a-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8831a-132">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="8831a-132">End of server support</span></span><br/>    | <span data-ttu-id="8831a-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8831a-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8831a-134">標頭</span><span class="sxs-lookup"><span data-stu-id="8831a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8831a-135"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="8831a-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8831a-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8831a-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="8831a-137"><dt>Scardssp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8831a-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8831a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8831a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8831a-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8831a-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8831a-140">IID</span><span class="sxs-lookup"><span data-stu-id="8831a-140">IID</span></span><br/>                      | <span data-ttu-id="8831a-141">IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="8831a-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

