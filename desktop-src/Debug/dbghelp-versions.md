---
description: DbgHelp 程式庫是由 DbgHelp.dll 所執行。
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: DbgHelp 版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811e92ba88bf38cb46274e2d2c716a620ea83b16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688548"
---
# <a name="dbghelp-versions"></a><span data-ttu-id="45eeb-103">DbgHelp 版本</span><span class="sxs-lookup"><span data-stu-id="45eeb-103">DbgHelp Versions</span></span>

<span data-ttu-id="45eeb-104">DbgHelp 程式庫是由 DbgHelp.dll 所執行。</span><span class="sxs-lookup"><span data-stu-id="45eeb-104">The DbgHelp library is implemented by DbgHelp.dll.</span></span> <span data-ttu-id="45eeb-105">雖然此 DLL 包含在所有支援的 Windows 版本中，但很少會有最新版本的 DbgHelp 可用。</span><span class="sxs-lookup"><span data-stu-id="45eeb-105">Although this DLL is included in all supported versions of Windows, it is rarely the most current version of DbgHelp available.</span></span> <span data-ttu-id="45eeb-106">此外，Windows 隨附的 DbgHelp 版本也減少了其他版本的功能，特別是它缺少符號伺服器和來源伺服器的支援。</span><span class="sxs-lookup"><span data-stu-id="45eeb-106">Furthermore, the version of DbgHelp that ships in Windows has reduced functionality from the other releases-- specifically, it lacks support for Symbol Server and Source Server.</span></span>

<span data-ttu-id="45eeb-107">DbgHelp.dll、SymSrv.dll 和 SrcSrv.dll 的最新版本，可作為 Windows 封裝的 [偵錯工具](https://developer.microsoft.com/windows/downloads/windows-10-sdk) 一部分來使用。</span><span class="sxs-lookup"><span data-stu-id="45eeb-107">The most current versions of DbgHelp.dll, SymSrv.dll, and SrcSrv.dll are available as a part of the [Debugging Tools For Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) package.</span></span> <span data-ttu-id="45eeb-108">這些內含 Dll 的重新發佈原則的設計目的，是要讓人們盡可能輕鬆地將這些檔案包含在自己的套件和版本中。</span><span class="sxs-lookup"><span data-stu-id="45eeb-108">The redistribution policies for these included DLLs were specifically designed to make it as easy as possible for people to include these files in their own packages and releases.</span></span>

> [!Caution]  
> <span data-ttu-id="45eeb-109">使用者絕對不應該嘗試將 Windows 版 DbgHelp.dll 的 [偵錯工具](https://developer.microsoft.com/windows/downloads/windows-10-sdk) 安裝到 windows 系統目錄中，因為它們在此案例中是未經過測試，而且可能會使系統不穩定。</span><span class="sxs-lookup"><span data-stu-id="45eeb-109">Users should never attempt to install the [Debugging Tools For Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) versions of DbgHelp.dll into the Windows system directories because they are untested in this scenario and likely to destabilize the system.</span></span> <span data-ttu-id="45eeb-110">有不同的 X64 和 X86 版本的偵錯工具套件，而且對於同時支援這兩個平臺的人員來說，兩者都是必要的。</span><span class="sxs-lookup"><span data-stu-id="45eeb-110">There are separate X64 and X86 versions of the debugging package and both are necessary for people interested in supporting both platforms.</span></span>

<span data-ttu-id="45eeb-111">若要取得 DbgHelp.dll 的最新版本，請移至 [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) 並下載適用于 Windows 的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="45eeb-111">To obtain the latest version of DbgHelp.dll, go to [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) and download Debugging Tools for Windows.</span></span> <span data-ttu-id="45eeb-112">如需正確安裝的詳細資訊，請參閱 [呼叫 DbgHelp 程式庫](calling-the-dbghelp-library.md) 。</span><span class="sxs-lookup"><span data-stu-id="45eeb-112">Refer to [Calling the DbgHelp Library](calling-the-dbghelp-library.md) for information on proper installation.</span></span>

> [!Note]  
> <span data-ttu-id="45eeb-113">Windows 隨附的 DbgHelp.dll 檔案無法轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="45eeb-113">The DbgHelp.dll file that ships in Windows is not redistributable.</span></span>

<span data-ttu-id="45eeb-114">許多版本的 DbgHelp 都包含額外的功能。</span><span class="sxs-lookup"><span data-stu-id="45eeb-114">Many versions of DbgHelp include additional functionality.</span></span> <span data-ttu-id="45eeb-115">若要確保您的應用程式可以使用正確的 DbgHelp 版本，請參閱特定 API 參考檔中的需求資訊。</span><span class="sxs-lookup"><span data-stu-id="45eeb-115">To ensure that the correct version of DbgHelp is available for your application, review the Requirements information in the specific API reference documentation.</span></span>
