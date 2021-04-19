---
title: 在 Windows 上使用 DirectML 的 Tensorflow
description: 在 Windows 上直接使用 DirectML 啟用 TensorFlow
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 665ba456d59f09f27a435135468cf71cb6f6f014
ms.sourcegitcommit: 8f3fb56ebad4615389dec5c74d965dec84ad4123
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/22/2020
ms.locfileid: "106965227"
---
# <a name="enable-tensorflow-with-directml-on-windows"></a><span data-ttu-id="32761-103">在 Windows 上使用 DirectML 啟用 TensorFlow</span><span class="sxs-lookup"><span data-stu-id="32761-103">Enable TensorFlow with DirectML on Windows</span></span>

<span data-ttu-id="32761-104">這項預覽可讓學生和初學者使用 TensorFlow with DirectML 封裝，開始在其現有硬體的 ML 空間中建立知識。</span><span class="sxs-lookup"><span data-stu-id="32761-104">This preview provides students and beginners a way to start building their knowledge in the ML space on their existing hardware by using the the TensorFlow with DirectML package.</span></span> <span data-ttu-id="32761-105">完成設定之後，使用者就可以開始使用 [TensorFlow 教學課程模型](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) 或 [我們的 DirectML 範例](https://github.com/microsoft/DirectML)。</span><span class="sxs-lookup"><span data-stu-id="32761-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="32761-106">下列功能目前處於預覽狀態，可能會變更。</span><span class="sxs-lookup"><span data-stu-id="32761-106">The following feature is in preview, and are subject to change.</span></span>

## <a name="check-your-version-of-windows"></a><span data-ttu-id="32761-107">檢查您的 Windows 版本</span><span class="sxs-lookup"><span data-stu-id="32761-107">Check your version of Windows</span></span> 

<span data-ttu-id="32761-108">原生 Windows 上的 TensorFlow with DirectML 封裝的運作方式，是從 Windows 10 1709 版 (組建16299或更高版本的) 開始。</span><span class="sxs-lookup"><span data-stu-id="32761-108">The TensorFlow with DirectML package on native Windows works starting with Windows 10 Version 1709 (Build 16299 or higher).</span></span> <span data-ttu-id="32761-109">您可以透過 `winver` [執行] 命令 (Windows 標誌鍵 + R) 來 **執行** ，以檢查您的組建版本號碼。</span><span class="sxs-lookup"><span data-stu-id="32761-109">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="check-for-gpu-driver-updates"></a><span data-ttu-id="32761-110">檢查 GPU 驅動程式更新</span><span class="sxs-lookup"><span data-stu-id="32761-110">Check for GPU driver updates</span></span> 

<span data-ttu-id="32761-111">確定您已安裝最新的 GPU 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="32761-111">Ensure you have the latest GPU driver installed.</span></span> <span data-ttu-id="32761-112">在 [設定] 應用程式的 [ **Windows Update** ] 區段中，選取 [**檢查更新**]。</span><span class="sxs-lookup"><span data-stu-id="32761-112">Select **Check for updates** in the **Windows Update** section of the Settings app.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="32761-113">使用 DirectML 預覽設定 TensorFlow</span><span class="sxs-lookup"><span data-stu-id="32761-113">Set up the TensorFlow with DirectML preview</span></span> 

<span data-ttu-id="32761-114">建議您在 Windows 中設定虛擬 Python 環境。</span><span class="sxs-lookup"><span data-stu-id="32761-114">We recommend setting up a virtual Python environment inside Windows.</span></span> <span data-ttu-id="32761-115">您可以使用許多工具來設定虛擬 Python 環境。在這些指示中，我們將使用 [Anaconda 的 Miniconda](https://docs.conda.io/en/latest/miniconda.html)。</span><span class="sxs-lookup"><span data-stu-id="32761-115">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="32761-116">此安裝程式的其餘部分假設您使用 miniconda 環境。</span><span class="sxs-lookup"><span data-stu-id="32761-116">The rest of this setup assumes you use a miniconda environment.</span></span> 

### <a name="set-up-python-environment"></a><span data-ttu-id="32761-117">設定 Python 環境</span><span class="sxs-lookup"><span data-stu-id="32761-117">Set up Python environment</span></span> 

<span data-ttu-id="32761-118">在您的系統上下載並安裝 [Miniconda Windows installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) 。</span><span class="sxs-lookup"><span data-stu-id="32761-118">Download and install the [Miniconda Windows installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) on your system.</span></span> <span data-ttu-id="32761-119">Anaconda 網站上的 [安裝程式有額外的指導](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) 方針。</span><span class="sxs-lookup"><span data-stu-id="32761-119">There is [additional guidance for setup](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) on Anaconda’s site.</span></span> <span data-ttu-id="32761-120">安裝 Miniconda 之後，請使用名為 **directml** 的 Python 建立環境，並透過下列命令啟動它。</span><span class="sxs-lookup"><span data-stu-id="32761-120">Once Miniconda is installed, create an environment using Python named **directml** and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="32761-121">在下列命令中，我們使用 Python 3.6。</span><span class="sxs-lookup"><span data-stu-id="32761-121">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="32761-122">不過，tensorflow directml 套件適用于 Python 3.5、3.6 或3.7 環境。</span><span class="sxs-lookup"><span data-stu-id="32761-122">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="32761-123">使用 DirectML 套件安裝 Tensorflow</span><span class="sxs-lookup"><span data-stu-id="32761-123">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="32761-124">藉由執行下列命令，使用 DirectML 後端透過 pip 安裝 TensorFlow 套件。</span><span class="sxs-lookup"><span data-stu-id="32761-124">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="32761-125">Tensorflow-directml 封裝僅支援 TensorFlow 1.15。</span><span class="sxs-lookup"><span data-stu-id="32761-125">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="32761-126">安裝 tensorflow directml 套件之後，您可以藉由新增兩個張量來確認它是否正確執行。</span><span class="sxs-lookup"><span data-stu-id="32761-126">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="32761-127">將下列幾行複製到互動式 Python 會話。</span><span class="sxs-lookup"><span data-stu-id="32761-127">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="32761-128">您應該會看到類似下列的輸出，並將 add 運算子放置在 DML 裝置上。</span><span class="sxs-lookup"><span data-stu-id="32761-128">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library DirectMLba106a7c621ea741d2159d8708ee581c11918380.dll 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="32761-129">Tensorflow 與 DirectML 範例和意見反應</span><span class="sxs-lookup"><span data-stu-id="32761-129">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="32761-130">現在您已經準備好開始深入瞭解 ML 訓練。</span><span class="sxs-lookup"><span data-stu-id="32761-130">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="32761-131">查看 [TensorFlow 教學](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) 課程或 [我們的範例](https://github.com/microsoft/DirectML)。</span><span class="sxs-lookup"><span data-stu-id="32761-131">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="32761-132">我們使用此內容做為具有 DirectML 後端之 TensorFlow 初始預覽套件的驗證。</span><span class="sxs-lookup"><span data-stu-id="32761-132">We used this content as validation for this initial preview package of TensorFlow with a DirectML backend.</span></span> 

<span data-ttu-id="32761-133">如果您遇到問題，或有關于 TensorFlow with DirectML package 的意見反應，請 [與我們的小組聯繫](https://github.com/microsoft/DirectML/issues)。</span><span class="sxs-lookup"><span data-stu-id="32761-133">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span> 
