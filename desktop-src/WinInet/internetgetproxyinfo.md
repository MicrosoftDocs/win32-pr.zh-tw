---
title: InternetGetProxyInfo 函式
description: 抓取用來存取指定資源的 proxy 資料。
ms.assetid: 5fc0f471-420c-4125-8323-cb1e1e72e43f
keywords:
- InternetGetProxyInfo 函數 WinINet
topic_type:
- apiref
api_name:
- InternetGetProxyInfo
api_location:
- JSProxy.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef441754fd5de09e3792d9269f05d96ecc08aa23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384689"
---
# <a name="internetgetproxyinfo-function"></a><span data-ttu-id="cb496-104">InternetGetProxyInfo 函式</span><span class="sxs-lookup"><span data-stu-id="cb496-104">InternetGetProxyInfo function</span></span>

> [!NOTE]
> <span data-ttu-id="cb496-105">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="cb496-105">This function is deprecated.</span></span> <span data-ttu-id="cb496-106">針對自動代理程式支援，請改用 (WinHTTP) 5.1 版的 HTTP 服務。</span><span class="sxs-lookup"><span data-stu-id="cb496-106">For autoproxy support, use HTTP Services (WinHTTP) version 5.1 instead.</span></span> <span data-ttu-id="cb496-107">如需詳細資訊，請參閱 [WinHTTP 自動代理程式支援](../winhttp/winhttp-autoproxy-support.md)。</span><span class="sxs-lookup"><span data-stu-id="cb496-107">For more information, see [WinHTTP AutoProxy Support](../winhttp/winhttp-autoproxy-support.md).</span></span>

<span data-ttu-id="cb496-108">抓取用來存取指定資源的 proxy 資料。</span><span class="sxs-lookup"><span data-stu-id="cb496-108">Retrieves proxy data for accessing specified resources.</span></span> <span data-ttu-id="cb496-109">只有動態連結至 "JSProxy.dll"，才能呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="cb496-109">This function can only be called by dynamically linking to "JSProxy.dll".</span></span>

## <a name="syntax"></a><span data-ttu-id="cb496-110">語法</span><span class="sxs-lookup"><span data-stu-id="cb496-110">Syntax</span></span>

```cpp
BOOL InternetGetProxyInfo(
  _In_  LPCSTR  lpszUrl,
  _In_  DWORD   dwUrlLength,
  _In_  LPSTR   lpszUrlHostName,
  _In_  DWORD   dwUrlHostNameLength,
  _Out_ LPSTR   *lplpszProxyHostName,
  _Out_ LPDWORD lpdwProxyHostNameLength
);
```

## <a name="parameters"></a><span data-ttu-id="cb496-111">參數</span><span class="sxs-lookup"><span data-stu-id="cb496-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb496-112">*lpszUrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb496-112">*lpszUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb496-113">以 null 結束的字串指標，指定目標 HTTP 資源的 URL。</span><span class="sxs-lookup"><span data-stu-id="cb496-113">A pointer to a null-terminated string that specifies the URL of the target HTTP resource.</span></span>

</dd> <dt>

<span data-ttu-id="cb496-114">*dwUrlLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb496-114">*dwUrlLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb496-115">*LpszUrl* 所指向的 URL 大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cb496-115">The size, in bytes, of the URL pointed to by *lpszUrl*.</span></span>

</dd> <dt>

<span data-ttu-id="cb496-116">*lpszUrlHostName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb496-116">*lpszUrlHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb496-117">以 null 結束的字串指標，指定目標 URL 的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="cb496-117">A pointer to a null-terminated string that specifies the host name of the target URL.</span></span>

</dd> <dt>

<span data-ttu-id="cb496-118">*dwUrlHostNameLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb496-118">*dwUrlHostNameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb496-119">*LpszUrlHostName* 所指向之主機名稱的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cb496-119">The size, in bytes, of the host name pointed to by *lpszUrlHostName*.</span></span>

</dd> <dt>

<span data-ttu-id="cb496-120">*lplpszProxyHostName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cb496-120">*lplpszProxyHostName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb496-121">緩衝區位址的指標，此緩衝區會接收要在指定資源的 HTTP 要求中使用之 proxy 的 URL。</span><span class="sxs-lookup"><span data-stu-id="cb496-121">A pointer to the address of a buffer that receives the URL of the proxy to use in an HTTP request for the specified resource.</span></span> <span data-ttu-id="cb496-122">應用程式會負責釋放這個字串。</span><span class="sxs-lookup"><span data-stu-id="cb496-122">The application is responsible for freeing this string.</span></span>

</dd> <dt>

<span data-ttu-id="cb496-123">*lpdwProxyHostNameLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cb496-123">*lpdwProxyHostNameLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb496-124">變數的指標，此變數會接收 *lplpszProxyHostName* 緩衝區中傳回之字串的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cb496-124">A pointer to a variable that receives the size, in bytes, of the string returned in the *lplpszProxyHostName* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb496-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb496-125">Return value</span></span>

<span data-ttu-id="cb496-126">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="cb496-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="cb496-127">若要取得擴充的錯誤資料，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="cb496-127">To get extended error data, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="cb496-128">備註</span><span class="sxs-lookup"><span data-stu-id="cb496-128">Remarks</span></span>

<span data-ttu-id="cb496-129">若要呼叫 **InternetGetProxyInfo**，您必須使用定義的函式指標類型 **pfnInternetGetProxyInfo**，以動態方式連結至該函式。</span><span class="sxs-lookup"><span data-stu-id="cb496-129">To call **InternetGetProxyInfo**, you must dynamically link to it using the defined function-pointer type **pfnInternetGetProxyInfo**.</span></span> <span data-ttu-id="cb496-130">下列程式碼片段顯示如何宣告此函式指標類型的實例，然後初始化並呼叫它。</span><span class="sxs-lookup"><span data-stu-id="cb496-130">The code snippet below shows how to declare an instance of this function-pointer type and then initialize and call it.</span></span>

```cpp
  HMODULE hModJS;                               // Handle for loading the DLL
  pfnInternetGetProxyInfo pIGPI;                // Function-pointer instance

  hModJS = LoadLibrary( TEXT("jsproxy.dll") );
  if (!hModJS)
  {
    _tprintf( TEXT("\nLoadLibrary failed to load jsproxy.dll with error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  pIGPI = (pfnInternetGetProxyInfo)
          GetProcAddress( hModJS, "InternetGetProxyInfo" );
  if (!pIGPI)         
  {
    _tprintf( TEXT("\nGetProcAddress failed to find InternetGetProxyInfo, error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  // The pIGPI function pointer can now be used to call InternetGetProxyInfo.
```

<span data-ttu-id="cb496-131">如同 WinINet API 的所有其他層面，無法從 DllMain 或全域物件的函式和析構函式中，安全地呼叫這個函式。</span><span class="sxs-lookup"><span data-stu-id="cb496-131">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="cb496-132">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="cb496-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="cb496-133">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="cb496-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="cb496-134">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="cb496-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb496-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb496-135">Requirements</span></span>

| <span data-ttu-id="cb496-136">需求</span><span class="sxs-lookup"><span data-stu-id="cb496-136">Requirement</span></span> | <span data-ttu-id="cb496-137">值</span><span class="sxs-lookup"><span data-stu-id="cb496-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb496-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb496-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cb496-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb496-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cb496-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb496-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cb496-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb496-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cb496-142">DLL</span><span class="sxs-lookup"><span data-stu-id="cb496-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb496-143"><dt>JSProxy.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb496-143"><dt>JSProxy.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="cb496-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb496-144">See also</span></span>

[<span data-ttu-id="cb496-145">**InternetInitializeAutoProxyDll**</span><span class="sxs-lookup"><span data-stu-id="cb496-145">**InternetInitializeAutoProxyDll**</span></span>](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

<span data-ttu-id="cb496-146">[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb496-146">[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span></span>

[<span data-ttu-id="cb496-147">**DetectAutoProxyUrl**</span><span class="sxs-lookup"><span data-stu-id="cb496-147">**DetectAutoProxyUrl**</span></span>](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
