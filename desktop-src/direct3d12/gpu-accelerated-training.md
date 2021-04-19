---
title: WSL 中的 GPU 加速
description: 直接 Machine Learning (DirectML) 支援 GPU accelleration Windows 子系統 Linux 版
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 217a1763c0030a856e10a822cbd9f2642480c056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966883"
---
# <a name="gpu-accelerated-ml-training"></a><span data-ttu-id="56dcb-103">GPU 加速 ML 訓練</span><span class="sxs-lookup"><span data-stu-id="56dcb-103">GPU accelerated ML training</span></span>

![Windows ML 圖形](images/winml-graphic.png)

<span data-ttu-id="56dcb-105">本檔涵蓋 [Windows 子系統 Linux 版](/windows/wsl/about) (WSL) 和原生 WINDOWS 的 GPU 加速機器學習服務 (ML) 訓練預覽中目前支援的功能。</span><span class="sxs-lookup"><span data-stu-id="56dcb-105">This documentation covers what is currently supported by the GPU accelerated machine learning (ML) training preview for the [Windows Subsystem for Linux](/windows/wsl/about) (WSL) and native Windows.</span></span>  

<span data-ttu-id="56dcb-106">此預覽支援專業和初學者案例。</span><span class="sxs-lookup"><span data-stu-id="56dcb-106">This preview supports both professional and beginner scenarios.</span></span> <span data-ttu-id="56dcb-107">您可以在下面找到逐步指南的指示，瞭解如何根據您的 ML、GPU 廠商和您想要使用的軟體程式庫中的專業知識層級，來取得系統設定。</span><span class="sxs-lookup"><span data-stu-id="56dcb-107">Below you will find pointers to step-by-step guides on how to get your system setup depending on your level of expertise in ML, GPU vendor, and the software library you intend to use.</span></span> 

> [!NOTE]
> <span data-ttu-id="56dcb-108">下列功能目前處於預覽狀態，可能會變更。</span><span class="sxs-lookup"><span data-stu-id="56dcb-108">The following features are in preview, and are subject to change.</span></span>


## <a name="professionals"></a><span data-ttu-id="56dcb-109">專業 人士</span><span class="sxs-lookup"><span data-stu-id="56dcb-109">Professionals</span></span>

<span data-ttu-id="56dcb-110">如果您是一位專業資料科學家，使用原生 Linux 環境進行內部迴圈 ML 開發和實驗，而且您有 NVIDIA GPU，建議您 [在 WSL 2 中設定 NVIDIA CUDA preview。](gpu-cuda-in-wsl.md)</span><span class="sxs-lookup"><span data-stu-id="56dcb-110">If you’re a professional data scientist that uses a native Linux environment day-to-day for inner-loop ML development and experimentation, and you have an NVIDIA GPU, we recommend setting up the [NVIDIA CUDA preview in WSL 2.](gpu-cuda-in-wsl.md)</span></span>

## <a name="students-and-beginners"></a><span data-ttu-id="56dcb-111">學生和初學者</span><span class="sxs-lookup"><span data-stu-id="56dcb-111">Students and beginners</span></span> 

<span data-ttu-id="56dcb-112">如果您是想要開始在 ML 空間中建立知識的學生或初學者，建議您使用 DirectML 後端套件來設定 TensorFlow。</span><span class="sxs-lookup"><span data-stu-id="56dcb-112">If you’re a student or beginner looking to start building your knowledge in the ML space, we recommend setting up the TensorFlow with DirectML backend package.</span></span> <span data-ttu-id="56dcb-113">此封裝目前會加速 AMD 和 Intel Gpu 上的工作流程。</span><span class="sxs-lookup"><span data-stu-id="56dcb-113">This package currently accelerates workflows on AMD and Intel GPUs.</span></span> <span data-ttu-id="56dcb-114">即將推出支援 NVIDIA Gpu。</span><span class="sxs-lookup"><span data-stu-id="56dcb-114">Support for NVIDIA GPUs is coming soon.</span></span> 

<span data-ttu-id="56dcb-115">針對熟悉開始使用 ML 工作流程的原生 Linux 環境，我們建議您在 [WSL 2 內以 DirectML 套件執行 TensorFlow](gpu-tensorflow-wsl.md)。</span><span class="sxs-lookup"><span data-stu-id="56dcb-115">For those more familiar with a native Linux environment that are getting started with ML workflows, we recommend running the [TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span> 

<span data-ttu-id="56dcb-116">針對更熟悉使用 ML 工作流程的 Windows，建議您 [在原生 Windows 上使用 DirectML 套件](gpu-tensorflow-windows.md)來設定 TensorFlow。</span><span class="sxs-lookup"><span data-stu-id="56dcb-116">For those more familiar with Windows that are getting started with ML workflows, we recommend setting up the [TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span> 

## <a name="next-steps"></a><span data-ttu-id="56dcb-117">下一步</span><span class="sxs-lookup"><span data-stu-id="56dcb-117">Next steps</span></span>

* <span data-ttu-id="56dcb-118">[在 WSL 2 中啟用 NVIDIA CUDA preview](gpu-cuda-in-wsl.md)。</span><span class="sxs-lookup"><span data-stu-id="56dcb-118">[Enable NVIDIA CUDA preview in WSL 2](gpu-cuda-in-wsl.md).</span></span>
* <span data-ttu-id="56dcb-119">[在 WSL 2 內使用 DirectML 套件啟用 TensorFlow](gpu-tensorflow-wsl.md)。</span><span class="sxs-lookup"><span data-stu-id="56dcb-119">[Enable TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span>
* <span data-ttu-id="56dcb-120">[在原生 Windows 上使用 DirectML 套件啟用 TensorFlow](gpu-tensorflow-windows.md)。</span><span class="sxs-lookup"><span data-stu-id="56dcb-120">[Enable TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span>