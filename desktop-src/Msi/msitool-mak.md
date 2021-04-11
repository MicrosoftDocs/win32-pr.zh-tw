---
description: Msitool 是可讓您用來建立工具和自訂動作的 makefile。
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: Msitool mak
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3dad9fd65aaa880e9fdb38369843907104dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115192"
---
# <a name="msitoolmak"></a><span data-ttu-id="d99cf-103">Msitool mak</span><span class="sxs-lookup"><span data-stu-id="d99cf-103">Msitool.mak</span></span>

<span data-ttu-id="d99cf-104">Msitool 是可讓您用來建立工具和自訂動作的 makefile。</span><span class="sxs-lookup"><span data-stu-id="d99cf-104">Msitool.mak is a makefile that you can use to build tools and custom actions.</span></span> <span data-ttu-id="d99cf-105">它可搭配 Visual C++ 4.0 版或更新版本使用。</span><span class="sxs-lookup"><span data-stu-id="d99cf-105">It may be used with Visual C++ version 4.0 or later.</span></span> <span data-ttu-id="d99cf-106">如需詳細資訊，請參閱標頭檔。</span><span class="sxs-lookup"><span data-stu-id="d99cf-106">For more information, see the header file.</span></span> <span data-ttu-id="d99cf-107">它需要在包含這個檔案之前定義一組值。</span><span class="sxs-lookup"><span data-stu-id="d99cf-107">It requires a set of values to be defined before including this file.</span></span> <span data-ttu-id="d99cf-108">開發人員通常會將它們放在 .cpp 的開頭，而由 C 編譯器略過 ifdef。</span><span class="sxs-lookup"><span data-stu-id="d99cf-108">Typically developers put those at the start of the .cpp, ifdef'd to be skipped by the C compiler.</span></span> <span data-ttu-id="d99cf-109">同樣地，資源也會新增至 .cpp 檔案的結尾。</span><span class="sxs-lookup"><span data-stu-id="d99cf-109">Likewise resources are added to the end of the .cpp file.</span></span> <span data-ttu-id="d99cf-110">如需詳細資訊，請參閱範例。</span><span class="sxs-lookup"><span data-stu-id="d99cf-110">See samples for details.</span></span>

<span data-ttu-id="d99cf-111">VCBIN 可以定義至找到 Visual C++ 工具的目錄，或 makefile 使用 MSVCDIR 和 MSDEVDIR。</span><span class="sxs-lookup"><span data-stu-id="d99cf-111">VCBIN can be defined to the directory where the Visual C++ tools are found or the makefile uses MSVCDIR and MSDEVDIR.</span></span> <span data-ttu-id="d99cf-112">如果未定義，則不會指定位置，假設工具位於路徑上。</span><span class="sxs-lookup"><span data-stu-id="d99cf-112">If those are not defined, it does not specify a location, assuming the tools to be on the PATH.</span></span> <span data-ttu-id="d99cf-113">Visual C++ 5.0 版中的環境變數有個問題，就是如果兩者都不在您的路徑上，連結器就找不到 Msdis100.dll。</span><span class="sxs-lookup"><span data-stu-id="d99cf-113">An issue with the environment variables in Visual C++ version 5.0 is that if both are not on you path, the linker cannot find Msdis100.dll.</span></span> <span data-ttu-id="d99cf-114">如果您將它從 MSDEVDIR 複製到 MSVCDIR，它就會運作。</span><span class="sxs-lookup"><span data-stu-id="d99cf-114">If you copy that from MSDEVDIR to MSVCDIR, it works.</span></span> <span data-ttu-id="d99cf-115">另一個選項是複製 Msdis100.dll，並 Rc.exe Rcdll.dll 至 MSVCDIR，並將 VCBIN 設定為該。</span><span class="sxs-lookup"><span data-stu-id="d99cf-115">The other option is to copy Msdis100.dll and Rc.exe and Rcdll.dll to MSVCDIR, and set VCBIN to that.</span></span>

<span data-ttu-id="d99cf-116">此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="d99cf-116">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d99cf-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="d99cf-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d99cf-118">Windows Installer 開發工具</span><span class="sxs-lookup"><span data-stu-id="d99cf-118">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="d99cf-119">已發行的版本、工具和可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d99cf-119">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



