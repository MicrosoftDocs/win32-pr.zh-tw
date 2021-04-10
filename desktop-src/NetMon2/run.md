---
description: 專家必須實行 Run 函數。 網路監視器會呼叫 Run 函式來啟動專家 DLL 內的專家。
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: " (Netmon) 執行回呼函數"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Run
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: c2dff2cf70a6d989928f17447fa3491dd9509f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848181"
---
# <a name="run-callback-function"></a><span data-ttu-id="aad71-104">執行回呼函數</span><span class="sxs-lookup"><span data-stu-id="aad71-104">Run callback function</span></span>

<span data-ttu-id="aad71-105">專家必須實行 **Run** 函數。</span><span class="sxs-lookup"><span data-stu-id="aad71-105">The expert must implement the **Run** function.</span></span> <span data-ttu-id="aad71-106">網路監視器會呼叫 **Run** 函式來啟動專家 DLL 內的專家。</span><span class="sxs-lookup"><span data-stu-id="aad71-106">Network Monitor calls the **Run** function to start the expert within the expert DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="aad71-107">語法</span><span class="sxs-lookup"><span data-stu-id="aad71-107">Syntax</span></span>


```C++
BOOL WINAPI Run(
  _In_ HEXPERTKEY         hExpertKey,
  _In_ PEXPERTCONFIG      pConfig,
  _In_ PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_ DWORD              StartupFlags,
  _In_ HWND               hWndParent
);
```



## <a name="parameters"></a><span data-ttu-id="aad71-108">參數</span><span class="sxs-lookup"><span data-stu-id="aad71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aad71-109">*hExpertKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aad71-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aad71-110">傳遞給所有專家特定網路監視器函式之專家的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="aad71-110">Unique identifier of the expert that is passed back to all expert-specific Network Monitor functions.</span></span>

> [!Note]  
> <span data-ttu-id="aad71-111">*HExpertKey* 識別碼可能會傳遞與 [**設定**](configure.md)函數所傳遞的專家金鑰不同的專家金鑰。</span><span class="sxs-lookup"><span data-stu-id="aad71-111">The *hExpertKey* identifier may pass an expert key that is different from the expert key that the [**Configure**](configure.md) function passes.</span></span>

 

</dd> <dt>

<span data-ttu-id="aad71-112">*>-pconfig* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aad71-112">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aad71-113">現有設定的指標。</span><span class="sxs-lookup"><span data-stu-id="aad71-113">Pointer to the existing configuration.</span></span> <span data-ttu-id="aad71-114">*>-pconfig* 參數可以是 **Null** ，這表示專家可以使用硬式編碼的預設值或 *pExpertStartupInfo* 參數所參考的啟動資訊來執行。</span><span class="sxs-lookup"><span data-stu-id="aad71-114">The *pConfig* parameter may be **NULL** which means that the expert can run with hard-coded defaults, or startup information that the *pExpertStartupInfo* parameter references.</span></span>

</dd> <dt>

<span data-ttu-id="aad71-115">*pExpertStartupInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aad71-115">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aad71-116">當專家開始時，具有焦點的 capture 元素指標。</span><span class="sxs-lookup"><span data-stu-id="aad71-116">Pointer to the capture element that has focus when the expert starts.</span></span>

</dd> <dt>

<span data-ttu-id="aad71-117">*StartupFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aad71-117">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aad71-118">有關專家應該如何使用 *pExpertStartupInfo* 參數的指標。</span><span class="sxs-lookup"><span data-stu-id="aad71-118">Indicator for how the expert should use the *pExpertStartupInfo* parameter.</span></span>

<span data-ttu-id="aad71-119">唯一定義的旗標為：</span><span class="sxs-lookup"><span data-stu-id="aad71-119">The only flag defined is:</span></span>



| <span data-ttu-id="aad71-120">值</span><span class="sxs-lookup"><span data-stu-id="aad71-120">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="aad71-121">意義</span><span class="sxs-lookup"><span data-stu-id="aad71-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <span data-ttu-id="aad71-122"><dt>**專家 \_ 啟動 \_ 旗標會在設定 \_ \_ \_ 資料上使用啟動資料 \_ \_ \_ 。**</dt></span><span class="sxs-lookup"><span data-stu-id="aad71-122"><dt>**EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA.**</dt></span></span> </dl> | <span data-ttu-id="aad71-123">此旗標表示專家使用 *pExpertStartupInfo* 參數，且不會使用 *>-pconfig* 參數。</span><span class="sxs-lookup"><span data-stu-id="aad71-123">This flag indicates that the expert uses the *pExpertStartupInfo* parameter, and does not use the *pConfig* parameter.</span></span> <span data-ttu-id="aad71-124">一般來說，當專家可以從滑鼠右鍵按一下來開始時，您可以設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="aad71-124">Typically, you can set this flag when the expert can start from a right-mouse click.</span></span> <span data-ttu-id="aad71-125">如果未設定旗標，則可能會發生下列兩種情況：專家不是以滑鼠右鍵按一下來啟動，也可能是由使用者以滑鼠右鍵按一下，然後由使用者進行設定。</span><span class="sxs-lookup"><span data-stu-id="aad71-125">If the flag is not set, the following two things can occur: either the expert does not start from a right-mouse click, or the expert starts from a right-mouse click, and then the user configures it.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="aad71-126">*hWndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aad71-126">*hWndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aad71-127">父 (的 *hWnd* 參數通常是網路監視器使用者介面) 。</span><span class="sxs-lookup"><span data-stu-id="aad71-127">The *hWnd* parameter of the parent (usually the Network Monitor user interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aad71-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="aad71-128">Return value</span></span>

<span data-ttu-id="aad71-129">如果函式成功 (也就是，如果專家從) 開始，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="aad71-129">If the function is successful (that is, if the expert starts), the return value is **TRUE**.</span></span>

<span data-ttu-id="aad71-130">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="aad71-130">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="aad71-131">備註</span><span class="sxs-lookup"><span data-stu-id="aad71-131">Remarks</span></span>

<span data-ttu-id="aad71-132">當執行時，專家會在 capture 檔案的框架中執行迴圈，並產生報表或建立顯示問題的事件。</span><span class="sxs-lookup"><span data-stu-id="aad71-132">When running, the expert loops through the frames in the capture file and either generates a report or creates events that show problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="aad71-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="aad71-133">Requirements</span></span>



| <span data-ttu-id="aad71-134">需求</span><span class="sxs-lookup"><span data-stu-id="aad71-134">Requirement</span></span> | <span data-ttu-id="aad71-135">值</span><span class="sxs-lookup"><span data-stu-id="aad71-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aad71-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aad71-136">Minimum supported client</span></span><br/> | <span data-ttu-id="aad71-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aad71-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="aad71-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aad71-138">Minimum supported server</span></span><br/> | <span data-ttu-id="aad71-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aad71-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aad71-140">標頭</span><span class="sxs-lookup"><span data-stu-id="aad71-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="aad71-141"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="aad71-141"><dt>Netmon.h</dt></span></span> </dl> |



 

 




