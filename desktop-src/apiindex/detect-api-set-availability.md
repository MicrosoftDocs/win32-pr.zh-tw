---
description: 說明如何偵測目前裝置上是否有特定的 API 集可用。
title: 偵測 API 集合可用性
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 7117ae82f142315a3e5f28065583381ef6af67f3
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/24/2020
ms.locfileid: "104093503"
---
# <a name="detect-api-set-availability"></a><span data-ttu-id="6bbc9-103">偵測 API 集合可用性</span><span class="sxs-lookup"><span data-stu-id="6bbc9-103">Detect API set availability</span></span>

<span data-ttu-id="6bbc9-104">在某些情況下，指定的 API 集合約名稱可能會刻意對應到某些 Windows 10 裝置上的空白模組名稱。</span><span class="sxs-lookup"><span data-stu-id="6bbc9-104">In some cases, a given API set contract name may be intentionally mapped to an empty module name on some Windows 10 devices.</span></span> <span data-ttu-id="6bbc9-105">這種情況的原因會有所不同，但常見的範例是在針對資源受限裝置設定時，可能會從 Windows 作業系統移除系統資源的昂貴功能。</span><span class="sxs-lookup"><span data-stu-id="6bbc9-105">The reasons for this vary, but a common example is that an expensive feature in terms of system resources may be removed from the Windows OS when configured for a resource-constrained device.</span></span> <span data-ttu-id="6bbc9-106">這會造成應用程式在 API 層級正常處理選用功能的挑戰。</span><span class="sxs-lookup"><span data-stu-id="6bbc9-106">This poses a challenge for applications to gracefully handle optional features at the API level.</span></span>

<span data-ttu-id="6bbc9-107">測試 WIN32 API 是否可用的傳統方法是使用 [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)。</span><span class="sxs-lookup"><span data-stu-id="6bbc9-107">The traditional approach for testing whether a Win32 API is available is to use [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="6bbc9-108">不過，因為 Windows 10 中的 [反向轉送](api-set-loader-operation.md#reverse-forwarding) 支援，所以這些不是測試 API 集的可靠方法。</span><span class="sxs-lookup"><span data-stu-id="6bbc9-108">However, these are not a reliable means for testing API sets because of the [reverse forwarding](api-set-loader-operation.md#reverse-forwarding) support in Windows 10.</span></span> <span data-ttu-id="6bbc9-109">當反向轉送套用至指定的 API 時， **LoadLibrary** 或 **GetProcAddress** 可能會解析為有效的函式指標，即使已移除內部實作為的情況也一樣。</span><span class="sxs-lookup"><span data-stu-id="6bbc9-109">When reverse forwarding is applied to a given API, **LoadLibrary** or **GetProcAddress** may resolve to a valid function pointer even in cases where the internal implementation has been removed.</span></span> <span data-ttu-id="6bbc9-110">在此情況下，函式指標將指向只傳回錯誤的存根函式。</span><span class="sxs-lookup"><span data-stu-id="6bbc9-110">In this case, the function pointer will be pointing to a stub function that simply returns an error.</span></span>

<span data-ttu-id="6bbc9-111">若要偵測這種情況，您可以使用 [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) 函式來查詢指定 API 執行的基礎可用性。</span><span class="sxs-lookup"><span data-stu-id="6bbc9-111">In order to detect this case, you can use the [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) function to query the underlying availability of a given API implementation.</span></span> <span data-ttu-id="6bbc9-112">這項測試會驗證呼叫這個函式將會導致執行 API 的功能執行。</span><span class="sxs-lookup"><span data-stu-id="6bbc9-112">This test validates that calling this function will result in executing a functional implementation of the API.</span></span>

<span data-ttu-id="6bbc9-113">下列程式碼範例示範如何使用 **IsApiSetImplemented** 來判斷 [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) 函式在呼叫之前是否可在目前的裝置上使用。</span><span class="sxs-lookup"><span data-stu-id="6bbc9-113">The following code example demonstrates how to use **IsApiSetImplemented** to determine whether the [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) function is available on the current device before calling it.</span></span> 

```c++
#include <windows.h>
#include <stdio.h>
#include <Wtsapi32.h>

int __cdecl wmain(int /* argc */, PCWSTR /* argv */ [])
{
    PWTS_SESSION_INFO pInfo = {};
    DWORD count = 0;

    if (!IsApiSetImplemented("ext-ms-win-session-wtsapi32-l1-1-0"))
    {
        wprintf(L"IsApiSetImplemented on ext-ms-win-session-wtsapi32-l1-1-0 returns FALSE\n");
    }
    else
    {
        if (WTSEnumerateSessionsW(WTS_CURRENT_SERVER_HANDLE, 0, 1, &pInfo, &count))
        {
            wprintf(L"SessionCount = %d\n", count);

            for (ULONG i = 0; i < count; i++)
            {
                PWTS_SESSION_INFO pCurInfo = &pInfo[i];
                wprintf(L"    %s: ID = %d, state = %d\n", pCurInfo->pWinStationName, 
                    pCurInfo->SessionId, pCurInfo->State);
            }

            WTSFreeMemory(pInfo);
        }
        else
        {
            wprintf(L"WTSEnumerateSessions failure : %x\n", GetLastError());
        }
    }

    return 0;
}
```