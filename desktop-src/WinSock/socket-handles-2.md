---
description: 通訊端控制碼可以選擇性地成為 Windows 通訊端2中的檔案控制代碼。 來自 Winsock 提供者的通訊端控制碼可搭配其他非 Winsock 函數使用，例如 ReadFile、WriteFile、ReadFileEx 和 WriteFileEx。
ms.assetid: 986dd9d8-52be-47aa-92b2-6cd40b83f5de
title: 通訊端控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6ca8ed935819e018a59c52fb43dcf816530c07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978899"
---
# <a name="socket-handles"></a><span data-ttu-id="87be4-104">通訊端控制碼</span><span class="sxs-lookup"><span data-stu-id="87be4-104">Socket Handles</span></span>

<span data-ttu-id="87be4-105">通訊端控制碼可以選擇性地成為 Windows 通訊端2中的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="87be4-105">A socket handle can optionally be a file handle in Windows Sockets 2.</span></span> <span data-ttu-id="87be4-106">來自 Winsock 提供者的通訊端控制碼可搭配其他非 Winsock 函數使用，例如 [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile)、 [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile)、 [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex)和 [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex)。</span><span class="sxs-lookup"><span data-stu-id="87be4-106">A socket handle from a Winsock provider can be used with other non-Winsock functions such as [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex), and [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex).</span></span>

<span data-ttu-id="87be4-107">**XP1 \_ ifs \_ 處理** 提供者的通訊協定資訊結構中的成員，會決定提供者的通訊端控制碼是否為可安裝的檔案系統 (IFS) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="87be4-107">The **XP1\_IFS\_HANDLES** member in the protocol information structure for a provider determines whether a socket handle from a provider is an Installable File System (IFS) handle.</span></span> <span data-ttu-id="87be4-108">您可以使用 [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) 和 [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile)以外的其他非 (Winsock 函式，來使用可使用 IFS 控制碼的通訊端控制碼，而不會受到任何效能影響，例如) 。</span><span class="sxs-lookup"><span data-stu-id="87be4-108">Socket handles that are IFS handles can be used without a performance penalty with other non-Winsock functions ([**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) and [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), for example).</span></span> <span data-ttu-id="87be4-109">搭配非 Winsock 函式使用時，任何非 IFS 通訊端控制碼 (**ReadFile** 和 **WriteFile**，例如) 導致提供者與檔案系統之間的互動，其中牽涉到額外的處理負荷，因此可能會造成顯著的效能影響。</span><span class="sxs-lookup"><span data-stu-id="87be4-109">Any non-IFS socket handles when used with non-Winsock functions (**ReadFile** and **WriteFile**, for example) result in interactions between the provider and the file system where extra processing overhead is involved that can result in a significant performance penalty.</span></span> <span data-ttu-id="87be4-110">搭配非 Winsock 函式使用通訊端控制碼時，從基底檔案系統傳播的錯誤碼不一定會對應到 Winsock 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="87be4-110">When using socket handles with non-Winsock functions, the error codes propagated from the base file system are not always mapped to Winsock error codes.</span></span> <span data-ttu-id="87be4-111">因此，建議您只搭配 Winsock 函數使用通訊端控制碼。</span><span class="sxs-lookup"><span data-stu-id="87be4-111">Consequently, it is recommended that socket handles be used only with Winsock functions.</span></span>

<span data-ttu-id="87be4-112">通訊端控制碼不應搭配 [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="87be4-112">A socket handle should not be used with the [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function.</span></span> <span data-ttu-id="87be4-113">有多層式服務提供者 (Lsp) 可能會導致這種情況失敗，而且目的地進程無法匯入通訊端控制碼。</span><span class="sxs-lookup"><span data-stu-id="87be4-113">The presence of layered service providers (LSPs) can cause this to fail and there is no way for the destination process to import the socket handle.</span></span>

> [!Note]  
> <span data-ttu-id="87be4-114">已淘汰分層服務提供者。</span><span class="sxs-lookup"><span data-stu-id="87be4-114">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="87be4-115">從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="87be4-115">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="87be4-116">Windows 通訊端2已展開特定功能，以使用控制碼在通訊端之間傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="87be4-116">Windows Sockets 2 has expanded certain functions that transfer data between sockets using handles.</span></span> <span data-ttu-id="87be4-117">這些函式提供通訊端特定的優點，以傳輸資料並包含 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)、 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)和 [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa)。</span><span class="sxs-lookup"><span data-stu-id="87be4-117">The functions offer advantages specific to sockets for transferring data and include [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), and [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa).</span></span>

 

 
