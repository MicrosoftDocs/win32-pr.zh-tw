---
description: PdhVbOpenQuery 函式會建立並初始化用來管理效能資料集合的唯一查詢結構。
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: PdhVbOpenQuery 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c657f033e2e972473218f2b283e03b11659d9f2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115561"
---
# <a name="pdhvbopenquery-function"></a><span data-ttu-id="26a78-103">PdhVbOpenQuery 函式</span><span class="sxs-lookup"><span data-stu-id="26a78-103">PdhVbOpenQuery function</span></span>

<span data-ttu-id="26a78-104">**PdhVbOpenQuery** 函式會建立並初始化用來管理效能資料集合的唯一查詢結構。</span><span class="sxs-lookup"><span data-stu-id="26a78-104">The **PdhVbOpenQuery** function creates and initializes a unique query structure that is used to manage the collection of performance data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26a78-105">本主題所描述的功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="26a78-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="26a78-106">相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。</span><span class="sxs-lookup"><span data-stu-id="26a78-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="26a78-107">函式 PdhVbOpenQuery ( \_ ByVal QueryHandle long \_ ) long</span><span class="sxs-lookup"><span data-stu-id="26a78-107">Function PdhVbOpenQuery( \_ ByVal QueryHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="26a78-108">參數</span><span class="sxs-lookup"><span data-stu-id="26a78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26a78-109">*QueryHandle*</span><span class="sxs-lookup"><span data-stu-id="26a78-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="26a78-110">在呼叫函式之前，已清除 (等於 0) 的變數，如果函式成功，則會包含所建立並開啟之查詢的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="26a78-110">Variable that is cleared (equals 0) before the function is called and, if the function is successful, contains the unique ID of the query that is created and opened.</span></span> <span data-ttu-id="26a78-111">這個控制碼是在後續呼叫其他 PDH 函數來識別查詢時使用。</span><span class="sxs-lookup"><span data-stu-id="26a78-111">This handle is used in the subsequent calls to other PDH functions to identify the query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26a78-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="26a78-112">Return value</span></span>

<span data-ttu-id="26a78-113">如果函式成功，它會傳回等於 ERROR SUCCESS 的 **長** 整數 \_ ，以及 *QueryHandle* 變數中的新控制碼。</span><span class="sxs-lookup"><span data-stu-id="26a78-113">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *QueryHandle* variable.</span></span>

<span data-ttu-id="26a78-114">如果函式失敗，則傳回值為 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 或 [PDH 錯誤碼](pdh-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="26a78-114">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="26a78-115">以下是可能的值。</span><span class="sxs-lookup"><span data-stu-id="26a78-115">The following are possible values.</span></span>



| <span data-ttu-id="26a78-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="26a78-116">Return code</span></span>                                                                                                     | <span data-ttu-id="26a78-117">Description</span><span class="sxs-lookup"><span data-stu-id="26a78-117">Description</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="26a78-118"><dt>**PDH \_ 不正確 \_ 引數**</dt></span><span class="sxs-lookup"><span data-stu-id="26a78-118"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="26a78-119">引數無效或不正確。</span><span class="sxs-lookup"><span data-stu-id="26a78-119">The argument is invalid or incorrect.</span></span><br/>             |
| <dl> <span data-ttu-id="26a78-120"><dt>**PDH \_ 記憶體 \_ 配置 \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="26a78-120"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="26a78-121">無法配置暫存記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="26a78-121">A temporary memory buffer could not be allocated.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="26a78-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="26a78-122">Requirements</span></span>



| <span data-ttu-id="26a78-123">需求</span><span class="sxs-lookup"><span data-stu-id="26a78-123">Requirement</span></span> | <span data-ttu-id="26a78-124">值</span><span class="sxs-lookup"><span data-stu-id="26a78-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26a78-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26a78-125">Minimum supported client</span></span><br/> | <span data-ttu-id="26a78-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26a78-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26a78-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26a78-127">Minimum supported server</span></span><br/> | <span data-ttu-id="26a78-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26a78-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="26a78-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="26a78-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="26a78-130"><dt>Pdh. .lib</dt></span><span class="sxs-lookup"><span data-stu-id="26a78-130"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="26a78-131">DLL</span><span class="sxs-lookup"><span data-stu-id="26a78-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26a78-132"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26a78-132"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26a78-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26a78-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26a78-134">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="26a78-134">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

