---
title: 處理資訊
description: 系統會維護正在執行的進程清單。 您可以藉由呼叫 EnumProcesses 函式，來取得這些進程的識別碼。 此函式會使用系統中所有進程的識別碼來填滿 DWORD 值的陣列。
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147debe36dd2647cd46d19a62b0374f47b73bc58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315553"
---
# <a name="process-information"></a><span data-ttu-id="1cbc0-105">處理資訊</span><span class="sxs-lookup"><span data-stu-id="1cbc0-105">Process Information</span></span>

<span data-ttu-id="1cbc0-106">系統會維護正在執行的進程清單。</span><span class="sxs-lookup"><span data-stu-id="1cbc0-106">The system maintains a list of running processes.</span></span> <span data-ttu-id="1cbc0-107">您可以藉由呼叫 [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) 函式，來取得這些進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1cbc0-107">You can retrieve the identifiers for these processes by calling the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="1cbc0-108">此函式會使用系統中所有進程的識別碼來填滿 **DWORD** 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="1cbc0-108">This function fills an array of **DWORD** values with the identifiers of all processes in the system.</span></span>

<span data-ttu-id="1cbc0-109">PSAPI.DLL 中的許多函式都需要進程控制碼。</span><span class="sxs-lookup"><span data-stu-id="1cbc0-109">Many functions in PSAPI require a process handle.</span></span> <span data-ttu-id="1cbc0-110">若要取得正在執行之進程的進程控制碼，請將其進程識別碼 (從 [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) 取得，傳遞給 [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) 函數。</span><span class="sxs-lookup"><span data-stu-id="1cbc0-110">To obtain a process handle for a running process, pass its process identifier (obtained from [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) to the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function.</span></span> <span data-ttu-id="1cbc0-111">當您完成進程控制碼時，請記得呼叫 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函數。</span><span class="sxs-lookup"><span data-stu-id="1cbc0-111">Remember to call the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function when you are finished with the process handle.</span></span>

 

 