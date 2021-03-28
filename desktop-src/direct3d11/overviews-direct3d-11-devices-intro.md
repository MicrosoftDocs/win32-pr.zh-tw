---
title: Direct3D 11 中的裝置簡介
description: Direct3D 11 物件模型會將資源建立和轉譯功能區分為裝置和一或多個內容。這項分隔是設計來協助多執行緒處理。
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b03333c6594f17d85fee28880e46928241e06c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971397"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a>Direct3D 11 中的裝置簡介

Direct3D 11 物件模型會將資源建立和轉譯功能區分為裝置和一或多個內容。這項分隔是設計來協助多執行緒處理。

-   [裝置](#introduction-to-a-device-in-direct3d-11)
-   [裝置內容](#device-context)
    -   [立即內容](#immediate-context)
    -   [延後內容](#deferred-context)
-   [執行緒考量](#threading-considerations)
-   [相關主題](#related-topics)

## <a name="device"></a>裝置

裝置可用來建立資源和列舉顯示介面卡的功能。 在 Direct3D 11 中，裝置會以 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 介面表示。

每個應用程式必須至少有一個裝置，大部分的應用程式只能建立一個裝置。 藉由呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) ，為安裝在電腦上的其中一個硬體驅動程式建立裝置，並指定具有 [**D3D \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) 旗標的驅動程式類型。 每個裝置可以使用一或多個裝置內容，視所需的功能而定。

## <a name="device-context"></a>裝置內容

裝置內容包含使用裝置的情況或設定。 更具體來說，裝置內容會用來設定管線狀態，並使用裝置所擁有的資源來產生轉譯命令。 Direct3D 11 會執行兩種類型的裝置內容，一個用於立即轉譯，另一個用於延遲轉譯;這兩個內容都以 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 介面表示。

### <a name="immediate-context"></a>立即內容

立即內容直接呈現到驅動程式。 每個裝置都只有一個可從 GPU 取出資料的立即內容。 立即內容可以用來立即轉譯 (，或) [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)中播放。

有兩種方式可以取得立即內容：

-   藉由呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)。
-   藉由呼叫 [**ID3D11Device：： GetImmediateCoNtext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext)。

### <a name="deferred-context"></a>延後內容

延後的內容會將 GPU 命令記錄到 [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)中。 延遲的內容主要用於多執行緒，而且對單一執行緒應用程式而言並不是必要的。 延遲的內容通常會由工作者執行緒（而非主要轉譯執行緒）使用。 當您建立延遲的內容時，它不會繼承來自立即內容的任何狀態。

若要取得延遲的內容，請呼叫 [**ID3D11Device：： CreateDeferredCoNtext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext)。

任何內容--immediate 或延後--可以在任何執行緒上使用，只要一次只在一個執行緒中使用內容即可。

## <a name="threading-considerations"></a>執行緒考量

下表強調 Direct3D 11 中的執行緒模型與舊版 Direct3D 之間的差異。



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Direct3D 11 與舊版 Direct3D 之間的差異：<br/> 所有 <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> 介面方法都是無限制執行緒，這表示可以安全地讓多個執行緒同時呼叫函數。<br/>
<ul>
<li>所有 <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>衍生介面 (<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>、 <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>等 ) 都是無限制執行緒。</li>
<li>Direct3D 11 會將建立和轉譯的資源分割成兩個介面。 Map、取消對應、Begin、End 和 >id3d11devicecoNtext 會在<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong></strong></a>上執行，因為<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>會強定義作業的順序。 <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> 和 <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> 介面也會針對自由執行緒作業執行方法。</li>
<li>除了存在於<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) 上的<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>>id3d11devicecoNtext</strong></a>方法 (不是無限制執行緒，也就是需要單一執行緒。 每次只有一個執行緒可以安全地呼叫其任何方法 (繪製、複製、對應等 ) 。</li>
<li>一般情況下，無限制執行緒會將使用的同步處理原始物件數目以及其持續時間降到最低。 不過，使用長期同步處理的應用程式可能會直接影響應用程式可預期達到的並行程度。</li>
</ul>
ID3D10Device 介面方法並非設計成可自由執行緒。 ID3D10Device 會 (與 Direct3D 9) 中的 ID3D9Device 一樣來實行所有建立和轉譯功能。 對應和取消對應會在衍生於 ID3D10Asynchronous 衍生介面的 ID3D10Resource 衍生介面、Begin、End 和上執行。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





