---
description: 本節包含有關 DXGI 所提供之函式的資訊。
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: DXGI 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06cb98c47ec3e2cb841aa5c27017ee6bb614f9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509880"
---
# <a name="dxgi-functions"></a>DXGI 函數

本節包含有關 DXGI 所提供之函式的資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                   | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | 建立可用來產生其他 DXGI 物件的 DXGI 1.0 factory。<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | 建立可用來產生其他 DXGI 物件的 DXGI 1.1 factory。<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | 建立可用來產生其他 DXGI 物件的 DXGI 1.3 factory。<br/> 在 Windows 8 中，系統上 DXGIDebug.dll 所建立的任何 DXGI factory 都會載入並使用它。 從 Windows 8.1 開始，應用程式會明確要求改為載入 DXGIDebug.dll。 使用 [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) 並指定 DXGI \_ 建立 \_ FACTORY 的 \_ 偵錯工具旗標來要求 DXGIDebug.dll; 如果系統上有 DLL，則會載入 DLL。<br/> |
| [**DXGIDeclareAdapterRemovalSupport**](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | 可讓進程指出它是否能夠復原任何正在移除的圖形裝置。<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | 抓取調試介面。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DXGIGetDebugInterface1**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | 抓取 Windows Store 應用程式用來對 Microsoft DirectX Graphic Infrastructure (DXGI) 進行偵錯工具的介面。<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DXGI 參考](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




