---
title: 如何使用 Direct3D 11
description: 本節將示範如何使用 Microsoft Direct3D 11 API 來完成數個常見工作。
ms.assetid: 9BDEDB68-3484-4683-85AF-B583971382C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5613a2ea9a4b8c472c7483e9e29d5ce2d5d2ffccbd3b4ee7d8c65a1621e88c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633048"
---
# <a name="how-to-use-direct3d-11"></a>如何使用 Direct3D 11

本節將示範如何使用 Microsoft Direct3D 11 API 來完成數個常見工作。



| 主題                                                                                                                         | 描述                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [如何：建立參考裝置](overviews-direct3d-11-devices-create-ref.md)<br/>                                  | 本主題說明如何建立參考裝置，以執行執行時間的高度精確、軟體執行。<br/>                                                                                                                                                    |
| [如何：建立變形裝置](overviews-direct3d-11-devices-create-warp.md)<br/>                                      | 本主題說明如何建立可執行高速度軟體轉譯器的變形裝置。<br/>                                                                                                                                                                                  |
| [如何：建立交換鏈](overviews-direct3d-11-devices-create-swap-chain.md)<br/>                                 | 本主題說明如何建立交換鏈，以封裝兩個或多個用於呈現和顯示的緩衝區。 <br/>                                                                                                                                                      |
| [如何：列舉介面卡](overviews-direct3d-11-devices-enum.md)<br/>                                               | 本主題說明如何使用 Microsoft DirectX Graphic Infrastructure (DXGI) 來列舉電腦上可用的圖形配接器。<br/>                                                                                                                                        |
| [如何：取得介面卡顯示模式](overviews-direct3d-11-devices-get-adapter-info.md)<br/>                            | 本主題說明如何使用 DXGI 來取得與介面卡相關聯的有效顯示模式。<br/>                                                                                                                                                                                     |
| [如何：建立裝置和立即內容](overviews-direct3d-11-devices-initialize.md)<br/>                      | 本主題說明如何初始化 [裝置](overviews-direct3d-11-devices-intro.md)。<br/>                                                                                                                                                                                        |
| [如何：取得裝置功能等級](overviews-direct3d-11-devices-downlevel-get.md)<br/>                            | 本主題說明如何取得[裝置](overviews-direct3d-11-devices-intro.md)支援的最高[功能層級](overviews-direct3d-11-devices-downlevel-intro.md)。<br/>                                                                                                   |
| [如何：建立頂點緩衝區](overviews-direct3d-11-resources-buffers-vertex-how-to.md)<br/>                        | 本主題說明如何初始化靜態 [頂點緩衝區](overviews-direct3d-11-resources-buffers-intro.md)，也就是不會變更的頂點緩衝區。<br/>                                                                                                                  |
| [如何：建立索引緩衝區](overviews-direct3d-11-resources-buffers-index-how-to.md)<br/>                         | 本主題說明如何在準備轉譯時初始化 [索引緩衝區](overviews-direct3d-11-resources-buffers-intro.md) 。<br/>                                                                                                                                           |
| [如何：建立常數緩衝區](overviews-direct3d-11-resources-buffers-constant-how-to.md)<br/>                    | 本主題說明如何初始化 [常數緩衝區](overviews-direct3d-11-resources-buffers-intro.md) 以準備轉譯。<br/>                                                                                                                                         |
| [如何：建立材質](overviews-direct3d-11-resources-textures-create.md)<br/>                                    | 本主題說明如何建立材質。<br/>                                                                                                                                                                                                                                       |
| [如何：以程式設計方式初始化材質](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)<br/> | 本主題包含數個範例，示範如何初始化使用不同類型的使用方式所建立的材質。<br/>                                                                                                                                                             |
| [如何：從檔案初始化材質](overviews-direct3d-11-resources-textures-how-to.md)<br/>                    | 本主題說明如何使用 Windows 影像處理元件 (WIC) 來分開建立材質和視圖。<br/>                                                                                                                                                                      |
| [如何：使用動態資源](how-to--use-dynamic-resources.md)<br/>                                                 | 當您的應用程式需要變更這些資源中的資料時，您會建立和使用動態資源。 您可以建立動態使用方式的材質和緩衝區。<br/>                                                                                                                              |
| [如何：建立計算著色器](direct3d-11-advanced-stages-compute-create.md)<br/>                                  | 本主題說明如何建立計算著色器。<br/>                                                                                                                                                                                                                                |
| [如何：設計輪廓著色器](direct3d-11-advanced-stages-hull-shader-design.md)<br/>                                 | 本主題說明如何設計輪廓著色器。<br/>                                                                                                                                                                                                                                  |
| [如何：建立輪廓著色器](direct3d-11-advanced-stages-hull-shader-create.md)<br/>                                 | 本主題說明如何建立輪廓著色器。<br/>                                                                                                                                                                                                                                   |
| [如何：初始化鑲嵌階段](direct3d-11-advanced-stages-tessellator-initialize.md)<br/>                 | 本主題說明如何初始化鑲嵌階段。<br/>                                                                                                                                                                                                                       |
| [如何：設計定義域著色器](direct3d-11-advanced-stages-domain-shader-design.md)<br/>                             | 本主題說明如何設計網域著色器。<br/>                                                                                                                                                                                                                                |
| [如何：建立網域著色器](direct3d-11-advanced-stages-domain-shader-create.md)<br/>                             | 本主題說明如何建立網域著色器。<br/>                                                                                                                                                                                                                                 |
| [如何：編譯著色器](how-to--compile-a-shader.md)<br/>                                                           | 本主題說明如何在執行時間使用 [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) 函式來編譯著色器程式碼。<br/>                                                                                                                                          |
| [如何：錄製命令清單](overviews-direct3d-11-render-multi-thread-command-list-record.md)<br/>                 | 本主題說明如何建立和記錄 [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)。<br/>                                                                                                                                                         |
| [如何：播放命令清單](overviews-direct3d-11-render-multi-thread-command-list-play.md)<br/>                | 本主題說明如何播放 [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)。<br/>                                                                                                                                                                 |
| [如何：檢查驅動程式支援](overviews-direct3d-11-render-multi-thread-support.md)<br/>                          | 本主題說明如何判斷多執行緒功能 (包括 [建立資源](overviews-direct3d-11-render-multi-thread-intro.md) ，以及硬體加速) 支援的 [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md) 。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11 圖形](atoc-dx-graphics-direct3d-11.md)
</dt> </dl>

 

