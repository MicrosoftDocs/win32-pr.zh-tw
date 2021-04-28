---
description: SPFILENOTIFY_ENDREGISTRATION 訊息-使用 RegisterDlls INF 指示詞自行註冊 Dll 時，SetupInstallFromInfSection 的呼叫端可能會在每個檔案註冊或取消註冊時接收通知。
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: 'SPFILENOTIFY_ENDREGISTRATION 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec341c26f9f88390ff1b807e6e932b3b381cd57
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094506"
---
# <a name="spfilenotify_endregistration-message"></a><span data-ttu-id="ecae2-103">SPFILENOTIFY \_ ENDREGISTRATION 訊息</span><span class="sxs-lookup"><span data-stu-id="ecae2-103">SPFILENOTIFY\_ENDREGISTRATION message</span></span>

<span data-ttu-id="ecae2-104">使用 **RegisterDlls** INF 指示詞來自行註冊 dll 時， [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) 的呼叫端可能會在每個檔案註冊或取消註冊時接收通知。</span><span class="sxs-lookup"><span data-stu-id="ecae2-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="ecae2-105">若要在註冊或取消註冊檔案之後，將 **SPFILENOTIFY \_ ENDREGISTRATION** 通知傳送給回呼常式，請 \_ \_ 在 **SPINST** 的 *Flags* 參數中包含 SPINST REGISTERCALLBACKAWARE plus REGSVR SetupInstallFromInfSection。</span><span class="sxs-lookup"><span data-stu-id="ecae2-105">To send a **SPFILENOTIFY\_ENDREGISTRATION** notification to a callback routine once after registering or unregistering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="ecae2-106">若要傳送取消註冊的通知，請 \_ \_ 在 *Flags* 參數中包含 SPINST REGISTERCALLBACKAWARE plus SPINST UNREGSVR。</span><span class="sxs-lookup"><span data-stu-id="ecae2-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="ecae2-107">[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)的 *MsgHandler* 參數所指定的回呼常式必須是 [PSP 檔案 \_ \_ 回呼](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)類型。</span><span class="sxs-lookup"><span data-stu-id="ecae2-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="ecae2-108">將 *coNtext* 參數設定為 **SetupInstallFromInfSection** 中指定的相同 *內容*。</span><span class="sxs-lookup"><span data-stu-id="ecae2-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="ecae2-109">將 *通知* 參數設定為 **SPFILENOTIFY \_ ENDREGISTRATION**。</span><span class="sxs-lookup"><span data-stu-id="ecae2-109">Set the *Notification* parameter to **SPFILENOTIFY\_ENDREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="ecae2-110">參數</span><span class="sxs-lookup"><span data-stu-id="ecae2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecae2-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="ecae2-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="ecae2-112">SP 暫存器 [**\_ \_ 控制 \_ 狀態**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) 結構的指標，其中包含要註冊或取消註冊之檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ecae2-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="ecae2-113">成員 **cbsize** 應該設定為結構的大小。</span><span class="sxs-lookup"><span data-stu-id="ecae2-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="ecae2-114">**檔案名** 應設定為所註冊之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ecae2-114">**FileName** should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="ecae2-115">**Win32Error** 應該設定為 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) ，指出擴充的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ecae2-115">**Win32Error** should be set to a [system error code](/windows/desktop/Debug/system-error-codes) indicating an extended error code.</span></span> <span data-ttu-id="ecae2-116">**FailureCode** 應該設定為其中一個表示註冊結果的有效失敗代碼。</span><span class="sxs-lookup"><span data-stu-id="ecae2-116">**FailureCode** should be set to one of the valid failure codes indicating the outcome of the registration.</span></span> <span data-ttu-id="ecae2-117">如需有效的失敗碼，請參閱 [**SP \_ 註冊 \_ 控制 \_ 狀態**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa)。</span><span class="sxs-lookup"><span data-stu-id="ecae2-117">For valid failure codes see [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span></span>

</dd> <dt>

<span data-ttu-id="ecae2-118">*Param2*</span><span class="sxs-lookup"><span data-stu-id="ecae2-118">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="ecae2-119">如果正在註冊檔案， *Param2* 應該設定為非零值的指標。</span><span class="sxs-lookup"><span data-stu-id="ecae2-119">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="ecae2-120">如果檔案正在取消註冊， *Param2* 應該設定為零的指標。</span><span class="sxs-lookup"><span data-stu-id="ecae2-120">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecae2-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="ecae2-121">Return value</span></span>

<span data-ttu-id="ecae2-122">收到通知之後，回呼函數可能會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ecae2-122">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="ecae2-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ecae2-123">Return code</span></span>                                                                                  | <span data-ttu-id="ecae2-124">Description</span><span class="sxs-lookup"><span data-stu-id="ecae2-124">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="ecae2-125"><dt>**FILEOP \_ 中止**</dt></span><span class="sxs-lookup"><span data-stu-id="ecae2-125"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="ecae2-126">停止處理 INF 區段。</span><span class="sxs-lookup"><span data-stu-id="ecae2-126">Stop processing the INF section.</span></span><br/>     |
| <dl> <span data-ttu-id="ecae2-127"><dt>**FILEOP \_ DOIT R**</dt></span><span class="sxs-lookup"><span data-stu-id="ecae2-127"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="ecae2-128">繼續處理 INF 區段。</span><span class="sxs-lookup"><span data-stu-id="ecae2-128">Continue processing the INF section.</span></span><br/> |
| <dl> <span data-ttu-id="ecae2-129"><dt>**FILE \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="ecae2-129"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="ecae2-130">繼續處理 INF 區段</span><span class="sxs-lookup"><span data-stu-id="ecae2-130">Continue processing the INF section</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="ecae2-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecae2-131">Requirements</span></span>



| <span data-ttu-id="ecae2-132">需求</span><span class="sxs-lookup"><span data-stu-id="ecae2-132">Requirement</span></span> | <span data-ttu-id="ecae2-133">值</span><span class="sxs-lookup"><span data-stu-id="ecae2-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ecae2-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ecae2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ecae2-135">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecae2-135">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ecae2-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ecae2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ecae2-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecae2-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ecae2-138">標頭</span><span class="sxs-lookup"><span data-stu-id="ecae2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecae2-139"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="ecae2-139"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecae2-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecae2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecae2-141">概觀</span><span class="sxs-lookup"><span data-stu-id="ecae2-141">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="ecae2-142">通知</span><span class="sxs-lookup"><span data-stu-id="ecae2-142">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="ecae2-143">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="ecae2-143">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="ecae2-144">**SPFILENOTIFY \_ STARTREGISTRATION**</span><span class="sxs-lookup"><span data-stu-id="ecae2-144">**SPFILENOTIFY\_STARTREGISTRATION**</span></span>](spfilenotify-startregistration.md)
</dt> </dl>

 

