---
title: 從 Visual Basic 和其他程式設計語言存取控制項
description: 從 Visual Basic 和其他程式設計語言存取控制項
ms.assetid: 869b8eb1-1f40-4d87-8501-e41d6c0a3a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45854b55b3826354543411c44dcd21d9f1d77e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965807"
---
# <a name="accessing-the-control-from-visual-basic-and-other-programming-languages"></a><span data-ttu-id="7fea7-103">從 Visual Basic 和其他程式設計語言存取控制項</span><span class="sxs-lookup"><span data-stu-id="7fea7-103">Accessing the Control from Visual Basic and Other Programming Languages</span></span>

<span data-ttu-id="7fea7-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7fea7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="7fea7-105">您也可以從 Visual Basic 和其他程式設計語言使用 Microsoft Agent 的控制權。</span><span class="sxs-lookup"><span data-stu-id="7fea7-105">You can also use Microsoft Agent's control from Visual Basic and other programming languages.</span></span> <span data-ttu-id="7fea7-106">請確定語言完全支援 ActiveX 控制項介面，並遵循其在加入和存取 ActiveX 控制項時的慣例。</span><span class="sxs-lookup"><span data-stu-id="7fea7-106">Make sure that the language fully supports the ActiveX control interface, and follow its conventions for adding and accessing ActiveX controls.</span></span> <span data-ttu-id="7fea7-107">若要存取此控制項，您必須已在目標系統上安裝代理程式。</span><span class="sxs-lookup"><span data-stu-id="7fea7-107">To access the control, Agent must already be installed on the target system.</span></span>

<span data-ttu-id="7fea7-108">然後，您可以從網站下載代理程式的自我安裝封包檔 (使用 [儲存而非執行] 選項) 。</span><span class="sxs-lookup"><span data-stu-id="7fea7-108">You can then download Agent's self-installing cabinet file from the website (using the Save rather than Run option).</span></span> <span data-ttu-id="7fea7-109">您可以在安裝安裝程式中包含此檔案。</span><span class="sxs-lookup"><span data-stu-id="7fea7-109">You can include this file in your installation setup program.</span></span> <span data-ttu-id="7fea7-110">每次執行時，它就會在目標系統上自動安裝代理程式。</span><span class="sxs-lookup"><span data-stu-id="7fea7-110">Whenever it is executed, it will automatically install Agent on the target system.</span></span> <span data-ttu-id="7fea7-111">如需安裝的詳細資訊，請參閱 Microsoft 代理程式散發授權合約。</span><span class="sxs-lookup"><span data-stu-id="7fea7-111">For further details on installation, see the Microsoft Agent distribution license agreement.</span></span> <span data-ttu-id="7fea7-112">不支援使用代理程式自行安裝封包檔（例如嘗試複製和註冊代理程式元件檔）進行安裝。</span><span class="sxs-lookup"><span data-stu-id="7fea7-112">Installation other than using Agent's self-installing cabinet file, such as attempting to copy and register Agent component files, is not supported.</span></span> <span data-ttu-id="7fea7-113">這可確保一致且完全的安裝。</span><span class="sxs-lookup"><span data-stu-id="7fea7-113">This ensures consistent and complete installation.</span></span> <span data-ttu-id="7fea7-114">請注意，Microsoft 代理程式自行安裝檔案不會安裝在 Microsoft Windows 2000 上，因為該版本的作業系統已經包含自己的代理程式版本。</span><span class="sxs-lookup"><span data-stu-id="7fea7-114">Note that the Microsoft Agent self-installing file will not install on Microsoft Windows 2000 because that version of the operating system already includes its own version of Agent.</span></span>

<span data-ttu-id="7fea7-115">若要成功在目標系統上安裝代理程式，您也必須確定目標系統有最新版本的 Microsoft Visual C++ 執行時間 (Msvcrt.dll) 、Microsoft 註冊工具 (Regsvr32.dll) 和 Microsoft COM dll。</span><span class="sxs-lookup"><span data-stu-id="7fea7-115">To successfully install Agent on a target system, you must also ensure that the target system has a recent version of the Microsoft Visual C++ runtime (Msvcrt.dll), Microsoft registration tool (Regsvr32.dll), and Microsoft COM dlls.</span></span> <span data-ttu-id="7fea7-116">若要確保目標系統上的必要元件，最簡單的方式就是要求安裝 Microsoft Internet Explorer 3.02 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7fea7-116">The easiest way to ensure that the necessary components are on the target system is to require that Microsoft Internet Explorer 3.02 or later is installed.</span></span> <span data-ttu-id="7fea7-117">或者，您可以安裝 Microsoft Visual C++ 中提供的前兩個元件。</span><span class="sxs-lookup"><span data-stu-id="7fea7-117">Alternatively, you can install the first two components which are available as part of Microsoft Visual C++.</span></span> <span data-ttu-id="7fea7-118">必要的 COM dll 可以安裝為 Microsoft DCOM update 的一部分，可在 Microsoft 網站上取得。</span><span class="sxs-lookup"><span data-stu-id="7fea7-118">The necessary COM dlls can be installed as part of the Microsoft DCOM update, available at the Microsoft website.</span></span> <span data-ttu-id="7fea7-119">您可以在 Microsoft 網站上找到這些元件的進一步資訊和授權資訊。</span><span class="sxs-lookup"><span data-stu-id="7fea7-119">You can find further information and licensing information for these components at the Microsoft website.</span></span>

<span data-ttu-id="7fea7-120">代理程式的語言元件可以用同樣的方式來安裝。</span><span class="sxs-lookup"><span data-stu-id="7fea7-120">Agent's language components can be installed the same way.</span></span> <span data-ttu-id="7fea7-121">同樣地，您可以使用這項技術，來安裝可從 Microsoft 代理程式網站散發的 Microsoft 字元 ACS 格式。</span><span class="sxs-lookup"><span data-stu-id="7fea7-121">Similarly, you can use this technique to install the ACS format of the Microsoft characters available for distribution from the Microsoft Agent website.</span></span> <span data-ttu-id="7fea7-122">字元檔會自動安裝到 Microsoft 代理程式 \\ 字元子目錄。</span><span class="sxs-lookup"><span data-stu-id="7fea7-122">The character files automatically install to the Microsoft Agent \\Chars subdirectory.</span></span>

<span data-ttu-id="7fea7-123">因為 Microsoft 代理程式的元件是設計為作業系統元件，所以代理程式可能不會卸載。</span><span class="sxs-lookup"><span data-stu-id="7fea7-123">Because Microsoft Agent's components are designed as operating system components, Agent may not be uninstalled.</span></span> <span data-ttu-id="7fea7-124">同樣地，當代理程式已安裝為 Windows 作業系統的一部分時，代理程式自行安裝封包可能無法安裝。</span><span class="sxs-lookup"><span data-stu-id="7fea7-124">Similarly, where Agent is already installed as part of the Windows operating system, the Agent self-installing cabinet may not install.</span></span>

 

 




