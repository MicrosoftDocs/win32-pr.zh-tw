---
description: 設定專家 DLL 內的專家。
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: '設定回呼函數 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 76ba55b7544e35a07b74a41788a3befa766f87bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977890"
---
# <a name="configure-callback-function"></a><span data-ttu-id="b3acd-103">設定回呼函數</span><span class="sxs-lookup"><span data-stu-id="b3acd-103">Configure callback function</span></span>

<span data-ttu-id="b3acd-104">設定函式會 **設定** 專家 DLL 內的專家。</span><span class="sxs-lookup"><span data-stu-id="b3acd-104">The **Configure** function configures the expert within the expert DLL.</span></span>

<span data-ttu-id="b3acd-105">專家必須實行 **設定** 函數。</span><span class="sxs-lookup"><span data-stu-id="b3acd-105">The expert must implement the **Configure** function.</span></span> <span data-ttu-id="b3acd-106">收到函式呼叫時，專家會顯示一個對話方塊，讓使用者變更任何可設定的專案。</span><span class="sxs-lookup"><span data-stu-id="b3acd-106">When the function call is received, the expert displays a dialog box that enables the user to change any configurable item.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3acd-107">語法</span><span class="sxs-lookup"><span data-stu-id="b3acd-107">Syntax</span></span>


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="b3acd-108">參數</span><span class="sxs-lookup"><span data-stu-id="b3acd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3acd-109">*hExpertKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3acd-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3acd-110">獨特的專家識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3acd-110">Unique expert identifier.</span></span>

<span data-ttu-id="b3acd-111">唯一的識別碼會傳回給所有專家特定的網路監視器函式。</span><span class="sxs-lookup"><span data-stu-id="b3acd-111">The unique identifier is passed back on all expert-specific Network Monitor functions.</span></span> <span data-ttu-id="b3acd-112">請注意，此識別碼可能與傳遞給 [**Run**](run.md) 函式的識別碼不是相同的專家索引鍵。</span><span class="sxs-lookup"><span data-stu-id="b3acd-112">Be aware that the identifier may not be the same expert key as the one passed to the [**Run**](run.md) function.</span></span> <span data-ttu-id="b3acd-113">請勿將專家金鑰儲存在 **設定** 呼叫中。</span><span class="sxs-lookup"><span data-stu-id="b3acd-113">Do not store the expert key from the **Configure** call.</span></span>

</dd> <dt>

<span data-ttu-id="b3acd-114">*ppConfig* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b3acd-114">*ppConfig* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3acd-115">進入時 [**EXPERTCONFIG**](expertconfig.md) 結構指標的指標。</span><span class="sxs-lookup"><span data-stu-id="b3acd-115">A pointer to a pointer to an [**EXPERTCONFIG**](expertconfig.md) structure upon entry.</span></span>

<span data-ttu-id="b3acd-116">成功結束之後，所參考的 [**EXPERTCONFIG**](expertconfig.md) 結構就會包含新的設定資料。</span><span class="sxs-lookup"><span data-stu-id="b3acd-116">After a successful exit, the referenced [**EXPERTCONFIG**](expertconfig.md) structure contains the new configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="b3acd-117">*pExpertStartupInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3acd-117">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3acd-118">當專家開始時，具有焦點的 capture 元素指標。</span><span class="sxs-lookup"><span data-stu-id="b3acd-118">A pointer to the capture element with focus when the expert started.</span></span>

</dd> <dt>

<span data-ttu-id="b3acd-119">*StartupFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3acd-119">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3acd-120">指出專家應該如何使用 *pExpertStartupInfo* 參數的旗標。</span><span class="sxs-lookup"><span data-stu-id="b3acd-120">The flags that indicate how the expert should use the *pExpertStartupInfo* parameter.</span></span> <span data-ttu-id="b3acd-121">唯一定義的旗標是「專家啟動」旗標，會 **\_ 在設定 \_ \_ \_ \_ \_ \_ \_ 資料上使用啟動資料**。</span><span class="sxs-lookup"><span data-stu-id="b3acd-121">The only flag defined is **EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA**.</span></span> <span data-ttu-id="b3acd-122">旗標表示專家將使用 *pExpertStartupInfo* 參數，而不是傳入的 *ppConfig* 參數。</span><span class="sxs-lookup"><span data-stu-id="b3acd-122">The flag indicates that the expert will use the *pExpertStartupInfo* parameter rather than the *ppConfig* parameter that passed in.</span></span> <span data-ttu-id="b3acd-123">一般來說，當您從操作功能表啟動專家時，會設定旗標。</span><span class="sxs-lookup"><span data-stu-id="b3acd-123">Typically, you set the flag when you start the expert from a context menu.</span></span>

</dd> <dt>

<span data-ttu-id="b3acd-124">*hWnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3acd-124">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3acd-125">父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b3acd-125">A handle to the parent window.</span></span> <span data-ttu-id="b3acd-126">使用控制碼開啟對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b3acd-126">Use the handle to open a dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3acd-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3acd-127">Return value</span></span>

<span data-ttu-id="b3acd-128">如果函式成功 (也就是，如果目前的設定存在) ，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="b3acd-128">If the function is successful (that is, if a current configuration exists), the return value is **TRUE**.</span></span>

<span data-ttu-id="b3acd-129">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b3acd-129">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3acd-130">備註</span><span class="sxs-lookup"><span data-stu-id="b3acd-130">Remarks</span></span>

<span data-ttu-id="b3acd-131">網路監視器會使用專家的目前設定來呼叫 **Configure** 函數（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="b3acd-131">Network Monitor calls the **Configure** function with the current configuration of the expert, if one exists.</span></span> <span data-ttu-id="b3acd-132">專家會顯示一個對話方塊，您可以在其中變更任何可設定的專案。</span><span class="sxs-lookup"><span data-stu-id="b3acd-132">The expert displays a dialog box, with which you can change any configurable item.</span></span>

<span data-ttu-id="b3acd-133">當傳入 *ppConfig* ，且網路監視器沒有為指定專家儲存的設定時，參數值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b3acd-133">When *ppConfig* is passed in and Network Monitor does not have a configuration stored for the specified expert, the parameter value can be **NULL**.</span></span> <span data-ttu-id="b3acd-134">在此情況下， **設定** 函數會假設 (或的硬式編碼預設值，會使用啟動資訊) 來開啟對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b3acd-134">In this case, the **Configure** function assumes hard-coded default values (or, uses the startup information) to open the dialog box.</span></span>

<span data-ttu-id="b3acd-135">設定函式傳回時，**設定** 資料也可以是 **null** ，而且傳入的是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="b3acd-135">The configuration data can also be **NULL** when the **Configure** function returns, and a **NULL** was passed-in.</span></span> <span data-ttu-id="b3acd-136">當網路監視器沒有預存預設值，且使用者按下 [ **取消**] 時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="b3acd-136">This situation occurs when Network Monitor does not have a stored default, and the user presses **Cancel**.</span></span>

<span data-ttu-id="b3acd-137">[**EXPERTCONFIG**](expertconfig.md)資料結構的開頭包含儲存結構大小資訊的私用區段。</span><span class="sxs-lookup"><span data-stu-id="b3acd-137">The beginning of the [**EXPERTCONFIG**](expertconfig.md) data structure includes a Private section that stores the structure size information.</span></span> <span data-ttu-id="b3acd-138">**EXPERTCONFIG** 結構的大小應該包含出現在結構開頭的保留 **DWORD** 長度。</span><span class="sxs-lookup"><span data-stu-id="b3acd-138">The size of the **EXPERTCONFIG** structure should include the reserved **DWORD** length that appears at the beginning of the structure.</span></span> <span data-ttu-id="b3acd-139">例如，如果您的設定資料需要20個位元組的儲存空間，請配置24個位元組來儲存資料。</span><span class="sxs-lookup"><span data-stu-id="b3acd-139">For example, if your configuration data requires 20 bytes of storage space, allocate 24 bytes to store the data.</span></span> <span data-ttu-id="b3acd-140">如果 *ppConfig* 為 **Null**，則 **Configure** 函式會呼叫 [**ExpertAllocMemory**](expertallocmemory.md) 函式，以配置大小正確的新設定。</span><span class="sxs-lookup"><span data-stu-id="b3acd-140">If a *ppConfig* is **NULL**, the **Configure** function calls the [**ExpertAllocMemory**](expertallocmemory.md) function to allocate a new configuration that is the correct size.</span></span> <span data-ttu-id="b3acd-141">如果緩衝區不足以保存專家資料，專家應該呼叫 [**ExpertReallocMemory**](expertreallocmemory.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="b3acd-141">If the buffer is not enough to hold the expert data, the expert should call the [**ExpertReallocMemory**](expertreallocmemory.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3acd-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3acd-142">Requirements</span></span>



| <span data-ttu-id="b3acd-143">需求</span><span class="sxs-lookup"><span data-stu-id="b3acd-143">Requirement</span></span> | <span data-ttu-id="b3acd-144">值</span><span class="sxs-lookup"><span data-stu-id="b3acd-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b3acd-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3acd-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b3acd-146">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3acd-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b3acd-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3acd-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b3acd-148">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3acd-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b3acd-149">標頭</span><span class="sxs-lookup"><span data-stu-id="b3acd-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3acd-150"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="b3acd-150"><dt>Netmon.h</dt></span></span> </dl> |



 

 




