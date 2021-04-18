---
title: 產生錯誤資訊
description: 如果伺服器或應用程式在透過 RPC 呼叫時發生嚴重錯誤，則應該向 RPC 執行時間指出發生失敗，而且在理想情況下，應該加入失敗的相關資訊以協助進行疑難排解。
ms.assetid: 6658c387-94df-4d85-9749-53858f9e0f5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b06a13e932034e6840479443e0b78f4c322c0b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965790"
---
# <a name="generating-error-information"></a><span data-ttu-id="5ed43-103">產生錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="5ed43-103">Generating Error Information</span></span>

<span data-ttu-id="5ed43-104">如果伺服器或應用程式在透過 RPC 呼叫時發生嚴重錯誤，則應該向 RPC 執行時間指出發生失敗，而且在理想情況下，應該加入失敗的相關資訊以協助進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="5ed43-104">If a server or application encounters a fatal error while being called through RPC, it should indicate to the RPC run time that it has encountered a failure, and ideally, should add information about the failure to facilitate troubleshooting.</span></span>

## <a name="indicating-fatal-errors-to-the-rpc-run-time"></a><span data-ttu-id="5ed43-105">指出 RPC 執行時間發生嚴重錯誤</span><span class="sxs-lookup"><span data-stu-id="5ed43-105">Indicating Fatal Errors to the RPC Run Time</span></span>

<span data-ttu-id="5ed43-106">若要指出 RPC 執行時間失敗，請呼叫 [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) 函式，並在 rpc 執行緒上呼叫例外狀況，或在另一個執行緒上以非同步方式處理呼叫時呼叫 [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) 。</span><span class="sxs-lookup"><span data-stu-id="5ed43-106">To indicate a failure to the RPC run time, call the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) function while on the RPC thread the exception was called on, or [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) if processing the call asynchronously on another thread.</span></span> <span data-ttu-id="5ed43-107">從伺服器常式傳回錯誤碼（例如管理員常式）並不足夠-根據 RPC 規格，函式的傳回值在伺服器上沒有錯誤的語義，不論 idl/acf 檔案設定為何。</span><span class="sxs-lookup"><span data-stu-id="5ed43-107">Returning an error code from the server routine, such as the manager routine, is not sufficient—according to the RPC specification, the return value of the function has no error semantics on the server, regardless of the idl/acf file settings.</span></span>

<span data-ttu-id="5ed43-108">當您的元件發生嚴重錯誤時，請執行所述的任何清除，然後使用錯誤碼呼叫 [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) 函式。</span><span class="sxs-lookup"><span data-stu-id="5ed43-108">When a fatal error occurs in your component, perform any cleanup deemed necessary and then call the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) function with the error code.</span></span> <span data-ttu-id="5ed43-109">**RpcRaiseException** 和傳回錯誤碼的唯一差異在於呼叫 **RpcRaiseException** 時，不會封送處理 out 參數。</span><span class="sxs-lookup"><span data-stu-id="5ed43-109">The only difference between **RpcRaiseException** and returning an error code is when the **RpcRaiseException** is called, the out parameters are not marshaled.</span></span> <span data-ttu-id="5ed43-110">這通常是一項優點，因為避免未初始化的參數變成不必要的。</span><span class="sxs-lookup"><span data-stu-id="5ed43-110">This is usually an advantage, since avoiding uninitialized out parameters becomes unnecessary.</span></span>

## <a name="generating-additional-extended-error-information"></a><span data-ttu-id="5ed43-111">產生額外的延伸錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="5ed43-111">Generating Additional Extended Error Information</span></span>

<span data-ttu-id="5ed43-112">如同 RPC 執行時間建立一連串的錯誤記錄，您的伺服器或應用程式可以將自己的記錄新增至鏈。</span><span class="sxs-lookup"><span data-stu-id="5ed43-112">Just as the RPC run time builds a chain of error records, your server or application can add its own records to the chain.</span></span> <span data-ttu-id="5ed43-113">這種方法通常有助於進行疑難排解程式。</span><span class="sxs-lookup"><span data-stu-id="5ed43-113">This approach often helps in the troubleshooting process.</span></span> <span data-ttu-id="5ed43-114">例如，伺服器可能會嘗試開啟指定的檔案，並收到「找不到檔案」錯誤。</span><span class="sxs-lookup"><span data-stu-id="5ed43-114">For example, a server may attempt to open a given file and receive a file not found error.</span></span> <span data-ttu-id="5ed43-115">只要傳回錯誤2，就不會對判斷遺失的檔案有説明。</span><span class="sxs-lookup"><span data-stu-id="5ed43-115">Simply returning error 2 would not be helpful in determining which file is missing.</span></span>

<span data-ttu-id="5ed43-116">相反地，您的伺服器可能會呼叫 [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) 函式，並在錯誤記錄中提供字串參數（ANSI 或 Unicode），指出它所尋找之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5ed43-116">Instead, your server could call the [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) function and provide a string parameter, either ANSI or Unicode, in the error record indicating the full path of the file it was looking for.</span></span> <span data-ttu-id="5ed43-117">當遠端電腦上的使用者畫面上出現這種資訊時，疑難排解就變得很簡單;可以完成檔案是否存在的簡單檢查，特別是因為 RPC 執行時間已經提供有問題的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="5ed43-117">When all this information appears on the user screen on a remote computer, troubleshooting becomes trivial; a simple check of whether the file exists can be done, especially since the name of the computer in question is already provided by the RPC run time.</span></span>

<span data-ttu-id="5ed43-118">如果沒有足夠的記憶體可用， [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) 函數呼叫可能會失敗，即使它只需要幾個位元組的堆積空間也一樣。</span><span class="sxs-lookup"><span data-stu-id="5ed43-118">The [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) function call may fail if enough memory is not available, even though it requires only a few bytes of heap space.</span></span> <span data-ttu-id="5ed43-119">此外， **RpcErrorAddRecord** 所加入的記錄會累積在指定的執行緒中。</span><span class="sxs-lookup"><span data-stu-id="5ed43-119">Also, records added by **RpcErrorAddRecord** accumulate in a given thread.</span></span> <span data-ttu-id="5ed43-120">執行時間通常會在呼叫您的伺服器常式之前清除這些記錄，但如果在 RPC 外部使用延伸的錯誤資訊，請呼叫 [**RpcErrorClearInformation**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorclearinformation)來處理線上程中累積累積的擴充錯誤。</span><span class="sxs-lookup"><span data-stu-id="5ed43-120">The runtime normally cleans those records up before it calls your server routine, but if extended error information is used outside RPC, take care of cleaning up the accumulated extended error in the thread by calling [**RpcErrorClearInformation**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorclearinformation).</span></span>

 

 




