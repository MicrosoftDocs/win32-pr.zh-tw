---
description: 專家會實作為 DllMain 函數。 作業系統會呼叫 DllMain 來取得專家實例的控制碼。
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: 'DllMain 專家回呼函數 (Process .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 914f50b75e83fdc67448770b32ac8d0f8e8ab656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850155"
---
# <a name="dllmain-expert-callback-function"></a><span data-ttu-id="40274-104">DllMain 專家回呼函數</span><span class="sxs-lookup"><span data-stu-id="40274-104">DllMain Expert callback function</span></span>

<span data-ttu-id="40274-105">專家會實作為 [**DllMain**](/windows/desktop/Dlls/dllmain) 函數。</span><span class="sxs-lookup"><span data-stu-id="40274-105">The expert implements the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> <span data-ttu-id="40274-106">作業系統會呼叫 **DllMain** 來取得專家實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="40274-106">The operating system calls **DllMain** to obtain a handle to an instance of the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="40274-107">語法</span><span class="sxs-lookup"><span data-stu-id="40274-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _Out_ HINSTANCE hInstance,
  _In_  ULONG     ulReason,
        LPVOID    Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="40274-108">參數</span><span class="sxs-lookup"><span data-stu-id="40274-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40274-109">*hInstance* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="40274-109">*hInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40274-110">專家實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="40274-110">Handle to an instance of the expert.</span></span>

<span data-ttu-id="40274-111">如果專家使用網路監視器的使用者介面， *hInstance* 值就必須儲存在全域變數中。</span><span class="sxs-lookup"><span data-stu-id="40274-111">If the expert uses the Network Monitor user interface, the *hInstance* value must be stored in a global variable.</span></span> <span data-ttu-id="40274-112">只有當 *ulReason* 參數的值設定為 DLL 進程附加時，才需要這個 \_ 方法 \_ 。</span><span class="sxs-lookup"><span data-stu-id="40274-112">This approach is necessary only when the value of the *ulReason* parameter is set to DLL\_PROCESS\_ATTACH.</span></span>

</dd> <dt>

<span data-ttu-id="40274-113">*ulReason* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40274-113">*ulReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40274-114">呼叫函數的原因指標。</span><span class="sxs-lookup"><span data-stu-id="40274-114">Indicator of why the function was called.</span></span> <span data-ttu-id="40274-115">DLL \_ 進程附加的值 \_ ， (在第一次載入 dll 時套用) 指出專家應該將 *hInstance* 值儲存在全域變數中。</span><span class="sxs-lookup"><span data-stu-id="40274-115">A value of DLL\_PROCESS\_ATTACH, (which applies when the DLL is first loaded) indicates that the expert should save the *hInstance* value in a global variable.</span></span>

<span data-ttu-id="40274-116">使用任何其他值，就可以忽略 [**DllMain**](/windows/desktop/Dlls/dllmain) 函數的所有呼叫。</span><span class="sxs-lookup"><span data-stu-id="40274-116">With any other value, all calls to the [**DllMain**](/windows/desktop/Dlls/dllmain) function can be ignored.</span></span> <span data-ttu-id="40274-117">如需作業系統所設定之所有可能旗標的清單，請參閱 **DLLMain**。</span><span class="sxs-lookup"><span data-stu-id="40274-117">For a list of all possible flags set by the operating system, see **DLLMain**.</span></span>

</dd> <dt>

<span data-ttu-id="40274-118">*已保留*</span><span class="sxs-lookup"><span data-stu-id="40274-118">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="40274-119">參數未使用中。</span><span class="sxs-lookup"><span data-stu-id="40274-119">Parameter is not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40274-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="40274-120">Return value</span></span>

<span data-ttu-id="40274-121">如果函式成功，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="40274-121">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="40274-122">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="40274-122">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="40274-123">備註</span><span class="sxs-lookup"><span data-stu-id="40274-123">Remarks</span></span>

<span data-ttu-id="40274-124">當進程載入或卸載專家 DLL 時，作業系統會呼叫 **DllMain** 專家功能。</span><span class="sxs-lookup"><span data-stu-id="40274-124">The operating system calls the **DllMain** expert function when a process loads or unloads the expert DLL.</span></span> <span data-ttu-id="40274-125">只有當專家的使用者介面可以用來查看設定或結果，然後只傳回適當的 *hInstance* 值時，才必須匯出 **DllMain** 專家函式。</span><span class="sxs-lookup"><span data-stu-id="40274-125">The **DllMain** expert function must be exported only if the expert has a user interface for viewing either configuration or results, and then only to return the proper *hInstance* value.</span></span>

<span data-ttu-id="40274-126">**DllMain** 專家函式是以動態連結程式庫 [**DllMain**](/windows/desktop/Dlls/dllmain)函數為基礎。</span><span class="sxs-lookup"><span data-stu-id="40274-126">The **DllMain** expert function is based on the dynamic link library [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="40274-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="40274-127">Requirements</span></span>



| <span data-ttu-id="40274-128">需求</span><span class="sxs-lookup"><span data-stu-id="40274-128">Requirement</span></span> | <span data-ttu-id="40274-129">值</span><span class="sxs-lookup"><span data-stu-id="40274-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="40274-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40274-130">Minimum supported client</span></span><br/> | <span data-ttu-id="40274-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40274-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="40274-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40274-132">Minimum supported server</span></span><br/> | <span data-ttu-id="40274-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40274-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="40274-134">標頭</span><span class="sxs-lookup"><span data-stu-id="40274-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="40274-135"><dt>處理。h</dt></span><span class="sxs-lookup"><span data-stu-id="40274-135"><dt>Process.h</dt></span></span> </dl> |



 

