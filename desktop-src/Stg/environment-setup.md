---
title: 環境設定
description: 已安裝的平臺軟體發展工具組 (SDK) 提供的 Setenv.bat 檔案位於 Platform SDK 的根目錄，您可以執行此檔案來設定您的環境，以建立使用 Platform SDK 的應用程式。
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f752872b96e4b02cbfd1724d8a4a99ca1de13f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969650"
---
# <a name="environment-setup"></a><span data-ttu-id="7deea-103">環境設定</span><span class="sxs-lookup"><span data-stu-id="7deea-103">Environment Setup</span></span>

<span data-ttu-id="7deea-104">已安裝的平臺軟體發展工具組 (SDK) 提供的 Setenv.bat 檔案位於 Platform SDK 的根目錄，您可以執行此檔案來設定您的環境，以建立使用 Platform SDK 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7deea-104">The installed Platform Software Development Kit (SDK) provides a Setenv.bat file located in the root directory of the Platform SDK that you can run to set up your environment for building applications that use the Platform SDK.</span></span>

## <a name="settings-and-variables"></a><span data-ttu-id="7deea-105">設定和變數</span><span class="sxs-lookup"><span data-stu-id="7deea-105">Settings and Variables</span></span>

<span data-ttu-id="7deea-106">您也可以手動設定您的環境，方法是在您的 Autoexec.bat 檔案中新增如下所示的內容。</span><span class="sxs-lookup"><span data-stu-id="7deea-106">You can also manually set up your environment by adding something like the following to your Autoexec.bat file.</span></span> <span data-ttu-id="7deea-107">您可以使用 Windows 來編輯 Autoexec.bat 檔案，以包含這些命令。</span><span class="sxs-lookup"><span data-stu-id="7deea-107">Using Windows, you can edit the Autoexec.bat file to include these commands.</span></span> <span data-ttu-id="7deea-108">您可以使用 Windows Server 2003、Windows XP、Windows 2000 或 Windows NT，使用您可以從主控台執行的 [系統] 對話方塊來編輯這些設定，或將這些設定新增至環境變數。</span><span class="sxs-lookup"><span data-stu-id="7deea-108">Using Windows Server 2003, Windows XP, Windows 2000, or Windows NT, you can edit or add these settings to your environment variables using the System dialog that you can run from the Control Panel.</span></span>


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



<span data-ttu-id="7deea-109">這些設定適用于執行 Windows Me、Windows 98 或 Windows 95 且同時安裝 Microsoft Visual C++ 和 Platform SDK 的 Intel 80386 或更新版本平臺。</span><span class="sxs-lookup"><span data-stu-id="7deea-109">These settings are appropriate for an Intel 80386 or later platform running Windows Me, Windows 98, or Windows 95 with both Microsoft Visual C++ and the Platform SDK installed.</span></span> <span data-ttu-id="7deea-110">例如，在此系統上，Visual C++ 版本5.0 會安裝在 C： \\ MSDEV 目錄下。</span><span class="sxs-lookup"><span data-stu-id="7deea-110">For example, on this system, Visual C++ version 5.0 is installed under the C:\\MSDEV directory.</span></span> <span data-ttu-id="7deea-111">Platform SDK 會安裝在 D： \\ MSSDK 目錄下。</span><span class="sxs-lookup"><span data-stu-id="7deea-111">The Platform SDK is installed under the D:\\MSSDK directory.</span></span> <span data-ttu-id="7deea-112">您的磁片設定可能會不同。</span><span class="sxs-lookup"><span data-stu-id="7deea-112">Your disk configuration may be different.</span></span> <span data-ttu-id="7deea-113">此範例的 Platform SDK 目錄 (，其中的 D： \\ MSSDK) 在每個路徑順序中都是稍早的。</span><span class="sxs-lookup"><span data-stu-id="7deea-113">The Platform SDK directories (for this example, those with D:\\MSSDK in them) are all earlier in each path sequence.</span></span> <span data-ttu-id="7deea-114">此順序假設命令列編譯是要在命令提示字元視窗中執行，而且 Platform SDK 中的 .h 包含和 .lib 程式庫檔案是這些編譯的慣用。</span><span class="sxs-lookup"><span data-stu-id="7deea-114">This sequence assumes that command line compilations are intended to be run in the Command Prompt window and that the .h include and .lib library files in the Platform SDK are preferred for those compilations.</span></span>

<span data-ttu-id="7deea-115">CPU 環境變數的定義是為了控制 Win32 組建，視平臺而定。</span><span class="sxs-lookup"><span data-stu-id="7deea-115">The CPU environment variable is defined to control the Win32 builds, depending on the platform.</span></span> <span data-ttu-id="7deea-116">目前可能的值包括 i386、MIPS、ALPHA 和 PPC。</span><span class="sxs-lookup"><span data-stu-id="7deea-116">Current possible values include i386, MIPS, ALPHA, and PPC.</span></span> <span data-ttu-id="7deea-117">如需詳細資訊，請參閱 \\ MSSDK INCLUDE 目錄的 PLATFORM SDK 中提供的 Win32 檔案 \\ 。</span><span class="sxs-lookup"><span data-stu-id="7deea-117">For more information, see the Win32.mak file provided in the Platform SDK in the \\MSSDK\\INCLUDE directory.</span></span> <span data-ttu-id="7deea-118">所有的 COM 教學課程程式碼範例 makefile 都包含 Win32. mak。</span><span class="sxs-lookup"><span data-stu-id="7deea-118">All of the COM tutorial code sample makefiles include Win32.mak.</span></span>

 

 




