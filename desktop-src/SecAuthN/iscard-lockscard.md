---
description: LockSCard 方法會宣告智慧卡的獨佔存取權。
ms.assetid: 70af7c5a-ebe7-48ee-8a76-dfea7f73f45e
title: 'ISCard：： LockSCard 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.LockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d5b834afec339aa4c3a4eee42f9817409fabb917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194507"
---
# <a name="iscardlockscard-method"></a><span data-ttu-id="6dfd3-103">ISCard：： LockSCard 方法</span><span class="sxs-lookup"><span data-stu-id="6dfd3-103">ISCard::LockSCard method</span></span>

<span data-ttu-id="6dfd3-104">\[**LockSCard** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6dfd3-104">\[The **LockSCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6dfd3-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="6dfd3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6dfd3-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="6dfd3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6dfd3-107">**LockSCard** 方法會宣告 [*智慧卡*](../secgloss/s-gly.md)的獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="6dfd3-107">The **LockSCard** method claims exclusive access to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6dfd3-108">語法</span><span class="sxs-lookup"><span data-stu-id="6dfd3-108">Syntax</span></span>


```C++
HRESULT LockSCard();
```



## <a name="parameters"></a><span data-ttu-id="6dfd3-109">參數</span><span class="sxs-lookup"><span data-stu-id="6dfd3-109">Parameters</span></span>

<span data-ttu-id="6dfd3-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6dfd3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6dfd3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6dfd3-111">Return value</span></span>

<span data-ttu-id="6dfd3-112">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="6dfd3-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6dfd3-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6dfd3-113">Return code</span></span>                                                                          | <span data-ttu-id="6dfd3-114">Description</span><span class="sxs-lookup"><span data-stu-id="6dfd3-114">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6dfd3-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6dfd3-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6dfd3-116">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="6dfd3-116">Operation completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6dfd3-117">備註</span><span class="sxs-lookup"><span data-stu-id="6dfd3-117">Remarks</span></span>

<span data-ttu-id="6dfd3-118">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6dfd3-118">In addition to the COM error code listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6dfd3-119">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="6dfd3-119">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="6dfd3-120">若要解除鎖定智慧卡，請呼叫 [**ISCard：： UnlockSCard**](iscard-unlockscard.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6dfd3-120">To unlock the smart card, call the [**ISCard::UnlockSCard**](iscard-unlockscard.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="6dfd3-121">範例</span><span class="sxs-lookup"><span data-stu-id="6dfd3-121">Examples</span></span>

<span data-ttu-id="6dfd3-122">下列範例顯示如何取得智慧卡的獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="6dfd3-122">The following example shows acquiring exclusive access to the smart card.</span></span>


```C++
HRESULT    hr;

// Lock the smart card.
hr = pISCard->LockSCard();
if (FAILED(hr))
{
    printf("Failed LockSCard\n");
    // Take error handling action as needed.
}
// Use smart card; unlock the smart card when done.
```



## <a name="requirements"></a><span data-ttu-id="6dfd3-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6dfd3-123">Requirements</span></span>



| <span data-ttu-id="6dfd3-124">需求</span><span class="sxs-lookup"><span data-stu-id="6dfd3-124">Requirement</span></span> | <span data-ttu-id="6dfd3-125">值</span><span class="sxs-lookup"><span data-stu-id="6dfd3-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dfd3-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6dfd3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6dfd3-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dfd3-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6dfd3-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6dfd3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6dfd3-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dfd3-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6dfd3-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6dfd3-130">End of client support</span></span><br/>    | <span data-ttu-id="6dfd3-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6dfd3-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6dfd3-132">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6dfd3-132">End of server support</span></span><br/>    | <span data-ttu-id="6dfd3-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6dfd3-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6dfd3-134">標頭</span><span class="sxs-lookup"><span data-stu-id="6dfd3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dfd3-135"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="6dfd3-135"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="6dfd3-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6dfd3-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="6dfd3-137"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6dfd3-137"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6dfd3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6dfd3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dfd3-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dfd3-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6dfd3-140">IID</span><span class="sxs-lookup"><span data-stu-id="6dfd3-140">IID</span></span><br/>                      | <span data-ttu-id="6dfd3-141">IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6dfd3-141">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6dfd3-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6dfd3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dfd3-143">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="6dfd3-143">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="6dfd3-144">**UnlockSCard**</span><span class="sxs-lookup"><span data-stu-id="6dfd3-144">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
