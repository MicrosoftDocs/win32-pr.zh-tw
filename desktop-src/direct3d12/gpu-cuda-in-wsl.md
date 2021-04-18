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
# <a name="enable-nvidia-cuda-in-wsl-2"></a>在 WSL 2 中啟用 NVIDIA CUDA

Windows 測試人員 SDK 支援執行現有的 ML 工具、程式庫和熱門架構，以在 WSL 2 實例內使用適用于 GPU 硬體加速的 NVIDIA CUDA。 這包括 PyTorch 和 TensorFlow，以及原生 Linux 環境中提供的所有 Docker 和 NVIDIA 容器工具組支援。 

> [!NOTE]
> 下列功能適用于 Windows 10 的發行前版本，而且可能會變更。

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>安裝最新的 Windows 測試人員開發人員通道組建 

若要使用此預覽版本，您必須 [註冊 Windows 測試人員計畫](https://insider.windows.com/getting-started/#register)。 完成之後，請遵循 [這些指令](https://insider.windows.com/getting-started/#install) 來安裝最新的 Insider build。 選擇您的設定時，請確定您選取的是 [開發通道](/windows-insider/flight-hub/#active-development-builds-of-windows-10)。 

針對此預覽版本，您需要組建20150或更高版本。 您可以透過 `winver` [執行] 命令 (Windows 標誌鍵 + R) 來 **執行** ，以檢查您的組建版本號碼。

## <a name="install-the-preview-gpu-driver"></a>安裝預覽版 GPU 驅動程式 

下載並安裝具 [NVIDIA CUDA 功能的驅動程式，以便 WSL](https://developer.nvidia.com/cuda/wsl) 與現有的 CUDA ML 工作流程搭配使用。 

## <a name="set-up-wsl-2-for-the-preview"></a>設定預覽版的 WSL 2 

安裝上述驅動程式之後，請確定您已 [啟用 WSL 2](/windows/wsl/install-win10) ，並 [安裝以 glibc 為基礎的散發](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) 套件 (例如 Ubuntu 或 Debian) 。 在 [設定] 應用程式的 [ **Windows Update** ] 區段中選取 [**檢查更新**]，以確定您有最新的核心。 

> [!NOTE]
> 當您啟用更新 Windows 時，請確定您已 **收到其他 Microsoft 產品的更新** 。 您可以在 [設定] 應用程式的 [ **Windows Update** ] 區段內的 [ **Advanced options** ] 中找到它。 

針對此預覽，您需要4.19.121 或更高版本的核心版本。 您可以在 PowerShell 中執行下列命令來檢查版本號碼。 

```powershell
wsl cat /proc/version
```

現在您可以透過 [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker)開始使用現有的 Linux 工作流程，或在 WSL 2 內安裝 [PyTorch](https://pytorch.org/get-started/locally/) 或 [TensorFlow](https://www.tensorflow.org/install/gpu) 。 有關取得設定的詳細資訊，請在 [NVIDIA 的 CUDA ON WSL 使用者指南](https://docs.nvidia.com/cuda/wsl-user-guide/index.html)中取得。

透過其 [CUDA 在 WSL 上的社區論壇，](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303)分享有關 NVIDIA 支援的意見反應。
