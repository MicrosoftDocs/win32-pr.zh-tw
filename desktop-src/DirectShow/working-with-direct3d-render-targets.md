---
description: 使用 Direct3D 轉譯目標
ms.assetid: 271b919c-421b-4484-8e60-afbf3cbdca44
title: 使用 Direct3D 轉譯目標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7bacf36402b071d60989e225cdcd9533500494a0593bcf9753ddc06bb93ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650338"
---
# <a name="working-with-direct3d-render-targets"></a>使用 Direct3D 轉譯目標

許多適用于 Direct3D 轉譯目標的媒體子類型都定義為與 VMR-7 和 VMR-9 搭配使用。 當上游篩選準則向其中一個子類型提出連接時，會向 VMR 指出要在 Direct3D 轉譯目標上執行轉譯。 若為 VMR-7，這會是 DirectX 7 Direct3D 轉譯目標，而針對 VMR-9，這會是 DirectX 9 Direct3D 轉譯目標。 如果 VMR 處於混合模式，介面也會是 Direct3D 材質介面。 如果 VMR 不在混合模式中，則介面會是一般的 Direct3D 介面。 只有在 VMR 為混合模式時，才支援 ARGB 像素格式。 轉譯目標子類型為：



| VMR-7                                | VMR-9                                |
|--------------------------------------|--------------------------------------|
| MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX7 \_ RT   | MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX9 \_ RT   |
| MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX9 \_ RT |
| MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX9 \_ RT |



 

這些類型定義于標頭檔 uuid. h 中。 MEDIASUBTYPE \_ RGB32 媒體類型是 RGBx888 格式，而 MEDIASUBTYPE \_ RGB16 媒體類型是 RGB565 格式。 如需這些像素格式的詳細資訊，請參閱 DirectX 圖形檔。

**要求未鎖定的介面**

鎖定和解除鎖定 DirectDraw 介面是計算成本高昂的作業。 使用 Direct3D 轉譯目標媒體子類型時，上游篩選器需要將介面解除鎖定，才能在圖形硬體上操作。 為了避免不必要的鎖定解除鎖定作業，VMR 會在 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) 方法（AM GBF NODDSURFACELOCK）上支援新的旗標，該旗標會 \_ 指示 VMR 在將 \_ 範例傳遞給上游篩選之前，不鎖定 DirectDraw 介面。 使用這個旗標時， [**IMediaSample：： GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) 的呼叫將會失敗，因為沒有鎖定的指標。 若要取得 DirectDraw 介面的存取權，篩選準則必須在傳回的 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample)物件上呼叫 **QueryInterface** ，並要求 [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface)介面。 很明顯地，上游篩選器在將範例釋放回可用清單時，必須確保介面未鎖定。

 

 



