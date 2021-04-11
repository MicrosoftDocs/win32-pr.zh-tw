---
description: Clone 方法會使用它自己的 seek 指標來建立新的物件，該物件會參考與原始 IByteBuffer 物件相同的位元組。
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: 'IByteBuffer：： Clone 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Clone
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d994ef55665b03da2a7d657689682f893fdf071f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194078"
---
# <a name="ibytebufferclone-method"></a><span data-ttu-id="50f5b-103">IByteBuffer：： Clone 方法</span><span class="sxs-lookup"><span data-stu-id="50f5b-103">IByteBuffer::Clone method</span></span>

<span data-ttu-id="50f5b-104">\[**複製** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="50f5b-104">\[The **Clone** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="50f5b-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="50f5b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="50f5b-106">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="50f5b-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="50f5b-107">**Clone** 方法會使用它自己的 seek 指標來建立新的物件，該物件會參考與原始 [**IByteBuffer**](ibytebuffer.md)物件相同的位元組。</span><span class="sxs-lookup"><span data-stu-id="50f5b-107">The **Clone** method creates a new object with its own seek pointer that references the same bytes as the original [**IByteBuffer**](ibytebuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="50f5b-108">語法</span><span class="sxs-lookup"><span data-stu-id="50f5b-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="50f5b-109">參數</span><span class="sxs-lookup"><span data-stu-id="50f5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50f5b-110">*ppByteBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="50f5b-110">*ppByteBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50f5b-111">成功時，指向新資料流程物件之 [**IByteBuffer**](ibytebuffer.md) 指標的位置。</span><span class="sxs-lookup"><span data-stu-id="50f5b-111">When successful, points to the location of an [**IByteBuffer**](ibytebuffer.md) pointer to the new stream object.</span></span> <span data-ttu-id="50f5b-112">當您完成使用 **IByteBuffer** 指標時，請呼叫 [**IUnknown：： release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 函式來釋放它。</span><span class="sxs-lookup"><span data-stu-id="50f5b-112">When you have finished using the **IByteBuffer** pointer, release it by calling the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) function.</span></span> <span data-ttu-id="50f5b-113">如果發生錯誤，此參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="50f5b-113">If an error occurs, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50f5b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="50f5b-114">Return value</span></span>

<span data-ttu-id="50f5b-115">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="50f5b-115">The return value is an **HRESULT**.</span></span> <span data-ttu-id="50f5b-116">值為 S \_ OK 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="50f5b-116">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="50f5b-117">備註</span><span class="sxs-lookup"><span data-stu-id="50f5b-117">Remarks</span></span>

<span data-ttu-id="50f5b-118">這個方法會建立新的資料流程物件來存取相同的位元組，但使用個別的 seek 指標。</span><span class="sxs-lookup"><span data-stu-id="50f5b-118">This method creates a new stream object for accessing the same bytes but using a separate seek pointer.</span></span> <span data-ttu-id="50f5b-119">新的資料流程物件會看到與來來源資料流物件相同的資料。</span><span class="sxs-lookup"><span data-stu-id="50f5b-119">The new stream object sees the same data as the source stream object.</span></span> <span data-ttu-id="50f5b-120">寫入至一個物件的變更會立即顯示在另一個物件中。</span><span class="sxs-lookup"><span data-stu-id="50f5b-120">Changes written to one object are immediately visible in the other.</span></span> <span data-ttu-id="50f5b-121">範圍鎖定會在資料流程物件之間共用。</span><span class="sxs-lookup"><span data-stu-id="50f5b-121">Range locking is shared between the stream objects.</span></span>

<span data-ttu-id="50f5b-122">複製的資料流程實例中搜尋指標的初始設定，與複製作業時原始資料流程中的搜尋指標目前設定相同。</span><span class="sxs-lookup"><span data-stu-id="50f5b-122">The initial setting of the seek pointer in the cloned stream instance is the same as the current setting of the seek pointer in the original stream at the time of the clone operation.</span></span>

## <a name="examples"></a><span data-ttu-id="50f5b-123">範例</span><span class="sxs-lookup"><span data-stu-id="50f5b-123">Examples</span></span>

<span data-ttu-id="50f5b-124">下列範例顯示覆制 [**IByteBuffer**](ibytebuffer.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="50f5b-124">The following example shows cloning the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT  hr;

// Clone the buffer.
hr = pIByteBuff->Clone(&pIByteClone);
if (FAILED(hr))
  printf("Failed IByteBuffer::Clone\n");
```



## <a name="requirements"></a><span data-ttu-id="50f5b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="50f5b-125">Requirements</span></span>



| <span data-ttu-id="50f5b-126">需求</span><span class="sxs-lookup"><span data-stu-id="50f5b-126">Requirement</span></span> | <span data-ttu-id="50f5b-127">值</span><span class="sxs-lookup"><span data-stu-id="50f5b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50f5b-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50f5b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="50f5b-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50f5b-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="50f5b-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50f5b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="50f5b-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50f5b-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50f5b-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="50f5b-132">End of client support</span></span><br/>    | <span data-ttu-id="50f5b-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="50f5b-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="50f5b-134">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="50f5b-134">End of server support</span></span><br/>    | <span data-ttu-id="50f5b-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="50f5b-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="50f5b-136">標頭</span><span class="sxs-lookup"><span data-stu-id="50f5b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="50f5b-137"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="50f5b-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="50f5b-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="50f5b-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="50f5b-139"><dt>Scardssp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="50f5b-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="50f5b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="50f5b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50f5b-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50f5b-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="50f5b-142">IID</span><span class="sxs-lookup"><span data-stu-id="50f5b-142">IID</span></span><br/>                      | <span data-ttu-id="50f5b-143">IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="50f5b-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

