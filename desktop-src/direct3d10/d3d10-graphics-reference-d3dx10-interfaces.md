---
description: 本章節包含 Direct3D 10 圖形中 D3DX 公用程式程式庫所提供之元件物件模型 (COM) 介面的參考資訊。
ms.assetid: c57d9c39-3f30-4205-9b0a-665fe53f2b14
title: " (Direct3D 10 圖形) 的 D3DX 介面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65edec72206540d1f0c8e91e8a375daf3844f3703d2f05a3b844697230b300e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304220"
---
# <a name="d3dx-interfaces-direct3d-10-graphics"></a> (Direct3D 10 圖形) 的 D3DX 介面

本章節包含 D3DX 公用程式程式庫所提供之元件物件模型 (COM) 介面的參考資訊。 下列介面適用于 D3DX 公用程式程式庫。



| 介面                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX10DataLoader 介面**](id3dx10dataloader.md)       | [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)用來以非同步方式載入資料的資料載入物件。<br/>                                                                                                                                                                                                                                                                                                   |
| [**ID3DX10DataProcessor 介面**](id3dx10dataprocessor.md) | [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)使用的資料處理物件，以非同步方式處理載入的資料。<br/>                                                                                                                                                                                                                                                                                      |
| [**ID3DX10Font 介面**](id3dx10font.md)                   | ID3DX10Font 介面會封裝在特定裝置上呈現特定字型所需的材質和資源。<br/>                                                                                                                                                                                                                                                                                                |
| [**ID3DX10Mesh 介面**](id3dx10mesh.md)                   | 應用程式會使用 ID3DX10Mesh 介面的方法來操作網格物件。<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**ID3DX10MeshBuffer 介面**](id3dx10meshbuffer.md)       |                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ID3DX10SkinInfo 介面**](id3dx10skininfo.md)           | ID3DX10SkinInfo 可讓您優化、處理及手動設定網格中的骨骼與頂點之間的關聯性 (請參閱 [維琪百科) 上的框架動畫](https://en.wikipedia.org/wiki/Skeletal_animation) 。 它最適合用來製作 DCC Apps 所匯出的. x 檔案 (例如 3DS Max 和 Maya) 更容易使用硬體，以及改善 skinned 網格在軟體轉譯模式中的呈現速度。<br/> |
| [**ID3DX10Sprite 介面**](id3dx10sprite.md)               | ID3DX10Sprite 介面提供一組方法，可使用 Microsoft Direct3D 簡化繪製 sprite 的程式。<br/>                                                                                                                                                                                                                                                                                            |
| [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)       | 用來以非同步方式執行工作。 此物件佔用大量資源，因此通常每個應用程式只能建立一個資源。<br/>                                                                                                                                                                                                                                                                  |
| [**ID3DXMatrixStack 介面**](d3d10-id3dxmatrixstack.md)   | 應用程式會使用 ID3DXMATRIXStack 介面的方法來操作矩陣堆疊。<br/>                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3DX 參考](d3d10-graphics-reference-d3dx10.md)
</dt> </dl>

 

 




