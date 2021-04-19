---
description: 特定 Windows 通訊端服務提供者支援的通訊端數目上限是特定的實值。
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: 支援的通訊端數目上限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207893836a411a2465ffcefe10e838c2e8b59011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972410"
---
# <a name="maximum-number-of-sockets-supported"></a><span data-ttu-id="27b91-103">支援的通訊端數目上限</span><span class="sxs-lookup"><span data-stu-id="27b91-103">Maximum Number of Sockets Supported</span></span>

<span data-ttu-id="27b91-104">特定 Windows 通訊端服務提供者支援的通訊端數目上限是特定的實值。</span><span class="sxs-lookup"><span data-stu-id="27b91-104">The maximum number of sockets supported by a particular Windows Sockets service provider is implementation specific.</span></span> <span data-ttu-id="27b91-105">Microsoft Winsock 提供者會限制只能由本機電腦上的可用記憶體支援的通訊端數目上限。</span><span class="sxs-lookup"><span data-stu-id="27b91-105">The Microsoft Winsock provider limits the maximum number of sockets supported only by available memory on the local computer.</span></span> <span data-ttu-id="27b91-106">不過，協力廠商 Winsock 提供者可能會限制支援的通訊端數目。</span><span class="sxs-lookup"><span data-stu-id="27b91-106">However, third-party Winsock providers may have limitations on the numbers of sockets supported.</span></span> <span data-ttu-id="27b91-107">應用程式不應對特定數量的通訊端提供任何假設。</span><span class="sxs-lookup"><span data-stu-id="27b91-107">An application should make no assumptions about the availability of a certain number of sockets.</span></span> <span data-ttu-id="27b91-108">如需有關此主題的詳細資訊，請參閱 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)。</span><span class="sxs-lookup"><span data-stu-id="27b91-108">For more information on this topic see [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).</span></span>

## <a name="fd_set-and-select"></a><span data-ttu-id="27b91-109">FD \_ 設定並選取</span><span class="sxs-lookup"><span data-stu-id="27b91-109">FD\_SET and select</span></span>

<span data-ttu-id="27b91-110">\_從 UNIX 環境將應用程式移植到 Windows 時，會在 *Winsock2* 標頭檔中定義一些 FD XXX 宏。</span><span class="sxs-lookup"><span data-stu-id="27b91-110">A number of FD\_XXX macros are defined in the *Winsock2.h* header file for use in porting applications to Windows from the UNIX environment.</span></span> <span data-ttu-id="27b91-111">這些宏會搭配 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 和 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 函式使用，以將應用程式移植到 Windows。</span><span class="sxs-lookup"><span data-stu-id="27b91-111">These macros are used with the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) and [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions for porting applications to Windows.</span></span> <span data-ttu-id="27b91-112">Windows 通訊端應用程式可使用的通訊端數目上限不受資訊清單常數 FD SETSIZE 所影響 \_ 。</span><span class="sxs-lookup"><span data-stu-id="27b91-112">The maximum number of sockets that a Windows Sockets application can use is not affected by the manifest constant FD\_SETSIZE.</span></span> <span data-ttu-id="27b91-113">此值定義于 *Winsock2* 標頭檔中，用來建立與 **select** 函數搭配使用的 [**FD \_ 集**](/windows/desktop/api/winsock/nf-winsock-fd_set)結構。</span><span class="sxs-lookup"><span data-stu-id="27b91-113">This value defined in the *Winsock2.h* header file is used in constructing the [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structures used with **select** function.</span></span> <span data-ttu-id="27b91-114">Winsock2 中的預設值是64。</span><span class="sxs-lookup"><span data-stu-id="27b91-114">The default value in Winsock2.h is 64.</span></span> <span data-ttu-id="27b91-115">如果應用程式的設計目的是要使用 **select** 和 **WSAPoll** 函式來處理超過64通訊端，實作項應該先定義每個原始程式檔中的資訊清單 FD \_ SETSIZE，然後再包含 *Winsock2. h* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="27b91-115">If an application is designed to be capable of working with more than 64 sockets using the **select** and **WSAPoll** functions, the implementor should define the manifest FD\_SETSIZE in every source file before including the *Winsock2.h* header file.</span></span> <span data-ttu-id="27b91-116">執行這項操作的其中一種方法，就是將定義包含在 makefile 的編譯器選項中。</span><span class="sxs-lookup"><span data-stu-id="27b91-116">One way of doing this may be to include the definition within the compiler options in the makefile.</span></span> <span data-ttu-id="27b91-117">例如，您可以將 "-DFD \_ SETSIZE = 128" 新增為 Microsoft c + + 編譯器命令列的選項。</span><span class="sxs-lookup"><span data-stu-id="27b91-117">For example, you could add "-DFD\_SETSIZE=128" as an option to the compiler command line for Microsoft C++.</span></span> <span data-ttu-id="27b91-118">您必須強調，將 FD \_ SETSIZE 定義為特定值，並不會影響 Windows 通訊端服務提供者所提供的實際通訊端數目。</span><span class="sxs-lookup"><span data-stu-id="27b91-118">It must be emphasized that defining FD\_SETSIZE as a particular value has no effect on the actual number of sockets provided by a Windows Sockets service provider.</span></span> <span data-ttu-id="27b91-119">此值只會影響 \_ **Select** 和 **WSAPoll** 函數所使用的 FD XXX 宏。</span><span class="sxs-lookup"><span data-stu-id="27b91-119">This value only affects the FD\_XXX macros used by the **select** and **WSAPoll** functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27b91-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="27b91-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27b91-121">**FD \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="27b91-121">**FD\_SET**</span></span>](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[<span data-ttu-id="27b91-122">將通訊端應用程式移植到 Winsock</span><span class="sxs-lookup"><span data-stu-id="27b91-122">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="27b91-123">**選擇**</span><span class="sxs-lookup"><span data-stu-id="27b91-123">**select**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[<span data-ttu-id="27b91-124">Winsock 程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="27b91-124">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="27b91-125">**WSAStartup**</span><span class="sxs-lookup"><span data-stu-id="27b91-125">**WSAStartup**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[<span data-ttu-id="27b91-126">**WSAPoll**</span><span class="sxs-lookup"><span data-stu-id="27b91-126">**WSAPoll**</span></span>](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
