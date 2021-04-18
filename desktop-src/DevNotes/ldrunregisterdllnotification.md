---
description: 取消先前藉由呼叫 LdrRegisterDllNotification 函式註冊的 DLL 載入通知。
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: LdrUnregisterDllNotification 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385856"
---
# <a name="ldrunregisterdllnotification-function"></a><span data-ttu-id="40c1f-103">LdrUnregisterDllNotification 函式</span><span class="sxs-lookup"><span data-stu-id="40c1f-103">LdrUnregisterDllNotification function</span></span>

<span data-ttu-id="40c1f-104">\[您可以在不另行通知的情況下，從 Windows 變更或移除此功能。\]</span><span class="sxs-lookup"><span data-stu-id="40c1f-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="40c1f-105">取消先前藉由呼叫 [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) 函式註冊的 DLL 載入通知。</span><span class="sxs-lookup"><span data-stu-id="40c1f-105">Cancels DLL load notification previously registered by calling the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="40c1f-106">語法</span><span class="sxs-lookup"><span data-stu-id="40c1f-106">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="40c1f-107">參數</span><span class="sxs-lookup"><span data-stu-id="40c1f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40c1f-108">*Cookie* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40c1f-108">*Cookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40c1f-109">從註冊通知的 [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) 呼叫所接收到的回呼識別碼指標。</span><span class="sxs-lookup"><span data-stu-id="40c1f-109">A pointer to the callback identifier received from the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) call that registered for notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40c1f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="40c1f-110">Return value</span></span>

<span data-ttu-id="40c1f-111">傳回 **NTSTATUS** 或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="40c1f-111">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="40c1f-112">如果函式成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="40c1f-112">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="40c1f-113">如果找不到回呼函式，函數會傳回 **\_ \_ \_ 找不到的狀態 DLL**。</span><span class="sxs-lookup"><span data-stu-id="40c1f-113">If the callback function is not found, the function returns **STATUS\_DLL\_NOT\_FOUND**.</span></span>

<span data-ttu-id="40c1f-114">在 WDK 中可用的 Ntstatus 標頭檔中，會列出 **ntstatus** 錯誤碼的表單和重要性，並會在 wdk 檔中說明。</span><span class="sxs-lookup"><span data-stu-id="40c1f-114">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="40c1f-115">備註</span><span class="sxs-lookup"><span data-stu-id="40c1f-115">Remarks</span></span>

<span data-ttu-id="40c1f-116">此函數沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="40c1f-116">This function has no associated header file.</span></span> <span data-ttu-id="40c1f-117">相關聯的匯入程式庫（Ntdll.dll）可在 WDK 中使用。</span><span class="sxs-lookup"><span data-stu-id="40c1f-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="40c1f-118">您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，動態連結至 Ntdll.dll。</span><span class="sxs-lookup"><span data-stu-id="40c1f-118">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="40c1f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="40c1f-119">Requirements</span></span>



| <span data-ttu-id="40c1f-120">需求</span><span class="sxs-lookup"><span data-stu-id="40c1f-120">Requirement</span></span> | <span data-ttu-id="40c1f-121">值</span><span class="sxs-lookup"><span data-stu-id="40c1f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="40c1f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40c1f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="40c1f-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40c1f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="40c1f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40c1f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="40c1f-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40c1f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="40c1f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="40c1f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40c1f-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40c1f-127"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40c1f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40c1f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40c1f-129">**LdrRegisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="40c1f-129">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> </dl>

 

 
