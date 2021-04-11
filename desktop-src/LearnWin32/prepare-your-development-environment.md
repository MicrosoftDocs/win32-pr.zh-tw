---
title: 準備您的開發環境
description: 準備您的開發環境
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314932"
---
# <a name="prepare-your-development-environment"></a><span data-ttu-id="3dad9-103">準備您的開發環境</span><span class="sxs-lookup"><span data-stu-id="3dad9-103">Prepare Your Development Environment</span></span>

<span data-ttu-id="3dad9-104">若要以 C 或 c + + 撰寫 Windows 程式，您必須安裝 Microsoft Windows 軟體開發套件 (SDK) 或 Microsoft Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="3dad9-104">To write a Windows program in C or C++, you must install the Microsoft Windows Software Development Kit (SDK) or Microsoft Visual Studio.</span></span> <span data-ttu-id="3dad9-105">Windows SDK 包含編譯和連結應用程式所需的標頭和程式庫。</span><span class="sxs-lookup"><span data-stu-id="3dad9-105">The Windows SDK contains the headers and libraries necessary to compile and link your application.</span></span> <span data-ttu-id="3dad9-106">Windows SDK 也包含用來建立 Windows 應用程式的命令列工具，包括 Visual C++ 編譯器和連結器。</span><span class="sxs-lookup"><span data-stu-id="3dad9-106">The Windows SDK also contains command-line tools for building Windows applications, including the Visual C++ compiler and linker.</span></span> <span data-ttu-id="3dad9-107">雖然您可以使用命令列工具來編譯和建立 Windows 程式，但建議您使用 Microsoft Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="3dad9-107">Although you can compile and build Windows programs with the command-line tools, we recommend using Microsoft Visual Studio.</span></span> <span data-ttu-id="3dad9-108">您可以在 [這裡](https://visualstudio.microsoft.com/downloads/)下載免費的 Visual Studio Community 下載，或 Visual Studio 其他版本的免費試用版。</span><span class="sxs-lookup"><span data-stu-id="3dad9-108">You can download a free download of Visual Studio Community or free trials of other versions of Visual Studio [here](https://visualstudio.microsoft.com/downloads/).</span></span>

<span data-ttu-id="3dad9-109">Windows SDK 的每個版本都是以最新版本的 Windows 為目標，以及數個舊版本。</span><span class="sxs-lookup"><span data-stu-id="3dad9-109">Each release of the Windows SDK targets the latest version of Windows as well as several previous versions.</span></span> <span data-ttu-id="3dad9-110">版本資訊會列出受支援的特定平臺，但除非您針對非常舊的 Windows 版本維護應用程式，否則您應該安裝最新版本的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="3dad9-110">The release notes list the specific platforms that are supported, but unless you are maintaining an application for a very old version of Windows, you should install the latest release of the Windows SDK.</span></span> <span data-ttu-id="3dad9-111">您可以在 [這裡](https://developer.microsoft.com/windows/downloads/windows-10-sdk)下載最新的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="3dad9-111">You can download the latest Windows SDK [here](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>

<span data-ttu-id="3dad9-112">Windows SDK 支援開發32位和64位應用程式。</span><span class="sxs-lookup"><span data-stu-id="3dad9-112">The Windows SDK supports development of both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="3dad9-113">Windows Api 的設計目的是要讓相同的程式碼可以針對32位或64位進行編譯，而不需要變更。</span><span class="sxs-lookup"><span data-stu-id="3dad9-113">The Windows APIs are designed so that the same code can compile for 32-bit or 64-bit without changes.</span></span>

> [!Note]  
> <span data-ttu-id="3dad9-114">Windows SDK 不支援硬體驅動程式開發，且此系列不會討論驅動程式開發。</span><span class="sxs-lookup"><span data-stu-id="3dad9-114">The Windows SDK does not support hardware driver development, and this series will not discuss driver development.</span></span> <span data-ttu-id="3dad9-115">如需有關撰寫硬體驅動程式的詳細資訊，請參閱 [使用 Windows 驅動程式開始使用](/windows-hardware/drivers/gettingstarted/)。</span><span class="sxs-lookup"><span data-stu-id="3dad9-115">For information about writing a hardware driver, see [Getting Started with Windows Drivers](/windows-hardware/drivers/gettingstarted/).</span></span>

## <a name="next"></a><span data-ttu-id="3dad9-116">下一個</span><span class="sxs-lookup"><span data-stu-id="3dad9-116">Next</span></span>

[<span data-ttu-id="3dad9-117">Windows 編碼慣例</span><span class="sxs-lookup"><span data-stu-id="3dad9-117">Windows Coding Conventions</span></span>](windows-coding-conventions.md)

## <a name="related-topics"></a><span data-ttu-id="3dad9-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="3dad9-118">Related topics</span></span>

* [<span data-ttu-id="3dad9-119">下載 Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3dad9-119">Download Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/)
* [<span data-ttu-id="3dad9-120">下載 Windows SDK</span><span class="sxs-lookup"><span data-stu-id="3dad9-120">Download Windows SDK</span></span>](https://developer.microsoft.com/windows/downloads/windows-10-sdk)