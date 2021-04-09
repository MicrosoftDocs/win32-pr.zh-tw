---
title: CleanupCredentialCache 函式
description: 由特定安全性支援提供者所執行 (SSP) 以排清 SSP 認證快取。
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- CleanupCredentialCache 函數 WinINet
topic_type:
- apiref
api_name:
- CleanupCredentialCache
api_location:
- MSNSSPC.dll
- MSAPSSPC.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53464073dd59837ba8026bbec03118055fba20cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093876"
---
# <a name="cleanupcredentialcache-function"></a><span data-ttu-id="260d4-104">CleanupCredentialCache 函式</span><span class="sxs-lookup"><span data-stu-id="260d4-104">CleanupCredentialCache function</span></span>

<span data-ttu-id="260d4-105">**CleanupCredentialCache** 函式是由特定的安全性支援提供者所執行， (ssp) 來排清 SSP 認證快取。</span><span class="sxs-lookup"><span data-stu-id="260d4-105">The **CleanupCredentialCache** function is implemented by certain Security Support Providers (SSP) to flush the SSP credential cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="260d4-106">語法</span><span class="sxs-lookup"><span data-stu-id="260d4-106">Syntax</span></span>


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a><span data-ttu-id="260d4-107">參數</span><span class="sxs-lookup"><span data-stu-id="260d4-107">Parameters</span></span>

<span data-ttu-id="260d4-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="260d4-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="260d4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="260d4-109">Return value</span></span>

<span data-ttu-id="260d4-110">如果函式成功，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="260d4-110">**TRUE** if the function succeeds; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="260d4-111">備註</span><span class="sxs-lookup"><span data-stu-id="260d4-111">Remarks</span></span>

<span data-ttu-id="260d4-112">**CleanupCredentialCache** 函式是由下列 ssp 所執行：</span><span class="sxs-lookup"><span data-stu-id="260d4-112">The **CleanupCredentialCache** function is implemented by the following SSPs:</span></span>

-   <span data-ttu-id="260d4-113">MSNSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="260d4-113">MSNSSPC.dll</span></span>
-   <span data-ttu-id="260d4-114">MSAPSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="260d4-114">MSAPSSPC.dll</span></span>

<span data-ttu-id="260d4-115">這些 Ssp 的 **CleanupCredentialCache** 執行一律會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="260d4-115">The implementation of **CleanupCredentialCache** by these SSPs always returns **TRUE**.</span></span>

<span data-ttu-id="260d4-116">在嘗試取得模組控制碼以匯出 **CleanupCredentialCache** 之前，應用程式必須確認已載入的 ssp 是執行 **CleanupCredentialCache** 函式的其中一個已知 ssp。</span><span class="sxs-lookup"><span data-stu-id="260d4-116">Before attempting to obtain a module handle to export **CleanupCredentialCache**, the application must verify that the SSP that has been loaded is one of the known SSPs implementing the **CleanupCredentialCache** function.</span></span>

<span data-ttu-id="260d4-117">為了排清 SSP 認證快取，應用程式必須藉由呼叫 [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 函式來取得 ssp 的模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="260d4-117">In order to flush the SSP credential cache, the application must obtain a module handle for the SSP by calling the [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span> <span data-ttu-id="260d4-118">取得模組之後，應用程式應藉由呼叫 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)函式來匯出由 SSP 所執行的 **CleanupCredentialCache** 函式，並將 **GetModuleHandle** 和 **CleanupCredentialCache** 傳回的模組傳遞為輸入參數。</span><span class="sxs-lookup"><span data-stu-id="260d4-118">After obtaining the module, the application should export the **CleanupCredentialCache** function implemented by the SSP by calling the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function, passing the module returned by **GetModuleHandle** and **CleanupCredentialCache** as input parameters.</span></span>

<span data-ttu-id="260d4-119">如同 WinINet API 的所有其他層面，無法從 DllMain 或全域物件的函式和析構函式中，安全地呼叫這個函式。</span><span class="sxs-lookup"><span data-stu-id="260d4-119">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="260d4-120">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="260d4-120">WinINet does not support server implementations.</span></span> <span data-ttu-id="260d4-121">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="260d4-121">In addition, it should not be used from a service.</span></span> <span data-ttu-id="260d4-122">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="260d4-122">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="260d4-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="260d4-123">Requirements</span></span>



| <span data-ttu-id="260d4-124">需求</span><span class="sxs-lookup"><span data-stu-id="260d4-124">Requirement</span></span> | <span data-ttu-id="260d4-125">值</span><span class="sxs-lookup"><span data-stu-id="260d4-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="260d4-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="260d4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="260d4-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="260d4-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="260d4-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="260d4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="260d4-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="260d4-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                       |
| <span data-ttu-id="260d4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="260d4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="260d4-131"><dt>MSNSSPC.dll;</dt><dt>MSAPSSPC.dll</dt></span><span class="sxs-lookup"><span data-stu-id="260d4-131"><dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt></span></span> </dl> |



 

