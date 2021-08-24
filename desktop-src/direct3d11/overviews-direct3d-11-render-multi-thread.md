---
title: 多執行緒
description: Direct3D 11 支援使用多個執行緒來建立和轉譯物件。
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 718d80d9b70db0d6102d746168f338ddd8099339cee349724d87036714b16580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124323"
---
# <a name="multithreading"></a>多執行緒

Direct3D 11 支援使用多個執行緒來建立和轉譯物件。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                   | 描述                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Direct3D 11 中的多執行緒簡介](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | 多執行緒的設計目的是要使用一或多個執行緒同時執行工作，以改善效能。 <br/>                                                                                                         |
| [使用多執行緒建立物件](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | 您可以使用 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 介面來建立資源和物件，並使用 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 來 [呈現](overviews-direct3d-11-render-multi-thread-render.md)。<br/> |
| [立即和延後轉譯](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | Direct3D 11 支援兩種轉譯類型：立即和延後。 兩者都是使用 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 介面來執行。<br/>                                                      |
| [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | 命令清單是可錄製和播放的 GPU 命令序列。 命令清單可以藉由減少執行時間所產生的額外負荷，來改善效能。<br/>                                    |
| [Direct3D 版本之間的執行緒差異](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | 許多多執行緒程式設計模型會使用同步處理原始物件 (例如 mutex) 來建立重要區段，並防止一次有多個執行緒存取程式碼。<br/>                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何：檢查驅動程式支援](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[轉譯](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





