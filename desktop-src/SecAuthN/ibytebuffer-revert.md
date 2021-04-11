---
description: Revert 方法會捨棄自從上次 IByteBuffer：： Commit 呼叫之後對交易資料流程所做的所有變更。
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: 'IByteBuffer：： Revert 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Revert
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cf7873407196c98868ca45c73db503568f8259e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191274"
---
# <a name="ibytebufferrevert-method"></a><span data-ttu-id="d7cce-103">IByteBuffer：： Revert 方法</span><span class="sxs-lookup"><span data-stu-id="d7cce-103">IByteBuffer::Revert method</span></span>

<span data-ttu-id="d7cce-104">\[**Revert** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d7cce-104">\[The **Revert** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d7cce-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="d7cce-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d7cce-106">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d7cce-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="d7cce-107">**Revert** 方法會捨棄自從上次 [**IByteBuffer：： Commit**](ibytebuffer-commit.md)呼叫之後對交易資料流程所做的所有變更。</span><span class="sxs-lookup"><span data-stu-id="d7cce-107">The **Revert** method discards all changes that have been made to a transacted stream since the last [**IByteBuffer::Commit**](ibytebuffer-commit.md) call.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7cce-108">語法</span><span class="sxs-lookup"><span data-stu-id="d7cce-108">Syntax</span></span>


```C++
HRESULT Revert();
```



## <a name="parameters"></a><span data-ttu-id="d7cce-109">參數</span><span class="sxs-lookup"><span data-stu-id="d7cce-109">Parameters</span></span>

<span data-ttu-id="d7cce-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d7cce-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7cce-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7cce-111">Return value</span></span>

<span data-ttu-id="d7cce-112">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d7cce-112">The return value is an **HRESULT**.</span></span> <span data-ttu-id="d7cce-113">值為 \_ [確定] 表示呼叫成功，而且資料流程已還原為先前的版本。</span><span class="sxs-lookup"><span data-stu-id="d7cce-113">A value of S\_OK indicates the call was successful and the stream was reverted to its previous version.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7cce-114">備註</span><span class="sxs-lookup"><span data-stu-id="d7cce-114">Remarks</span></span>

<span data-ttu-id="d7cce-115">這個方法會捨棄自上次認可作業之後對交易資料流程所做的變更。</span><span class="sxs-lookup"><span data-stu-id="d7cce-115">This method discards changes made to a transacted stream since the last commit operation.</span></span>

## <a name="examples"></a><span data-ttu-id="d7cce-116">範例</span><span class="sxs-lookup"><span data-stu-id="d7cce-116">Examples</span></span>

<span data-ttu-id="d7cce-117">下列範例會示範如何將交易資料流程還原至最後認可的作業。</span><span class="sxs-lookup"><span data-stu-id="d7cce-117">The following example shows reverting a transacted stream to the last-committed operation.</span></span>


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
```



## <a name="requirements"></a><span data-ttu-id="d7cce-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7cce-118">Requirements</span></span>



| <span data-ttu-id="d7cce-119">需求</span><span class="sxs-lookup"><span data-stu-id="d7cce-119">Requirement</span></span> | <span data-ttu-id="d7cce-120">值</span><span class="sxs-lookup"><span data-stu-id="d7cce-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7cce-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7cce-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d7cce-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7cce-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d7cce-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7cce-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d7cce-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7cce-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7cce-125">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d7cce-125">End of client support</span></span><br/>    | <span data-ttu-id="d7cce-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d7cce-126">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d7cce-127">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d7cce-127">End of server support</span></span><br/>    | <span data-ttu-id="d7cce-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d7cce-128">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d7cce-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d7cce-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7cce-130"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7cce-130"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7cce-131">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d7cce-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="d7cce-132"><dt>Scardssp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d7cce-132"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d7cce-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d7cce-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7cce-134"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7cce-134"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d7cce-135">IID</span><span class="sxs-lookup"><span data-stu-id="d7cce-135">IID</span></span><br/>                      | <span data-ttu-id="d7cce-136">IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="d7cce-136">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

