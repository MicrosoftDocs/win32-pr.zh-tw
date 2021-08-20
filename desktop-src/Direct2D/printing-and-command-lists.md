---
title: 列印和命令清單
description: Direct2D \ 32; 列印控制項是 Windows 8 之 Direct2D 模組中的新元件。
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0026071ce8e78fc2ea946e0fffff2993e32ab48a2a20d4de6cdb12ca9b1eaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075044"
---
# <a name="printing-and-command-lists"></a>列印和命令清單

[Direct2D](./direct2d-portal.md) [**列印控制項**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)是 Windows 8 之 Direct2D 模組中的新元件。 此元件可讓 Direct2D apps 重複使用其 Direct2D 繪圖呼叫 (的狀態變更和轉譯基本) ，以提供類似您在螢幕上所看到的列印結果。

[**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)介面代表虛擬列印工作：您可以建立 [Direct2D](./direct2d-portal.md)列印控制項來起始新的列印工作、針對您要列印的每個頁面傳入 Direct2D 內容，然後關閉列印控制項來完成列印工作。

> [!Note]  
> 列印控制項只會對應到一項列印工作，您也無法重複使用它。

[Direct2D](./direct2d-portal.md)列印控制項會轉換和優化針對列印子系統所傳入的 Direct2D 內容，這可與真實的印表機搭配使用，以提供實際的列印結果。 Direct2D apps 不會隱藏所有列印特定的詳細資料，這表示 Direct2D apps 可以列印，而不需要知道其繪製的裝置，或如何將繪圖轉譯成列印。

若要使用 [Direct2D](./direct2d-portal.md)進行列印，您需要為您想要列印的每個頁面準備一個 Direct2D 命令清單，然後將該命令清單傳遞給 Direct2D 列印控制項。 若要準備該 Direct2D 命令清單，您只需建立命令清單，並將其設定為目前裝置內容的繪製目標，然後繪製至該裝置內容，就像您繪製到點陣圖目標以供顯示一樣。 如需裝置和目標的詳細資訊，請參閱 [裝置和裝置](devices-and-device-contexts.md) 內容。

下圖說明應用程式、裝置內容、點陣圖目標、命令清單目標和列印控制項之間的互動。

> [!Note]  
> Windows 列印 Sub-System 和印表機元件都是灰色，因為它們完全隱藏在[Direct2D](./direct2d-portal.md) apps 中。

![顯示 commandlist 和列印如何與應用程式和 direct2d 互動的圖表。](images/d2dprintcontroldiagram.png)

## <a name="example"></a>範例

列印 Direct2D 內容的完整流程包含下列步驟。

1.  建立列印控制項來起始列印工作。
2.  藉由傳入命令清單，將頁面加入至列印控制項。
3.  針對檔其餘部分中的每個頁面重複步驟2
4.  關閉列印控制項以完成列印工作。

以下是顯示進程的程式碼範例。

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a>相關主題

[**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[改善 Direct2D 應用程式和列印的效能](improving-direct2d-performance.md)