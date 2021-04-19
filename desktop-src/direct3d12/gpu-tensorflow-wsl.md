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
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a><span data-ttu-id="93891-103">在 WSL 2 中使用 DirectML 啟用 TensorFlow</span><span class="sxs-lookup"><span data-stu-id="93891-103">Enable TensorFlow with DirectML in WSL 2</span></span>

<span data-ttu-id="93891-104">此預覽可讓學生和初學者使用 TensorFlow with DirectML 套件，開始在其現有硬體的 ML 空間中建立知識。</span><span class="sxs-lookup"><span data-stu-id="93891-104">This preview provides students and beginners a way to start building knowledge in the ML space on their existing hardware by using the TensorFlow with DirectML package.</span></span> <span data-ttu-id="93891-105">完成設定之後，使用者就可以開始使用 [TensorFlow 教學課程模型](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) 或我們的 [DirectML 範例](https://github.com/microsoft/DirectML)。</span><span class="sxs-lookup"><span data-stu-id="93891-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or our [DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="93891-106">下列功能適用于 Windows 10 的發行前版本，而且可能會變更。</span><span class="sxs-lookup"><span data-stu-id="93891-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="93891-107">安裝最新的 Windows 測試人員開發人員通道組建</span><span class="sxs-lookup"><span data-stu-id="93891-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="93891-108">若要使用此預覽版本，您必須 [註冊 Windows 測試人員計畫](https://insider.windows.com/getting-started/#register)。</span><span class="sxs-lookup"><span data-stu-id="93891-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="93891-109">完成之後，請遵循 [這些指令](https://insider.windows.com/getting-started/#install) 來安裝最新的 insider build。</span><span class="sxs-lookup"><span data-stu-id="93891-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest insider build.</span></span> <span data-ttu-id="93891-110">選擇您的設定時，請確定您選取的是 [開發通道](/windows-insider/flight-hub/#active-development-builds-of-windows-10)。</span><span class="sxs-lookup"><span data-stu-id="93891-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="93891-111">針對此預覽版本，您需要組建20150或更高版本。</span><span class="sxs-lookup"><span data-stu-id="93891-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="93891-112">您可以透過 `winver` [執行] 命令 (Windows 標誌鍵 + R) 來 **執行** ，以檢查您的組建版本號碼。</span><span class="sxs-lookup"><span data-stu-id="93891-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="93891-113">安裝預覽版 GPU 驅動程式</span><span class="sxs-lookup"><span data-stu-id="93891-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="93891-114">在 WSL 2 內以 DirectML 套件安裝 TensorFlow 之前，您必須先安裝 GPU 硬體廠商的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="93891-114">Before installing the TensorFlow with DirectML package inside WSL 2, you need to install drivers from your GPU hardware vendor.</span></span> <span data-ttu-id="93891-115">這些驅動程式可讓 Windows GPU 使用 WSL 2。</span><span class="sxs-lookup"><span data-stu-id="93891-115">These drivers enable the Windows GPU to work with WSL 2.</span></span>

### <a name="amd"></a><span data-ttu-id="93891-116">AMD</span><span class="sxs-lookup"><span data-stu-id="93891-116">AMD</span></span> 

<span data-ttu-id="93891-117">從他們的網站[下載並安裝 AMD preview 驅動程式](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support)。</span><span class="sxs-lookup"><span data-stu-id="93891-117">[Download and install AMD’s preview driver](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) from their website.</span></span> <span data-ttu-id="93891-118">此預覽驅動程式支援下列硬體：</span><span class="sxs-lookup"><span data-stu-id="93891-118">This preview driver supports the following hardware:</span></span> 

* <span data-ttu-id="93891-119">AMD Radeon™ RX 系列和 Radeon™ VII 圖形。</span><span class="sxs-lookup"><span data-stu-id="93891-119">AMD Radeon™ RX series and Radeon™ VII graphics.</span></span> 
* <span data-ttu-id="93891-120">AMD Radeon™ Pro 系列圖形。</span><span class="sxs-lookup"><span data-stu-id="93891-120">AMD Radeon™ Pro series graphics.</span></span> 
* <span data-ttu-id="93891-121">AMD Ryzen™和 Ryzen™ PRO 處理器與 Radeon™ Vega 圖形。</span><span class="sxs-lookup"><span data-stu-id="93891-121">AMD Ryzen™ and Ryzen™ PRO Processors with Radeon™ Vega graphics.</span></span> 
* <span data-ttu-id="93891-122">AMD Ryzen™和 Ryzen™ PRO 行動處理器與 Radeon™ Vega 圖形。</span><span class="sxs-lookup"><span data-stu-id="93891-122">AMD Ryzen™ and Ryzen™ PRO Mobile Processors with Radeon™ Vega graphics.</span></span> 

<span data-ttu-id="93891-123">如需相容 AMD 產品的完整清單，請參閱 AMD 版本資訊。</span><span class="sxs-lookup"><span data-stu-id="93891-123">For a complete list of compatible AMD products, please refer to the AMD Release Notes.</span></span> 

### <a name="intel"></a><span data-ttu-id="93891-124">Intel</span><span class="sxs-lookup"><span data-stu-id="93891-124">Intel</span></span> 

<span data-ttu-id="93891-125">[下載並安裝 Intel 的 preview 驅動程式](https://downloadcenter.intel.com/download/29526) ，以便從其網站與 DirectML 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="93891-125">[Download and install Intel’s preview driver](https://downloadcenter.intel.com/download/29526) to use with DirectML from their website.</span></span> 

### <a name="nvidia"></a><span data-ttu-id="93891-126">NVIDIA</span><span class="sxs-lookup"><span data-stu-id="93891-126">NVIDIA</span></span> 

<span data-ttu-id="93891-127">[下載並安裝 NVIDIA preview 驅動程式](https://developer.nvidia.com/cuda/wsl/download) ，以便從其網站與 DirectML 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="93891-127">[Download and install NVIDIA's preview driver](https://developer.nvidia.com/cuda/wsl/download) to use with DirectML from their website.</span></span> <span data-ttu-id="93891-128">如需詳細資訊，請參閱 [Windows 子系統 Linux 版 (WSL) 頁面中的 NVIDIA GPU ](https://developer.nvidia.com/cuda/wsl) 。</span><span class="sxs-lookup"><span data-stu-id="93891-128">For more information, see [NVIDIA's GPU in Windows Subsystem for Linux (WSL)](https://developer.nvidia.com/cuda/wsl) page.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="93891-129">使用 DirectML 預覽設定 TensorFlow</span><span class="sxs-lookup"><span data-stu-id="93891-129">Set up the TensorFlow with DirectML preview</span></span> 

### <a name="install-wsl-2"></a><span data-ttu-id="93891-130">安裝 WSL 2</span><span class="sxs-lookup"><span data-stu-id="93891-130">Install WSL 2</span></span> 

<span data-ttu-id="93891-131">安裝上述驅動程式之後，請確定您已 [啟用 WSL 2](/windows/wsl/install-win10) 並 [安裝以 glibc 為基礎的散發](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) 套件 (例如 Ubuntu 或 Debian) 。</span><span class="sxs-lookup"><span data-stu-id="93891-131">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (like Ubuntu or Debian).</span></span> <span data-ttu-id="93891-132">在我們的測試中，我們使用 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="93891-132">For our testing, we used Ubuntu.</span></span> <span data-ttu-id="93891-133">在 [設定] 應用程式的 [ **Windows Update** ] 區段中選取 [**檢查更新**]，以確定您有最新的核心。</span><span class="sxs-lookup"><span data-stu-id="93891-133">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="93891-134">當您啟用更新 Windows 時，請確定您有 **其他 Microsoft 產品的接收更新** 。</span><span class="sxs-lookup"><span data-stu-id="93891-134">Ensure you have the **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="93891-135">您可以在 [設定] 應用程式的 [ **Windows Update** ] 區段內的 [ **Advanced options** ] 中找到它。</span><span class="sxs-lookup"><span data-stu-id="93891-135">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="93891-136">針對此預覽，您需要4.19.121 或更高版本的核心版本。</span><span class="sxs-lookup"><span data-stu-id="93891-136">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="93891-137">您可以在 PowerShell 中執行下列命令來檢查版本號碼。</span><span class="sxs-lookup"><span data-stu-id="93891-137">You can check the version number by running the following command in PowerShell.</span></span> 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a><span data-ttu-id="93891-138">設定 Python 環境</span><span class="sxs-lookup"><span data-stu-id="93891-138">Set up Python environment</span></span> 

<span data-ttu-id="93891-139">建議您在 WSL 2 實例內設定虛擬 Python 環境。</span><span class="sxs-lookup"><span data-stu-id="93891-139">We recommend setting up a virtual Python environment inside your WSL 2 instance.</span></span> <span data-ttu-id="93891-140">您可以使用許多工具來設定虛擬 Python 環境。在這些指示中，我們將使用 [Anaconda 的 Miniconda](https://docs.conda.io/en/latest/miniconda.html)。</span><span class="sxs-lookup"><span data-stu-id="93891-140">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="93891-141">此安裝程式的其餘部分假設您使用 miniconda 環境。</span><span class="sxs-lookup"><span data-stu-id="93891-141">The rest of this setup assumes you use a miniconda environment.</span></span> 

<span data-ttu-id="93891-142">遵循 [Anaconda 網站上的指導](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)方針，或在 WSL 中執行下列命令，以安裝 Miniconda。</span><span class="sxs-lookup"><span data-stu-id="93891-142">Install Miniconda by following the [guidance on Anaconda’s site](https://conda.io/projects/conda/en/latest/user-guide/install/index.html), or by running the following commands in WSL.</span></span> 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

<span data-ttu-id="93891-143">在 WSL 中安裝 Miniconda 之後，請使用名為 "directml" 的 Python 建立環境，並透過下列命令啟動它。</span><span class="sxs-lookup"><span data-stu-id="93891-143">Once Miniconda is installed in WSL, create an environment using Python named “directml” and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="93891-144">在下列命令中，我們使用 Python 3.6。</span><span class="sxs-lookup"><span data-stu-id="93891-144">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="93891-145">不過，tensorflow directml 套件適用于 Python 3.5、3.6 或3.7 環境。</span><span class="sxs-lookup"><span data-stu-id="93891-145">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="93891-146">使用 DirectML 套件安裝 Tensorflow</span><span class="sxs-lookup"><span data-stu-id="93891-146">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="93891-147">藉由執行下列命令，使用 DirectML 後端透過 pip 安裝 TensorFlow 套件。</span><span class="sxs-lookup"><span data-stu-id="93891-147">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="93891-148">Tensorflow-directml 封裝僅支援 TensorFlow 1.15。</span><span class="sxs-lookup"><span data-stu-id="93891-148">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="93891-149">安裝 tensorflow directml 套件之後，您可以藉由新增兩個張量來確認它是否正確執行。</span><span class="sxs-lookup"><span data-stu-id="93891-149">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="93891-150">將下列幾行複製到互動式 Python 會話。</span><span class="sxs-lookup"><span data-stu-id="93891-150">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="93891-151">您應該會看到類似下列的輸出，並將 add 運算子放置在 DML 裝置上。</span><span class="sxs-lookup"><span data-stu-id="93891-151">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="93891-152">Tensorflow 與 DirectML 範例和意見反應</span><span class="sxs-lookup"><span data-stu-id="93891-152">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="93891-153">現在您已經準備好開始深入瞭解 ML 訓練。</span><span class="sxs-lookup"><span data-stu-id="93891-153">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="93891-154">查看 [TensorFlow 教學](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) 課程或 [我們的範例](https://github.com/microsoft/DirectML)。</span><span class="sxs-lookup"><span data-stu-id="93891-154">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="93891-155">我們已使用此內容作為此初始預覽套件 TensorFlow with DirectML 的驗證。</span><span class="sxs-lookup"><span data-stu-id="93891-155">We used this content as validation for this initial preview package of TensorFlow with DirectML.</span></span> 

<span data-ttu-id="93891-156">如果您遇到問題，或有關于 TensorFlow with DirectML package 的意見反應，請 [與我們的小組聯繫](https://github.com/microsoft/DirectML/issues)。</span><span class="sxs-lookup"><span data-stu-id="93891-156">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span>
