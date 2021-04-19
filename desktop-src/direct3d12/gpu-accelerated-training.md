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
# <a name="gpu-accelerated-ml-training"></a>GPU 加速 ML 訓練

![Windows ML 圖形](images/winml-graphic.png)

本檔涵蓋 [Windows 子系統 Linux 版](/windows/wsl/about) (WSL) 和原生 WINDOWS 的 GPU 加速機器學習服務 (ML) 訓練預覽中目前支援的功能。  

此預覽支援專業和初學者案例。 您可以在下面找到逐步指南的指示，瞭解如何根據您的 ML、GPU 廠商和您想要使用的軟體程式庫中的專業知識層級，來取得系統設定。 

> [!NOTE]
> 下列功能目前處於預覽狀態，可能會變更。


## <a name="professionals"></a>專業 人士

如果您是一位專業資料科學家，使用原生 Linux 環境進行內部迴圈 ML 開發和實驗，而且您有 NVIDIA GPU，建議您 [在 WSL 2 中設定 NVIDIA CUDA preview。](gpu-cuda-in-wsl.md)

## <a name="students-and-beginners"></a>學生和初學者 

如果您是想要開始在 ML 空間中建立知識的學生或初學者，建議您使用 DirectML 後端套件來設定 TensorFlow。 此封裝目前會加速 AMD 和 Intel Gpu 上的工作流程。 即將推出支援 NVIDIA Gpu。 

針對熟悉開始使用 ML 工作流程的原生 Linux 環境，我們建議您在 [WSL 2 內以 DirectML 套件執行 TensorFlow](gpu-tensorflow-wsl.md)。 

針對更熟悉使用 ML 工作流程的 Windows，建議您 [在原生 Windows 上使用 DirectML 套件](gpu-tensorflow-windows.md)來設定 TensorFlow。 

## <a name="next-steps"></a>下一步

* [在 WSL 2 中啟用 NVIDIA CUDA preview](gpu-cuda-in-wsl.md)。
* [在 WSL 2 內使用 DirectML 套件啟用 TensorFlow](gpu-tensorflow-wsl.md)。
* [在原生 Windows 上使用 DirectML 套件啟用 TensorFlow](gpu-tensorflow-windows.md)。