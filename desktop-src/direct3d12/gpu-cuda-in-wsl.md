---
title: 在 WSL 2 中啟用 NVIDIA CUDA
description: 在 Windows 子系統 Linux 版上啟用 NVIDIA CUDA 預覽
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: ea5b460d4b4c71417f8ac9969f58bcebf6d10af9
ms.sourcegitcommit: 85acfd5afdcd30c81e3d2b375e813957f9830e9f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/03/2020
ms.locfileid: "106965258"
---
# <a name="enable-nvidia-cuda-in-wsl-2"></a><span data-ttu-id="cf13c-103">在 WSL 2 中啟用 NVIDIA CUDA</span><span class="sxs-lookup"><span data-stu-id="cf13c-103">Enable NVIDIA CUDA in WSL 2</span></span>

<span data-ttu-id="cf13c-104">Windows 測試人員 SDK 支援執行現有的 ML 工具、程式庫和熱門架構，以在 WSL 2 實例內使用適用于 GPU 硬體加速的 NVIDIA CUDA。</span><span class="sxs-lookup"><span data-stu-id="cf13c-104">The Windows Insider SDK supports running existing ML tools, libraries, and popular frameworks that use NVIDIA CUDA for GPU hardware acceleration inside a WSL 2 instance.</span></span> <span data-ttu-id="cf13c-105">這包括 PyTorch 和 TensorFlow，以及原生 Linux 環境中提供的所有 Docker 和 NVIDIA 容器工具組支援。</span><span class="sxs-lookup"><span data-stu-id="cf13c-105">This includes PyTorch and TensorFlow as well as all the Docker and NVIDIA Container Toolkit support available in a native Linux environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="cf13c-106">下列功能適用于 Windows 10 的發行前版本，而且可能會變更。</span><span class="sxs-lookup"><span data-stu-id="cf13c-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="cf13c-107">安裝最新的 Windows 測試人員開發人員通道組建</span><span class="sxs-lookup"><span data-stu-id="cf13c-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="cf13c-108">若要使用此預覽版本，您必須 [註冊 Windows 測試人員計畫](https://insider.windows.com/getting-started/#register)。</span><span class="sxs-lookup"><span data-stu-id="cf13c-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="cf13c-109">完成之後，請遵循 [這些指令](https://insider.windows.com/getting-started/#install) 來安裝最新的 Insider build。</span><span class="sxs-lookup"><span data-stu-id="cf13c-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest Insider build.</span></span> <span data-ttu-id="cf13c-110">選擇您的設定時，請確定您選取的是 [開發通道](/windows-insider/flight-hub/#active-development-builds-of-windows-10)。</span><span class="sxs-lookup"><span data-stu-id="cf13c-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="cf13c-111">針對此預覽版本，您需要組建20150或更高版本。</span><span class="sxs-lookup"><span data-stu-id="cf13c-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="cf13c-112">您可以透過 `winver` [執行] 命令 (Windows 標誌鍵 + R) 來 **執行** ，以檢查您的組建版本號碼。</span><span class="sxs-lookup"><span data-stu-id="cf13c-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="cf13c-113">安裝預覽版 GPU 驅動程式</span><span class="sxs-lookup"><span data-stu-id="cf13c-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="cf13c-114">下載並安裝具 [NVIDIA CUDA 功能的驅動程式，以便 WSL](https://developer.nvidia.com/cuda/wsl) 與現有的 CUDA ML 工作流程搭配使用。</span><span class="sxs-lookup"><span data-stu-id="cf13c-114">Download and install the [NVIDIA CUDA-enabled driver for WSL](https://developer.nvidia.com/cuda/wsl) to use with your existing CUDA ML workflows.</span></span> 

## <a name="set-up-wsl-2-for-the-preview"></a><span data-ttu-id="cf13c-115">設定預覽版的 WSL 2</span><span class="sxs-lookup"><span data-stu-id="cf13c-115">Set up WSL 2 for the preview</span></span> 

<span data-ttu-id="cf13c-116">安裝上述驅動程式之後，請確定您已 [啟用 WSL 2](/windows/wsl/install-win10) ，並 [安裝以 glibc 為基礎的散發](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) 套件 (例如 Ubuntu 或 Debian) 。</span><span class="sxs-lookup"><span data-stu-id="cf13c-116">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (such as Ubuntu or Debian).</span></span> <span data-ttu-id="cf13c-117">在 [設定] 應用程式的 [ **Windows Update** ] 區段中選取 [**檢查更新**]，以確定您有最新的核心。</span><span class="sxs-lookup"><span data-stu-id="cf13c-117">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="cf13c-118">當您啟用更新 Windows 時，請確定您已 **收到其他 Microsoft 產品的更新** 。</span><span class="sxs-lookup"><span data-stu-id="cf13c-118">Ensure you have **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="cf13c-119">您可以在 [設定] 應用程式的 [ **Windows Update** ] 區段內的 [ **Advanced options** ] 中找到它。</span><span class="sxs-lookup"><span data-stu-id="cf13c-119">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="cf13c-120">針對此預覽，您需要4.19.121 或更高版本的核心版本。</span><span class="sxs-lookup"><span data-stu-id="cf13c-120">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="cf13c-121">您可以在 PowerShell 中執行下列命令來檢查版本號碼。</span><span class="sxs-lookup"><span data-stu-id="cf13c-121">You can check the version number by running the following command in PowerShell.</span></span> 

```powershell
wsl cat /proc/version
```

<span data-ttu-id="cf13c-122">現在您可以透過 [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker)開始使用現有的 Linux 工作流程，或在 WSL 2 內安裝 [PyTorch](https://pytorch.org/get-started/locally/) 或 [TensorFlow](https://www.tensorflow.org/install/gpu) 。</span><span class="sxs-lookup"><span data-stu-id="cf13c-122">Now you can start using your exisiting Linux workflows through [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker), or by installing [PyTorch](https://pytorch.org/get-started/locally/) or [TensorFlow](https://www.tensorflow.org/install/gpu) inside WSL 2.</span></span> <span data-ttu-id="cf13c-123">有關取得設定的詳細資訊，請在 [NVIDIA 的 CUDA ON WSL 使用者指南](https://docs.nvidia.com/cuda/wsl-user-guide/index.html)中取得。</span><span class="sxs-lookup"><span data-stu-id="cf13c-123">More information on getting set up is captured in [NVIDIA's CUDA on WSL User Guide](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).</span></span>

<span data-ttu-id="cf13c-124">透過其 [CUDA 在 WSL 上的社區論壇，](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303)分享有關 NVIDIA 支援的意見反應。</span><span class="sxs-lookup"><span data-stu-id="cf13c-124">Share feedback on NVIDIA's support via their [Community forum for CUDA on WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).</span></span>
