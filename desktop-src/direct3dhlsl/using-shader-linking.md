---
title: 使用著色器連結
description: 我們會示範如何建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7528415f1bedb0364a9c4b09126a983222fc42b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683011"
---
# <a name="using-shader-linking"></a>使用著色器連結

我們會示範如何建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。 從 Windows 8.1 開始支援著色器連結。

**目標：** 瞭解如何使用著色器連結。

## <a name="prerequisites"></a>必要條件

我們假設您熟悉 C++。 您還需要圖形程式設計概念的基本經驗。

**完成的總時間：** 60 分鐘。

## <a name="where-to-go-from-here"></a>現在該如何開始

另請參閱 [HLSL 編譯器 api](dx-graphics-d3dcompiler-reference.md)。

我們將示範如何：

-   編譯著色器程式碼
-   將已編譯的程式碼載入著色器程式庫
-   將來源位置的資源系結至目的地位置
-   建立著色器的函式連結圖形 (FLGs) 
-   連結著色器圖形與著色器程式庫，以產生 Direct3D 執行時間可使用的著色器 blob

接下來我們要建立著色器程式庫，並將來源位置的資源系結至目的地位置。

[封裝著色器程式庫](pachaging-a-shader-library.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Direct3D 11 圖形](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[DXGI](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 