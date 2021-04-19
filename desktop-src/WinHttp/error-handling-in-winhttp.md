---
description: WinHTTP 中的錯誤處理
ms.assetid: 96bceda2-ca96-4f88-ab38-35021889c2dd
title: WinHTTP 中的錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf234220d0973e86c830063e4ecc25312fa2d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979966"
---
# <a name="error-handling-in-winhttp"></a><span data-ttu-id="5712c-103">WinHTTP 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="5712c-103">Error Handling in WinHTTP</span></span>

<span data-ttu-id="5712c-104">並非所有的 WinHTTP API 函數都會以相同的方式報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="5712c-104">Not all WinHTTP API functions report errors in the same way.</span></span>

<span data-ttu-id="5712c-105">某些函式（例如 [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)）會傳回 **布林** 值，指出在 **FALSE** 時失敗。</span><span class="sxs-lookup"><span data-stu-id="5712c-105">Some functions, such as [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts), return a **BOOL** that indicates failure when **FALSE**.</span></span> <span data-ttu-id="5712c-106">如果傳回 **FALSE** ，則對錯誤感興趣的呼叫端應該呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="5712c-106">If **FALSE** is returned, callers interested in the error should call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="5712c-107">如果 **在** 函式成功 (傳回的值為 **FALSE**) ，則傳回的值會無法預期，而且可能會在 Windows 版本、Service pack 之間，甚至在相同函式的呼叫之間變更。</span><span class="sxs-lookup"><span data-stu-id="5712c-107">If **GetLastError** is called when the function succeded (returned anything but **FALSE**), the returned value is unpredictable and may change between Windows versions, Service Packs, or even between calls to the same function.</span></span>

<span data-ttu-id="5712c-108">某些函式（例如 [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)）會傳回 [HINTERNET](hinternet-handles-in-winhttp.md) 虛擬控制碼。</span><span class="sxs-lookup"><span data-stu-id="5712c-108">Some functions, such as [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect), return an [HINTERNET](hinternet-handles-in-winhttp.md) pseudo handle.</span></span> <span data-ttu-id="5712c-109">這些函式完全相同，但失敗是藉由傳回 **Null** 來表示。</span><span class="sxs-lookup"><span data-stu-id="5712c-109">These functions are exactly the same, except failure is indicated by returning **NULL**.</span></span> <span data-ttu-id="5712c-110">如果傳回 **Null** ，則對錯誤感興趣的呼叫端應該呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="5712c-110">If **NULL** is returned, callers interested in the error should call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="5712c-111">如果 **在** 函式成功 (傳回的任何值都是 **Null**) ，則傳回的值會無法預期，而且可能會在 Windows 版本、Service pack 之間，甚至在相同函式的呼叫之間變更。</span><span class="sxs-lookup"><span data-stu-id="5712c-111">If **GetLastError** is called when the function succeded (returned anything but **NULL**), the returned value is unpredictable and may change between Windows versions, Service Packs, or even between calls to the same function.</span></span>

<span data-ttu-id="5712c-112">某些函式（例如 [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)）會傳回 **DWORD** 錯誤碼，而且不需要呼叫任何其他函式來取得更多錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="5712c-112">Some functions, such as [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult), return a **DWORD** error code and there is no need to call any other functions for more error information.</span></span> <span data-ttu-id="5712c-113">針對這些函式，不應呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 。</span><span class="sxs-lookup"><span data-stu-id="5712c-113">For these functions, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) should not be called.</span></span> <span data-ttu-id="5712c-114">如果呼叫 **GetLastError** （不論函式成功或失敗），則傳回的值會無法預期，而且可能會在 Windows 版本、Service pack 之間，甚至在相同函式的呼叫之間變更。</span><span class="sxs-lookup"><span data-stu-id="5712c-114">If **GetLastError** is called, regardless of the success or failure of the function, the returned value is unpredictable and may change between Windows versions, Service Packs, or even between calls to the same function.</span></span>

 

 
