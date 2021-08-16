---
description: 應用程式會將混合階段與目前材質集中的每個材質產生關聯。 Direct3D 會依序評估每個混合階段，從集合中的第一個材質開始，然後以第八個材質為結尾。
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: " (Direct3D 9) 的材質混合作業和引數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d242092de5919267d30a9b8ff4e7bd2324f0bc3120649d3bb1a423b3462be77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797770"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a> (Direct3D 9) 的材質混合作業和引數

應用程式會將混合階段與目前材質集中的每個材質產生關聯。 Direct3D 會依序評估每個混合階段，從集合中的第一個材質開始，然後以第八個材質為結尾。

Direct3D 會將目前材質集中每個材質的資訊套用至與其相關聯的混合階段。 應用程式會藉由呼叫 [**IDirect3DDevice9：： SetTextureStageState**](/windows/desktop/api)，來控制來自材質階段的資訊。 您可以針對色彩和 Alpha 通道設定個別的作業，每個作業都使用兩個引數。 使用 D3DTSS COLOROP 階段狀態指定色彩通道作業 \_ ; 使用 D3DTSS ALPHAOP 指定 Alpha 作業 \_ 。 這兩個階段狀態會使用 [**D3DTEXTUREOP**](./d3dtextureop.md) 列舉型別中的值。

紋理混合引數使用 D3DTSS \_ COLORARG1、D3DTSS \_ COLORARG2、D3DTSS \_ ALPHARG1 和 D3DTSS \_ 列舉型別的 ALPHARG2 [](./d3dtexturestagestatetype.md) D3DTEXTURESTAGESTATETYPE 成員。 您可以使用 [D3DTA](d3dta.md)來識別對應的引數值。

> [!Note]  
> 您可以將該階段的色彩作業設定為 [D3DTOP 停用]，以停用材質階段以及任何後續的材質混合階段 \_ 。 停用色彩作業也會有效地停用 Alpha 運算。 啟用色彩作業時，無法停用 Alpha 作業。 當色彩混合啟用時，將 Alpha 作業設定為 D3DTOP \_ 停用會導致未定義的行為。

 

若要判斷裝置支援的材質混合作業，請查詢 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 TextureCaps 成員。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質混色](texture-blending.md)
</dt> </dl>

 

 
