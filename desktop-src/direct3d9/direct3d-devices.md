---
description: Direct3D 裝置是 Direct3D 的轉譯元件。 它會封裝和儲存呈現狀態。 此外，Direct3D 裝置會執行轉換和燈光作業，並將影像柵格化至介面。
ms.assetid: b592edb8-351a-4a82-9ff7-8a69d82723bc
title: 'Direct3d 裝置 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07726069b952ba99d608e5f36df8e1fb7745cd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187464"
---
# <a name="direct3d-devices-direct3d-9"></a>Direct3d 裝置 (Direct3D 9) 

Direct3D 裝置是 Direct3D 的轉譯元件。 它會封裝和儲存呈現狀態。 此外，Direct3D 裝置會執行轉換和燈光作業，並將影像柵格化至介面。

-   [XPDM 和 WDDM](xpdm-vs-wddm.md)
-   [ (Direct3D 9) 的裝置類型 ](device-types.md)
-   [ (Direct3D 9) 建立裝置 ](creating-a-device.md)
-   [ (Direct3D 9) 的視窗型 vs Full-Screen 模式 ](windowed-vs-full-screen-mode.md)
-   [選取 (Direct3D 9) 的裝置 ](selecting-a-device.md)
-   [ (Direct3D 9) 的裝置遺失 ](lost-devices.md)
-   [判斷 (Direct3D 9) 的硬體支援 ](determining-hardware-support.md)
-   [處理 (Direct3D 9) 的頂點資料 ](processing-vertex-data.md)
-   [基本](primitives.md)

架構上來說，Direct3D 裝置包含轉換模組、光源模組及點陣化模組，如下圖所示。

![Direct3D 裝置架構圖](images/d3ddev.png)

Direct3D 目前支援兩種主要類型的 Direct3D 裝置：

-   具有硬體加速點陣化的 HAL 裝置，以及同時具有硬體和軟體頂點處理的著色
-   參照裝置

您可以將這些裝置視為兩個不同的驅動程式。 軟體與參照裝置是由軟體驅動程式表示，而 hal 裝置是由硬體驅動程式表示。 利用這些裝置的最常見方式是使用 hal 裝置傳送應用程式，以及參照裝置用於功能測試。 這些是由協力廠商提供，用來模擬特定裝置 - 例如尚未發行的開發中硬體。

應用程式建立的 Direct3D 裝置必須符合應用程式執行所在硬體的功能。 Direct3D 提供轉譯功能，可透過存取電腦上安裝的 3D 硬體，或藉由模擬軟體中的 3D 硬體功能。 因此，Direct3D 提供裝置同時用於硬體存取和軟體模擬。

硬體加速裝置提供的效能比軟體裝置好很多。 所有支援圖形卡的 Direct3D 上都提供 hal 裝置類型。 在大部分案例中，應用程式會以有硬體加速且依賴軟體模擬的電腦為目標，以配合較低階的電腦。

參照裝置則例外，軟體裝置不一定與硬體裝置支援相同的功能。 應用程式應該永遠查詢裝置功能，以判斷支援哪些功能。

由於 Direct3D 9 提供的軟體和參照裝置行為與 hal 裝置提供的相同，因此為搭配 hal 裝置所撰寫的應用程式程式碼將可搭配軟體或參照裝置運作，不需修改。 請注意，雖然提供的軟體或參考裝置行為與 hal 裝置的行為完全相同，但裝置功能的確不同，而特定軟體裝置可能會執行一組較小的功能。

## <a name="behaviors"></a>行為

Direct3D 可讓您指定裝置的行為，以及裝置的類型。 [**IDirect3D9：： CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)方法可結合一或多個行為旗標，以控制 Direct3D 裝置的全域行為。 這些行為會指定在 Direct3D 的執行時間部分中不會維護什麼，而且裝置類型會指定要使用的驅動程式。 雖然某些裝置行為組合無效，但您可以使用所有裝置類型的所有裝置行為。 例如， \_ 在使用 D3DCREATE PUREDEVICE 建立的裝置上指定 D3DDEVTYPE SW 是有效的 \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速入門](getting-started.md)
</dt> </dl>

 

 
