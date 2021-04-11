---
description: 在第一次載入 DLL 時註冊通知。 這是在動態連結進行之前發生的通知。
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: LdrRegisterDllNotification 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025833"
---
# <a name="ldrregisterdllnotification-function"></a><span data-ttu-id="56f1e-104">LdrRegisterDllNotification 函式</span><span class="sxs-lookup"><span data-stu-id="56f1e-104">LdrRegisterDllNotification function</span></span>

<span data-ttu-id="56f1e-105">\[您可以在不另行通知的情況下，從 Windows 變更或移除此功能。\]</span><span class="sxs-lookup"><span data-stu-id="56f1e-105">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="56f1e-106">在第一次載入 DLL 時註冊通知。</span><span class="sxs-lookup"><span data-stu-id="56f1e-106">Registers for notification when a DLL is first loaded.</span></span> <span data-ttu-id="56f1e-107">這是在動態連結進行之前發生的通知。</span><span class="sxs-lookup"><span data-stu-id="56f1e-107">This notification occurs before dynamic linking takes place.</span></span>

## <a name="syntax"></a><span data-ttu-id="56f1e-108">語法</span><span class="sxs-lookup"><span data-stu-id="56f1e-108">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="56f1e-109">參數</span><span class="sxs-lookup"><span data-stu-id="56f1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56f1e-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="56f1e-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56f1e-111">此參數必須為零。</span><span class="sxs-lookup"><span data-stu-id="56f1e-111">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="56f1e-112">*NotificationFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="56f1e-112">*NotificationFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56f1e-113">載入 DLL 時要呼叫之 [*LdrDllNotification*](ldrdllnotification.md) 通知回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="56f1e-113">A pointer to an [*LdrDllNotification*](ldrdllnotification.md) notification callback function to call when the DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="56f1e-114">*內容* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="56f1e-114">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="56f1e-115">回呼函數的內容資料指標。</span><span class="sxs-lookup"><span data-stu-id="56f1e-115">A pointer to context data for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="56f1e-116">*Cookie* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="56f1e-116">*Cookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56f1e-117">變數的指標，用來接收回呼函數的識別碼。</span><span class="sxs-lookup"><span data-stu-id="56f1e-117">A pointer to a variable to receive an identifier for the callback function.</span></span> <span data-ttu-id="56f1e-118">此識別碼是用來取消註冊通知回呼函式。</span><span class="sxs-lookup"><span data-stu-id="56f1e-118">This identifier is used to unregister the notification callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56f1e-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="56f1e-119">Return value</span></span>

<span data-ttu-id="56f1e-120">如果函式成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="56f1e-120">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="56f1e-121">在 WDK 中可用的 Ntstatus 標頭檔中，會列出 **ntstatus** 錯誤碼的表單和重要性，並會在 wdk 檔中說明。</span><span class="sxs-lookup"><span data-stu-id="56f1e-121">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="56f1e-122">備註</span><span class="sxs-lookup"><span data-stu-id="56f1e-122">Remarks</span></span>

<span data-ttu-id="56f1e-123">此函數沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="56f1e-123">This function has no associated header file.</span></span> <span data-ttu-id="56f1e-124">相關聯的匯入程式庫（Ntdll.dll）可在 WDK 中使用。</span><span class="sxs-lookup"><span data-stu-id="56f1e-124">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="56f1e-125">您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，動態連結至 Ntdll.dll。</span><span class="sxs-lookup"><span data-stu-id="56f1e-125">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="56f1e-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="56f1e-126">Requirements</span></span>



| <span data-ttu-id="56f1e-127">需求</span><span class="sxs-lookup"><span data-stu-id="56f1e-127">Requirement</span></span> | <span data-ttu-id="56f1e-128">值</span><span class="sxs-lookup"><span data-stu-id="56f1e-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="56f1e-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56f1e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="56f1e-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56f1e-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="56f1e-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56f1e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="56f1e-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56f1e-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="56f1e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="56f1e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56f1e-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56f1e-134"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56f1e-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56f1e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56f1e-136">*LdrDllNotification*</span><span class="sxs-lookup"><span data-stu-id="56f1e-136">*LdrDllNotification*</span></span>](ldrdllnotification.md)
</dt> <dt>

[<span data-ttu-id="56f1e-137">**LdrUnregisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="56f1e-137">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
