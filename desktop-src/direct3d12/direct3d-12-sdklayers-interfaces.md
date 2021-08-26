---
title: Debug 圖層介面
description: 下列介面是在 d3d12sdklayers 中宣告。
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d7e16d6c593f2dcfcc46266102ac15a61386ef
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812872"
---
# <a name="debug-layer-interfaces"></a>Debug 圖層介面

下列介面是在中定義 `d3d12sdklayers.h` 。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**ID3D12Debug**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | Debug 介面會控制 debug 設定並驗證管線狀態。 只有在開啟 debug 層時，才能使用它。 |
| [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | 將以 GPU 為基礎的驗證和相依的命令佇列同步處理新增至 debug 圖層。 |
| [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | 加入可設定的 GPU-Based 驗證層級。 |
| [**ID3D12Debug3**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | 新增至 debug layer GPU 型驗證、相依的命令佇列同步處理，以及可設定的 GPU 型驗證層級。 |
| [**ID3D12Debug4**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug4) | 新增停用 debug 層的功能。 |
| [**ID3D12Debug5**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug5) | 將設定自動命名物件的能力新增至 debug 圖層。 |
| [**ID3D12DebugCommandList**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | 提供監視和偵測命令清單的方法。 |
| [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | 此介面可讓您修改其他命令清單的調試層設定。 |
| [**ID3D12DebugCommandQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | 提供監視和偵測命令佇列的方法。 |
| [**ID3D12DebugDevice**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | 此介面代表要進行偵錯工具的圖形裝置。 |
| [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | 指定全裝置的調試層設定。 |
| [**ID3D12InfoQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | 資訊佇列介面會儲存、抓取及篩選 debug 訊息。 佇列包含訊息佇列、選擇性的儲存體篩選堆疊，以及選擇性的抓取篩選堆疊。 |
| [**ID3D12SharingContract**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | D3D11On12 診斷層和圖形診斷工具之間的合約的一部分。 |

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 12 程式設計環境設定](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Debug 圖層參考](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Direct3D 12 參考](direct3d-12-reference.md)
</dt> </dl>