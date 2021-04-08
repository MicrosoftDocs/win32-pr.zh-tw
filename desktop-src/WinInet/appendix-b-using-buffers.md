---
title: 使用字串緩衝區
description: 傳回字串的函式包含輸入參數、lpszBuffer 和大小參數 lpdwBufferLength。 雖然 lpszBuffer 可以是 Null，但 lpdwBufferLength 必須是 DWORD 變數的有效指標。
ms.assetid: ae7f84ba-15d4-483b-bdda-0042854f9e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309d887458521b99069b381f8bf6650ebeda488a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682723"
---
# <a name="using-string-buffers"></a><span data-ttu-id="7ee07-104">使用字串緩衝區</span><span class="sxs-lookup"><span data-stu-id="7ee07-104">Using String Buffers</span></span>

<span data-ttu-id="7ee07-105">傳回字串的函式包含輸入參數、 *lpszBuffer* 和大小參數 *lpdwBufferLength*。</span><span class="sxs-lookup"><span data-stu-id="7ee07-105">Functions that return strings contain an input parameter, *lpszBuffer*, and a size parameter, *lpdwBufferLength*.</span></span> <span data-ttu-id="7ee07-106">雖然 *lpszBuffer* 可以是 **Null**，但 *lpdwBufferLength* 必須是 **DWORD** 變數的有效指標。</span><span class="sxs-lookup"><span data-stu-id="7ee07-106">Although *lpszBuffer* can be **NULL**, *lpdwBufferLength* must be a valid pointer to a **DWORD** variable.</span></span> <span data-ttu-id="7ee07-107">如果 *lpszBuffer* 所指向的輸入緩衝區為 **Null** 或太小，無法容納輸出字串，則函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 **錯誤的 \_ \_ 緩衝區不足**。</span><span class="sxs-lookup"><span data-stu-id="7ee07-107">If the input buffer pointed to by *lpszBuffer* is **NULL** or too small to hold the output string, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**.</span></span> <span data-ttu-id="7ee07-108">*LpdwBufferLength* 所指向的變數包含一個數位，表示函式傳回要求的字串所需的位元組數目，包括 **null** 結束字元。</span><span class="sxs-lookup"><span data-stu-id="7ee07-108">The variable pointed to by *lpdwBufferLength* contains a number that represents the number of bytes the function requires to return the requested string, including the **null** terminator.</span></span> <span data-ttu-id="7ee07-109">應用程式應配置此大小的緩衝區，將 *lpdwBufferLength* 所指向的變數設定為此值，然後重新提交要求。</span><span class="sxs-lookup"><span data-stu-id="7ee07-109">The application should allocate a buffer of this size, set the variable pointed to by *lpdwBufferLength* to this value, and resubmit the request.</span></span> <span data-ttu-id="7ee07-110">如果緩衝區大小足以接收要求的字串，則會將字串複製到具有 **null** 結束字元的輸出緩衝區，而函數會傳回成功指示。</span><span class="sxs-lookup"><span data-stu-id="7ee07-110">If the buffer size is sufficient to receive the requested string, the string is copied to the output buffer with a **null** terminator and the function returns a success indication.</span></span> <span data-ttu-id="7ee07-111">*LpdwBufferLength* 所指向的變數現在包含儲存在緩衝區中的字元數，但不包括 **null** 結束字元。</span><span class="sxs-lookup"><span data-stu-id="7ee07-111">The variable pointed to by *lpdwBufferLength* now contains the number of characters stored in the buffer, excluding the **null** terminator.</span></span>

> [!Note]  
> <span data-ttu-id="7ee07-112">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="7ee07-112">WinINet does not support server implementations.</span></span> <span data-ttu-id="7ee07-113">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="7ee07-113">In addition, it should not be used from a service.</span></span> <span data-ttu-id="7ee07-114">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="7ee07-114">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 