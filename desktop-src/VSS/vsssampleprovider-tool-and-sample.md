---
description: 顯示如何使用 VSS 介面建立 VSS 硬體提供者。
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: VssSampleProvider 工具和範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fceaa65b851e5469a3e82323da92d8bde0651a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998067"
---
# <a name="vsssampleprovider-tool-and-sample"></a><span data-ttu-id="a69dc-103">VssSampleProvider 工具和範例</span><span class="sxs-lookup"><span data-stu-id="a69dc-103">VssSampleProvider Tool and Sample</span></span>

<span data-ttu-id="a69dc-104">顯示如何使用 VSS [介面](volume-shadow-copy-api-interfaces.md) 建立 vss 硬體提供者。</span><span class="sxs-lookup"><span data-stu-id="a69dc-104">Shows how to use the VSS [interfaces](volume-shadow-copy-api-interfaces.md) to create a VSS hardware provider.</span></span>

> [!Note]  
> <span data-ttu-id="a69dc-105">Microsoft Windows 軟體開發套件 (SDK) 包含 VssSampleProvider 工具和範例。</span><span class="sxs-lookup"><span data-stu-id="a69dc-105">The VssSampleProvider tool and sample are included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a69dc-106">您可以從 [適用于 Windows 8 的 Windows 軟體開發套件 (SDK) ](https://developer.microsoft.com/windows/downloads/windows-8-sdk)下載 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="a69dc-106">You can download the Windows SDK from [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).</span></span>

 

<span data-ttu-id="a69dc-107">在 Windows SDK 安裝中，您可以在 `%Program Files(x86)%\Windows Kits\8.1\bin\x64` 64 位 windows) 的 (和 `%Program Files(x86)%\Windows Kits\8.1\bin\x86` 32 位 windows) 的 (中找到 VssSampleProvider 工具。</span><span class="sxs-lookup"><span data-stu-id="a69dc-107">In the Windows SDK installation, the VssSampleProvider tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

> [!Note]  
> <span data-ttu-id="a69dc-108">只有在 Windows Server 作業系統上才支援硬體提供者。</span><span class="sxs-lookup"><span data-stu-id="a69dc-108">Hardware providers are only supported on Windows Server operating systems.</span></span> <span data-ttu-id="a69dc-109">在 Windows 用戶端作業系統上，您可以編譯 VssSampleProvider 範例，但無法將它註冊為硬體提供者。</span><span class="sxs-lookup"><span data-stu-id="a69dc-109">On a Windows Client operating system, you can compile the VssSampleProvider sample, but you can't register it as a hardware provider.</span></span>

 

<span data-ttu-id="a69dc-110">VssSampleProvider 工具組含下列檔案：</span><span class="sxs-lookup"><span data-stu-id="a69dc-110">The VssSampleProvider tool consists of the following files:</span></span>

-   <span data-ttu-id="a69dc-111">Virtualstorage.sys</span><span class="sxs-lookup"><span data-stu-id="a69dc-111">Virtualstorage.sys</span></span>
-   <span data-ttu-id="a69dc-112">Vstorcontrol.exe</span><span class="sxs-lookup"><span data-stu-id="a69dc-112">Vstorcontrol.exe</span></span>
-   <span data-ttu-id="a69dc-113">Vssampleprovider.dll</span><span class="sxs-lookup"><span data-stu-id="a69dc-113">Vssampleprovider.dll</span></span>
-   <span data-ttu-id="a69dc-114">Vstorinterface.dll</span><span class="sxs-lookup"><span data-stu-id="a69dc-114">Vstorinterface.dll</span></span>

<span data-ttu-id="a69dc-115">VssSampleProvider 範例包含下列安裝和卸載腳本：</span><span class="sxs-lookup"><span data-stu-id="a69dc-115">The VssSampleProvider sample includes the following installation and uninstallation scripts:</span></span>

-   <span data-ttu-id="a69dc-116">Install-sampleprovider .cmd</span><span class="sxs-lookup"><span data-stu-id="a69dc-116">Install-sampleprovider.cmd</span></span>
-   <span data-ttu-id="a69dc-117">Uninstall-sampleprovider .cmd</span><span class="sxs-lookup"><span data-stu-id="a69dc-117">Uninstall-sampleprovider.cmd</span></span>
-   <span data-ttu-id="a69dc-118">註冊 \_app.vbs</span><span class="sxs-lookup"><span data-stu-id="a69dc-118">Register\_app.vbs</span></span>

<span data-ttu-id="a69dc-119">**安裝和使用 VssSampleProvider 範例**</span><span class="sxs-lookup"><span data-stu-id="a69dc-119">**To install and use the VssSampleProvider sample**</span></span>

1.  <span data-ttu-id="a69dc-120">瀏覽至 `Program Files (x86)\Windows Kits\8.0\bin\` 目錄。</span><span class="sxs-lookup"><span data-stu-id="a69dc-120">Navigate to the `Program Files (x86)\Windows Kits\8.0\bin\` directory.</span></span> <span data-ttu-id="a69dc-121">此目錄包含 virtualstoragevss.sys 和 vstorcontrol.exe。</span><span class="sxs-lookup"><span data-stu-id="a69dc-121">This directory contains virtualstoragevss.sys and vstorcontrol.exe.</span></span>
2.  <span data-ttu-id="a69dc-122">在指定的目錄中開啟命令提示字元視窗。</span><span class="sxs-lookup"><span data-stu-id="a69dc-122">Open a command prompt window in the specified directory.</span></span>
3.  <span data-ttu-id="a69dc-123">若要安裝虛擬儲存驅動程式，請在 [命令提示字元] 視窗中輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="a69dc-123">To install the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  <span data-ttu-id="a69dc-124">若要安裝 VSS 範例提供者，請在 [命令提示字元] 視窗中輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="a69dc-124">To install the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  <span data-ttu-id="a69dc-125">若要建立虛擬 LUN，請執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="a69dc-125">To create a virtual LUN, do the following.</span></span>

    1.  <span data-ttu-id="a69dc-126">在命令提示字元視窗中，鍵入下列命令：</span><span class="sxs-lookup"><span data-stu-id="a69dc-126">In the command prompt window, type the following command:</span></span>

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        <span data-ttu-id="a69dc-127">此命令會建立虛擬 LUN，其儲存體識別碼為 **VSS 範例 HW 提供者**。</span><span class="sxs-lookup"><span data-stu-id="a69dc-127">This command creates a virtual LUN whose storage identifier is **VSS Sample HW Provider**.</span></span> <span data-ttu-id="a69dc-128">若要建立其他虛擬 Lun，請重複此步驟。</span><span class="sxs-lookup"><span data-stu-id="a69dc-128">To create additional virtual LUNs, repeat this step.</span></span>

        <span data-ttu-id="a69dc-129">只有當 **Vss 範例 HW 提供者** 是儲存體識別碼的一部分時，vss 範例提供者才會辨識 LUN。</span><span class="sxs-lookup"><span data-stu-id="a69dc-129">The VSS sample provider recognizes a LUN only if **VSS Sample HW Provider** is a part of the storage identifier.</span></span> <span data-ttu-id="a69dc-130">如需儲存體識別碼的詳細資訊，請參閱下列 blog 文章。</span><span class="sxs-lookup"><span data-stu-id="a69dc-130">For more information about the storage identifier, see the following blog post.</span></span>

        [<span data-ttu-id="a69dc-131">LUN-重新同步處理 Diskshadow 和虛擬儲存體</span><span class="sxs-lookup"><span data-stu-id="a69dc-131">LUN - Resync with Diskshadow and Virtual Storage</span></span>](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  <span data-ttu-id="a69dc-132">在 [命令提示字元] 視窗中，使用 diskpart.exe 來格式化虛擬磁片並指派磁碟機號給它。</span><span class="sxs-lookup"><span data-stu-id="a69dc-132">In the command prompt window, use diskpart.exe to format the virtual disk and assign a drive letter to it.</span></span>

        <span data-ttu-id="a69dc-133">以下是要在 diskpart 命令提示字元執行的範例腳本。</span><span class="sxs-lookup"><span data-stu-id="a69dc-133">Here is a sample script to run at the diskpart command prompt.</span></span>

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  <span data-ttu-id="a69dc-134">若要執行範例提供者，請在 [命令提示字元] 視窗中輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="a69dc-134">To run the sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    <span data-ttu-id="a69dc-135">*<drive>* 代表虛擬 LUN 的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="a69dc-135">*<drive>* represents the drive letter of the virtual LUN.</span></span>

7.  <span data-ttu-id="a69dc-136">若要卸載 VSS 範例提供者，請在 [命令提示字元] 視窗中輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="a69dc-136">To uninstall the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  <span data-ttu-id="a69dc-137">若要卸載虛擬儲存驅動程式，請在 [命令提示字元] 視窗中輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="a69dc-137">To uninstall the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



