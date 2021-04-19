---
description: Commit 方法可確保在交易模式中開啟之物件所做的任何變更，都會反映在父儲存體中。
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: 'IByteBuffer：： Commit 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 066925361d0ee4391bcd1eaafe33e0ae2d4b9120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985282"
---
# <a name="ibytebuffercommit-method"></a><span data-ttu-id="e7f86-103">IByteBuffer：： Commit 方法</span><span class="sxs-lookup"><span data-stu-id="e7f86-103">IByteBuffer::Commit method</span></span>

<span data-ttu-id="e7f86-104">\[**Commit** 方法可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="e7f86-104">\[The **Commit** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e7f86-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="e7f86-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e7f86-106">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="e7f86-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="e7f86-107">**Commit** 方法可確保在交易模式中開啟之物件所做的任何變更，都會反映在父儲存體中。</span><span class="sxs-lookup"><span data-stu-id="e7f86-107">The **Commit** method ensures that any changes made to an object open in transacted mode are reflected in the parent storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7f86-108">語法</span><span class="sxs-lookup"><span data-stu-id="e7f86-108">Syntax</span></span>


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e7f86-109">參數</span><span class="sxs-lookup"><span data-stu-id="e7f86-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7f86-110">*grfCommitFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7f86-110">*grfCommitFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f86-111">控制資料流物件的變更如何認可。</span><span class="sxs-lookup"><span data-stu-id="e7f86-111">Controls how the changes for the stream object are committed.</span></span> <span data-ttu-id="e7f86-112">如需這些值的定義，請參閱 STGC 列舉。</span><span class="sxs-lookup"><span data-stu-id="e7f86-112">For a definition of these values, see the STGC enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7f86-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7f86-113">Return value</span></span>

<span data-ttu-id="e7f86-114">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="e7f86-114">The return value is an **HRESULT**.</span></span> <span data-ttu-id="e7f86-115">值為 S \_ OK 表示呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="e7f86-115">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7f86-116">備註</span><span class="sxs-lookup"><span data-stu-id="e7f86-116">Remarks</span></span>

<span data-ttu-id="e7f86-117">這個方法可確保在交易模式中開啟之資料流程物件的變更會反映在父儲存體中。</span><span class="sxs-lookup"><span data-stu-id="e7f86-117">This method ensures that changes to a stream object opened in transacted mode are reflected in the parent storage.</span></span> <span data-ttu-id="e7f86-118">自從開啟或上次認可之後對資料流程所做的變更，都會反映在父儲存物件中。</span><span class="sxs-lookup"><span data-stu-id="e7f86-118">Changes that have been made to the stream since it was opened or last committed are reflected to the parent storage object.</span></span> <span data-ttu-id="e7f86-119">如果以交易模式開啟父系，父系可能仍會在稍後回復此資料流程物件的變更時還原。</span><span class="sxs-lookup"><span data-stu-id="e7f86-119">If the parent is opened in transacted mode, the parent may still revert at a later time rolling back the changes to this stream object.</span></span> <span data-ttu-id="e7f86-120">複合檔案的執行不支援在交易模式中開啟資料流程，因此這個方法的效果幾乎不會影響到清除記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e7f86-120">The compound file implementation does not support opening streams in transacted mode, so this method has very little effect other than to flush memory buffers.</span></span>

## <a name="examples"></a><span data-ttu-id="e7f86-121">範例</span><span class="sxs-lookup"><span data-stu-id="e7f86-121">Examples</span></span>

<span data-ttu-id="e7f86-122">下列範例顯示如何將變更認可至儲存體。</span><span class="sxs-lookup"><span data-stu-id="e7f86-122">The following example shows committing changes to storage.</span></span>


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
```



## <a name="requirements"></a><span data-ttu-id="e7f86-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7f86-123">Requirements</span></span>



| <span data-ttu-id="e7f86-124">需求</span><span class="sxs-lookup"><span data-stu-id="e7f86-124">Requirement</span></span> | <span data-ttu-id="e7f86-125">值</span><span class="sxs-lookup"><span data-stu-id="e7f86-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f86-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7f86-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e7f86-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7f86-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e7f86-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7f86-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e7f86-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7f86-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e7f86-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e7f86-130">End of client support</span></span><br/>    | <span data-ttu-id="e7f86-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e7f86-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e7f86-132">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e7f86-132">End of server support</span></span><br/>    | <span data-ttu-id="e7f86-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7f86-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e7f86-134">標頭</span><span class="sxs-lookup"><span data-stu-id="e7f86-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7f86-135"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7f86-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7f86-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e7f86-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="e7f86-137"><dt>Scardssp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e7f86-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e7f86-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e7f86-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7f86-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7f86-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e7f86-140">IID</span><span class="sxs-lookup"><span data-stu-id="e7f86-140">IID</span></span><br/>                      | <span data-ttu-id="e7f86-141">IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="e7f86-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

