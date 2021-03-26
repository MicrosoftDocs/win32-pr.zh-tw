---
title: 圖層介面
description: 本節包含圖層介面的相關資訊。
ms.assetid: 100cb66a-9bf5-4d0b-9f03-ad7c00e76d9d
keywords:
- 介面，Direct3D 11 圖層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57945866e8dea1b04c4066362105c8ac6e259a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104991042"
---
# <a name="layer-interfaces"></a><span data-ttu-id="eeab7-104">圖層介面</span><span class="sxs-lookup"><span data-stu-id="eeab7-104">Layer Interfaces</span></span>

<span data-ttu-id="eeab7-105">本節包含圖層介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eeab7-105">This section contains information about the layer interfaces.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="eeab7-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="eeab7-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eeab7-107">主題</span><span class="sxs-lookup"><span data-stu-id="eeab7-107">Topic</span></span></th>
<th><span data-ttu-id="eeab7-108">描述</span><span class="sxs-lookup"><span data-stu-id="eeab7-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eeab7-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeab7-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span></span><br/></td>
<td><span data-ttu-id="eeab7-110">Debug 介面可控制偵錯工具的設定、驗證管線狀態，而且只有在開啟 debug 層時才能使用。</span><span class="sxs-lookup"><span data-stu-id="eeab7-110">A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeab7-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeab7-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span></span><br/></td>
<td><span data-ttu-id="eeab7-112">資訊佇列介面會儲存、抓取及篩選 debug 訊息。</span><span class="sxs-lookup"><span data-stu-id="eeab7-112">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="eeab7-113">佇列包含訊息佇列、選擇性的儲存體篩選堆疊，以及選擇性的抓取篩選堆疊。</span><span class="sxs-lookup"><span data-stu-id="eeab7-113">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eeab7-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeab7-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="eeab7-115">預設追蹤介面集會設定參考預設追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="eeab7-115">The default tracking interface sets reference default tracking options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeab7-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeab7-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="eeab7-117">追蹤介面會設定參考追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="eeab7-117">The tracking interface sets reference tracking options.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eeab7-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeab7-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="eeab7-119">Direct3D 11 中不支援 <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> 介面和其方法。</span><span class="sxs-lookup"><span data-stu-id="eeab7-119">The <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> interface and its methods are not supported in Direct3D 11.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eeab7-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span><span class="sxs-lookup"><span data-stu-id="eeab7-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span></span><br/></td>
<td><span data-ttu-id="eeab7-121">追蹤裝置介面會設定著色器追蹤資訊，以便正確記錄和播放著色器的執行。</span><span class="sxs-lookup"><span data-stu-id="eeab7-121">The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="eeab7-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="eeab7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeab7-123">圖層參考</span><span class="sxs-lookup"><span data-stu-id="eeab7-123">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





