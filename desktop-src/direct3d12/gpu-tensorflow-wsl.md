---
title: Tensorflow with DirectML on WSL 2
description: 在 Windows 子系統 Linux 版上使用 DirectML 啟用 TensorFlow
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: bfd776013e417760d52134d697439be60c5a1ae8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106968122"
---
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a>在 WSL 2 中使用 DirectML 啟用 TensorFlow

此預覽可讓學生和初學者使用 TensorFlow with DirectML 套件，開始在其現有硬體的 ML 空間中建立知識。 完成設定之後，使用者就可以開始使用 [TensorFlow 教學課程模型](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) 或我們的 [DirectML 範例](https://github.com/microsoft/DirectML)。 

> [!NOTE]
> 下列功能適用于 Windows 10 的發行前版本，而且可能會變更。

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>安裝最新的 Windows 測試人員開發人員通道組建 

若要使用此預覽版本，您必須 [註冊 Windows 測試人員計畫](https://insider.windows.com/getting-started/#register)。 完成之後，請遵循 [這些指令](https://insider.windows.com/getting-started/#install) 來安裝最新的 insider build。 選擇您的設定時，請確定您選取的是 [開發通道](/windows-insider/flight-hub/#active-development-builds-of-windows-10)。 

針對此預覽版本，您需要組建20150或更高版本。 您可以透過 `winver` [執行] 命令 (Windows 標誌鍵 + R) 來 **執行** ，以檢查您的組建版本號碼。

## <a name="install-the-preview-gpu-driver"></a>安裝預覽版 GPU 驅動程式 

在 WSL 2 內以 DirectML 套件安裝 TensorFlow 之前，您必須先安裝 GPU 硬體廠商的驅動程式。 這些驅動程式可讓 Windows GPU 使用 WSL 2。

### <a name="amd"></a>AMD 

從他們的網站[下載並安裝 AMD preview 驅動程式](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support)。 此預覽驅動程式支援下列硬體： 

* AMD Radeon™ RX 系列和 Radeon™ VII 圖形。 
* AMD Radeon™ Pro 系列圖形。 
* AMD Ryzen™和 Ryzen™ PRO 處理器與 Radeon™ Vega 圖形。 
* AMD Ryzen™和 Ryzen™ PRO 行動處理器與 Radeon™ Vega 圖形。 

如需相容 AMD 產品的完整清單，請參閱 AMD 版本資訊。 

### <a name="intel"></a>Intel 

[下載並安裝 Intel 的 preview 驅動程式](https://downloadcenter.intel.com/download/29526) ，以便從其網站與 DirectML 搭配使用。 

### <a name="nvidia"></a>NVIDIA 

[下載並安裝 NVIDIA preview 驅動程式](https://developer.nvidia.com/cuda/wsl/download) ，以便從其網站與 DirectML 搭配使用。 如需詳細資訊，請參閱 [Windows 子系統 Linux 版 (WSL) 頁面中的 NVIDIA GPU ](https://developer.nvidia.com/cuda/wsl) 。

## <a name="set-up-the-tensorflow-with-directml-preview"></a>使用 DirectML 預覽設定 TensorFlow 

### <a name="install-wsl-2"></a>安裝 WSL 2 

安裝上述驅動程式之後，請確定您已 [啟用 WSL 2](/windows/wsl/install-win10) 並 [安裝以 glibc 為基礎的散發](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) 套件 (例如 Ubuntu 或 Debian) 。 在我們的測試中，我們使用 Ubuntu。 在 [設定] 應用程式的 [ **Windows Update** ] 區段中選取 [**檢查更新**]，以確定您有最新的核心。 

> [!NOTE]
> 當您啟用更新 Windows 時，請確定您有 **其他 Microsoft 產品的接收更新** 。 您可以在 [設定] 應用程式的 [ **Windows Update** ] 區段內的 [ **Advanced options** ] 中找到它。 

針對此預覽，您需要4.19.121 或更高版本的核心版本。 您可以在 PowerShell 中執行下列命令來檢查版本號碼。 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a>設定 Python 環境 

建議您在 WSL 2 實例內設定虛擬 Python 環境。 您可以使用許多工具來設定虛擬 Python 環境。在這些指示中，我們將使用 [Anaconda 的 Miniconda](https://docs.conda.io/en/latest/miniconda.html)。 此安裝程式的其餘部分假設您使用 miniconda 環境。 

遵循 [Anaconda 網站上的指導](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)方針，或在 WSL 中執行下列命令，以安裝 Miniconda。 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

在 WSL 中安裝 Miniconda 之後，請使用名為 "directml" 的 Python 建立環境，並透過下列命令啟動它。 

> [!NOTE]
> 在下列命令中，我們使用 Python 3.6。 不過，tensorflow directml 套件適用于 Python 3.5、3.6 或3.7 環境。 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a>使用 DirectML 套件安裝 Tensorflow 

藉由執行下列命令，使用 DirectML 後端透過 pip 安裝 TensorFlow 套件。

> [!NOTE]
> Tensorflow-directml 封裝僅支援 TensorFlow 1.15。 

```
pip install tensorflow-directml
```

安裝 tensorflow directml 套件之後，您可以藉由新增兩個張量來確認它是否正確執行。 將下列幾行複製到互動式 Python 會話。 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

您應該會看到類似下列的輸出，並將 add 運算子放置在 DML 裝置上。 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a>Tensorflow 與 DirectML 範例和意見反應 

現在您已經準備好開始深入瞭解 ML 訓練。 查看 [TensorFlow 教學](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) 課程或 [我們的範例](https://github.com/microsoft/DirectML)。 我們已使用此內容作為此初始預覽套件 TensorFlow with DirectML 的驗證。 

如果您遇到問題，或有關于 TensorFlow with DirectML package 的意見反應，請 [與我們的小組聯繫](https://github.com/microsoft/DirectML/issues)。
