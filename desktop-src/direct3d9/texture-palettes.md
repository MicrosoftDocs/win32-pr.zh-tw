---
description: Direct3D 9 透過一組與 IDirect3DDevice9 物件相關聯的256專案調色板來支援調色板紋理。
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: " (Direct3D 9) 的材質調色板"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d755abb638ab1dd94e25edd98b2daef5e65d5a54cca7baf21a74e7d06173eed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291163"
---
# <a name="texture-palettes-direct3d-9"></a> (Direct3D 9) 的材質調色板

Direct3D 9 透過一組與 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 物件相關聯的256專案調色板來支援調色板紋理。 藉由呼叫 [**IDirect3DDevice9：： SetCurrentTexturePalette**](/windows/desktop/api) 方法，將元件設為最新。 目前的調色板用於轉譯所有使用中材質階段的所有調色板紋理。 [**IDirect3DDevice9：： SetPaletteEntries**](/windows/desktop/api) 會更新所有調色板的256專案。 每個專案都是 D3DFMT A8R8G8B8 格式的 [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) 結構 \_ 。 所有專案都會預設為0xFFFFFFFF。

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)調色板包含 Alpha 色板。 設定 D3DPTEXTURECAPS ALPHAPALETTE 裝置功能旗標時，可以使用此 Alpha 通道 \_ ，表示裝置支援來自調色板的 Alpha。 當材質格式沒有 Alpha 色板時，會使用調色板 Alpha 通道。 如果裝置不支援來自調色板的 Alpha，且材質格式沒有 Alpha 色板，則會將0xFF 的值用於 Alpha。

最多可以有 65536 (0x0000FFFF) 調色板。 由於與應用程式所參考的最大調色板數目成正比，因此與一組調色板相關聯的記憶體資源會使用從零開始的連續調色板編號。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本紋理概念](basic-texturing-concepts.md)
</dt> </dl>

 

 
