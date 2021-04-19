---
title: 使用 StoServe
description: StoServe 是主要用於 COM 伺服器的 DLL。
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d46dfd4070e9951223e0a498184b8db814c7a43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969922"
---
# <a name="using-stoserve"></a><span data-ttu-id="304f5-103">使用 StoServe</span><span class="sxs-lookup"><span data-stu-id="304f5-103">Using StoServe</span></span>

<span data-ttu-id="304f5-104">**StoServe** 是主要用於 COM 伺服器的 DLL。</span><span class="sxs-lookup"><span data-stu-id="304f5-104">**StoServe** is a DLL that is intended primarily as a COM server.</span></span> <span data-ttu-id="304f5-105">雖然可以透過連結到其相關聯的方式隱含載入。LIB 檔案，通常是在明確的 LoadLibrary 呼叫之後使用，通常是從 COM 函數 [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject)內。</span><span class="sxs-lookup"><span data-stu-id="304f5-105">Although it can be implicitly loaded by linking to its associated .LIB file, it is normally used after an explicit LoadLibrary call, usually from within the COM function [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject).</span></span> <span data-ttu-id="304f5-106">**StoServe** 是自我註冊的同進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="304f5-106">**StoServe** is a self-registering in-process server.</span></span>

<span data-ttu-id="304f5-107">若要使用 **StoServe**，用戶端程式不需要包含 StoServe。H 或 STOSERVE 的連結。自由。</span><span class="sxs-lookup"><span data-stu-id="304f5-107">To use **StoServe**, a client program does not need to include STOSERVE.H or link to STOSERVE.LIB.</span></span> <span data-ttu-id="304f5-108">**StoServe** 的 COM 用戶端只會透過其物件的 CLSID 和 COM 服務取得存取權。</span><span class="sxs-lookup"><span data-stu-id="304f5-108">A COM client of **StoServe** obtains access solely through its object's CLSID and COM services.</span></span> <span data-ttu-id="304f5-109">若為 **StoServe**，該 clsid 是 \_ 在 [檔案 PAPGUIDS] 中定義的 clsid DllPaper (。H 在 \\ inc. 的) 。</span><span class="sxs-lookup"><span data-stu-id="304f5-109">For **StoServe**, that CLSID is CLSID\_DllPaper (defined in file PAPGUIDS.H in the \\INC sibling directory).</span></span> <span data-ttu-id="304f5-110">[StoClien](structured-storage-client-sample--stoclien-.md)程式碼範例會顯示用戶端如何取得此存取權。</span><span class="sxs-lookup"><span data-stu-id="304f5-110">The [StoClien](structured-storage-client-sample--stoclien-.md) code sample shows how the client obtains this access.</span></span>

<span data-ttu-id="304f5-111">建立此範例的 makefile 會自動在登錄中註冊伺服器。</span><span class="sxs-lookup"><span data-stu-id="304f5-111">The makefile that builds this sample automatically registers the server in the registry.</span></span> <span data-ttu-id="304f5-112">您可以在 **StoServe** 目錄中的命令提示字元發出下列命令，以手動起始自我註冊：</span><span class="sxs-lookup"><span data-stu-id="304f5-112">You can manually initiate its self-registration by issuing the following command at the command prompt in the **StoServe** directory:</span></span>

<span data-ttu-id="304f5-113">**nmake** **註冊**</span><span class="sxs-lookup"><span data-stu-id="304f5-113">**nmake** **register**</span></span>

<span data-ttu-id="304f5-114">這會假設您已設定編譯環境。</span><span class="sxs-lookup"><span data-stu-id="304f5-114">This assumes that you have a compilation environment set up.</span></span> <span data-ttu-id="304f5-115">如果不是，您也可以在 **StoServe** 目錄中的命令提示字元，直接叫用 REGISTER.EXE 命令。</span><span class="sxs-lookup"><span data-stu-id="304f5-115">If not, you can also directly invoke the REGISTER.EXE command at the command prompt while in the **StoServe** directory.</span></span>

<span data-ttu-id="304f5-116">**..\\註冊 \\register.exe** **stoserve.dll**</span><span class="sxs-lookup"><span data-stu-id="304f5-116">**..\\register\\register.exe** **stoserve.dll**</span></span>

<span data-ttu-id="304f5-117">這些註冊命令需要在此系列中有先前的註冊範例組建，以及先前的 STOSERVE.DLL 組建。</span><span class="sxs-lookup"><span data-stu-id="304f5-117">These registration commands require a prior build of the REGISTER sample in this series, as well as a prior build of STOSERVE.DLL.</span></span>

<span data-ttu-id="304f5-118">在此系列中，makefile 使用來自註冊範例的 REGISTER.EXE 公用程式。</span><span class="sxs-lookup"><span data-stu-id="304f5-118">In this series, the makefiles use the REGISTER.EXE utility from the REGISTER sample.</span></span> <span data-ttu-id="304f5-119">最新版本的平臺軟體發展工具組 (SDK) 和 Visual C++ 包含公用程式 REGSVR32.EXE，可使用類似于註冊同進程伺服器和封送處理 Dll 的方式來使用。</span><span class="sxs-lookup"><span data-stu-id="304f5-119">Recent releases of the Platform Software Development Kit (SDK) and Visual C++ include a utility, REGSVR32.EXE, which can be used in a similar fashion to register in-process servers and marshaling DLLs.</span></span>

<span data-ttu-id="304f5-120">**StoServe** 會使用 APPUTIL 所提供的許多公用程式類別和服務。</span><span class="sxs-lookup"><span data-stu-id="304f5-120">**StoServe** uses many of the utility classes and services provided by APPUTIL.</span></span> <span data-ttu-id="304f5-121">如需更多有關 APPUTIL 的詳細資訊，請研究 APPUTIL 程式庫在同輩 APPUTIL 目錄中的原始程式碼，並 APPUTIL.HTM 在主要教學課程目錄中。</span><span class="sxs-lookup"><span data-stu-id="304f5-121">For more details on APPUTIL, study the APPUTIL library's source code in the sibling APPUTIL directory and APPUTIL.HTM in the main tutorial directory.</span></span>

 

 