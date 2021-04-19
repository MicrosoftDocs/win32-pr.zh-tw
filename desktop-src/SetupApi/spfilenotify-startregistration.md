---
description: 使用 RegisterDlls INF 指示詞來自行註冊 Dll 時，SetupInstallFromInfSection 的呼叫端可能會在每個檔案註冊或取消註冊時接收通知。
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: 'SPFILENOTIFY_STARTREGISTRATION 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe795af38c21c17bf4e81692985d4bfe50dc8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988350"
---
# <a name="spfilenotify_startregistration-message"></a><span data-ttu-id="4aa16-103">SPFILENOTIFY \_ STARTREGISTRATION 訊息</span><span class="sxs-lookup"><span data-stu-id="4aa16-103">SPFILENOTIFY\_STARTREGISTRATION message</span></span>

<span data-ttu-id="4aa16-104">使用 **RegisterDlls** INF 指示詞來自行註冊 dll 時， [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) 的呼叫端可能會在每個檔案註冊或取消註冊時接收通知。</span><span class="sxs-lookup"><span data-stu-id="4aa16-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="4aa16-105">若要在註冊檔案之前將 **SPFILENOTIFY \_ STARTREGISTRATION** 通知傳送給回呼常式一次，請 \_ \_ 在 **SPINST** 的 *旗標* 參數中包含 SPINST REGISTERCALLBACKAWARE plus REGSVR SetupInstallFromInfSection。</span><span class="sxs-lookup"><span data-stu-id="4aa16-105">To send a **SPFILENOTIFY\_STARTREGISTRATION** notification to the callback routine once before registering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="4aa16-106">若要傳送取消註冊的通知，請 \_ \_ 在 *Flags* 參數中包含 SPINST REGISTERCALLBACKAWARE plus SPINST UNREGSVR。</span><span class="sxs-lookup"><span data-stu-id="4aa16-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="4aa16-107">[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)的 *MsgHandler* 參數所指定的回呼常式必須是 [PSP 檔案 \_ \_ 回呼](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)類型。</span><span class="sxs-lookup"><span data-stu-id="4aa16-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="4aa16-108">將 *coNtext* 參數設定為 **SetupInstallFromInfSection** 中指定的相同 *內容*。</span><span class="sxs-lookup"><span data-stu-id="4aa16-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="4aa16-109">將 *通知* 參數設定為 **SPFILENOTIFY \_ STARTREGISTRATION**。</span><span class="sxs-lookup"><span data-stu-id="4aa16-109">Set the *Notification* parameter to **SPFILENOTIFY\_STARTREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="4aa16-110">參數</span><span class="sxs-lookup"><span data-stu-id="4aa16-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aa16-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="4aa16-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="4aa16-112">SP 暫存器 [**\_ \_ 控制 \_ 狀態**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) 結構的指標，其中包含要註冊或取消註冊之檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4aa16-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="4aa16-113">成員 **cbsize** 應該設定為結構的大小。</span><span class="sxs-lookup"><span data-stu-id="4aa16-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="4aa16-114">**FileName** 成員應設定為所註冊之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4aa16-114">The **FileName** member should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="4aa16-115">**Win32Error** 不會使用，且應該設定為無 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="4aa16-115">**Win32Error** is not used and should be set to NO\_ERROR.</span></span> <span data-ttu-id="4aa16-116">**FailureCode** 不會使用，且應設定為 SPREG \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="4aa16-116">**FailureCode** is not used and should be set to SPREG\_SUCCESS.</span></span>

</dd> <dt>

<span data-ttu-id="4aa16-117">*Param2*</span><span class="sxs-lookup"><span data-stu-id="4aa16-117">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="4aa16-118">如果正在註冊檔案， *Param2* 應該設定為非零值的指標。</span><span class="sxs-lookup"><span data-stu-id="4aa16-118">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="4aa16-119">如果檔案正在取消註冊， *Param2* 應該設定為零的指標。</span><span class="sxs-lookup"><span data-stu-id="4aa16-119">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aa16-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="4aa16-120">Return value</span></span>

<span data-ttu-id="4aa16-121">收到通知之後，回呼函數可能會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4aa16-121">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="4aa16-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4aa16-122">Return code</span></span>                                                                                  | <span data-ttu-id="4aa16-123">Description</span><span class="sxs-lookup"><span data-stu-id="4aa16-123">Description</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4aa16-124"><dt>**FILEOP \_ 中止**</dt></span><span class="sxs-lookup"><span data-stu-id="4aa16-124"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="4aa16-125">請勿註冊或取消註冊檔案，並停止處理 INF 區段。</span><span class="sxs-lookup"><span data-stu-id="4aa16-125">Do not register or unregister the file and stop processing the INF section.</span></span><br/>             |
| <dl> <span data-ttu-id="4aa16-126"><dt>**FILEOP \_ DOIT R**</dt></span><span class="sxs-lookup"><span data-stu-id="4aa16-126"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="4aa16-127">註冊或取消註冊檔案，並繼續處理 INF 區段。</span><span class="sxs-lookup"><span data-stu-id="4aa16-127">Register or unregister the file and continue processing the INF section.</span></span><br/>                |
| <dl> <span data-ttu-id="4aa16-128"><dt>**FILE \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="4aa16-128"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="4aa16-129">略過註冊或取消註冊檔案，但繼續處理 INF 區段</span><span class="sxs-lookup"><span data-stu-id="4aa16-129">Skip registration or unregistration of the file but continue processing the INF section</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4aa16-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="4aa16-130">Requirements</span></span>



| <span data-ttu-id="4aa16-131">需求</span><span class="sxs-lookup"><span data-stu-id="4aa16-131">Requirement</span></span> | <span data-ttu-id="4aa16-132">值</span><span class="sxs-lookup"><span data-stu-id="4aa16-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa16-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4aa16-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4aa16-134">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4aa16-134">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4aa16-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4aa16-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4aa16-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4aa16-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4aa16-137">標頭</span><span class="sxs-lookup"><span data-stu-id="4aa16-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aa16-138"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="4aa16-138"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aa16-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4aa16-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aa16-140">概觀</span><span class="sxs-lookup"><span data-stu-id="4aa16-140">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="4aa16-141">通知</span><span class="sxs-lookup"><span data-stu-id="4aa16-141">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="4aa16-142">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="4aa16-142">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="4aa16-143">**SPFILENOTIFY \_ ENDREGISTRATION**</span><span class="sxs-lookup"><span data-stu-id="4aa16-143">**SPFILENOTIFY\_ENDREGISTRATION**</span></span>](spfilenotify-endregistration.md)
</dt> </dl>

 

