---
description: 當系統啟動使用載入時間動態連結的程式時，它會使用連結器放置在檔案中的資訊，來找出進程所使用的 Dll 名稱。
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Load-Time 動態連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28435fd6df4a3fc5311dc46dbb761b48c139a6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514004"
---
# <a name="load-time-dynamic-linking"></a><span data-ttu-id="a3230-103">Load-Time 動態連結</span><span class="sxs-lookup"><span data-stu-id="a3230-103">Load-Time Dynamic Linking</span></span>

<span data-ttu-id="a3230-104">當系統啟動使用載入時間動態連結的程式時，它會使用連結器放置在檔案中的資訊，來找出進程所使用的 Dll 名稱。</span><span class="sxs-lookup"><span data-stu-id="a3230-104">When the system starts a program that uses load-time dynamic linking, it uses the information the linker placed in the file to locate the names of the DLLs that are used by the process.</span></span> <span data-ttu-id="a3230-105">然後系統會搜尋 Dll。</span><span class="sxs-lookup"><span data-stu-id="a3230-105">The system then searches for the DLLs.</span></span> <span data-ttu-id="a3230-106">如需詳細資訊，請參閱 [動態連結程式庫搜尋順序](dynamic-link-library-search-order.md)。</span><span class="sxs-lookup"><span data-stu-id="a3230-106">For more information, see [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).</span></span>

<span data-ttu-id="a3230-107">如果系統找不到必要的 DLL，它就會終止處理常式，並顯示向使用者報告錯誤的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a3230-107">If the system cannot locate a required DLL, it terminates the process and displays a dialog box that reports the error to the user.</span></span> <span data-ttu-id="a3230-108">否則，系統會將 DLL 對應到進程的虛擬位址空間，並遞增 DLL 參考計數。</span><span class="sxs-lookup"><span data-stu-id="a3230-108">Otherwise, the system maps the DLL into the virtual address space of the process and increments the DLL reference count.</span></span>

<span data-ttu-id="a3230-109">系統會呼叫進入點函數。</span><span class="sxs-lookup"><span data-stu-id="a3230-109">The system calls the entry-point function.</span></span> <span data-ttu-id="a3230-110">此函式會接收程式碼，指出進程正在載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="a3230-110">The function receives a code indicating that the process is loading the DLL.</span></span> <span data-ttu-id="a3230-111">如果進入點函數未傳回 TRUE，則系統會終止進程並回報錯誤。</span><span class="sxs-lookup"><span data-stu-id="a3230-111">If the entry-point function does not return TRUE, the system terminates the process and reports the error.</span></span> <span data-ttu-id="a3230-112">如需進入點函數的詳細資訊，請參閱 [動態連結程式庫 Entry-Point](dynamic-link-library-entry-point-function.md)函式。</span><span class="sxs-lookup"><span data-stu-id="a3230-112">For more information about the entry-point function, see [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).</span></span>

<span data-ttu-id="a3230-113">最後，系統會使用匯入的 DLL 函式的起始位址來修改函式位址表。</span><span class="sxs-lookup"><span data-stu-id="a3230-113">Finally, the system modifies the function address table with the starting addresses for the imported DLL functions.</span></span>

<span data-ttu-id="a3230-114">DLL 會在初始化期間對應到進程的虛擬位址空間，而且只有在需要時才會載入實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="a3230-114">The DLL is mapped into the virtual address space of the process during its initialization and is loaded into physical memory only when needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3230-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3230-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3230-116">使用 Load-Time 動態連結</span><span class="sxs-lookup"><span data-stu-id="a3230-116">Using Load-Time Dynamic Linking</span></span>](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



