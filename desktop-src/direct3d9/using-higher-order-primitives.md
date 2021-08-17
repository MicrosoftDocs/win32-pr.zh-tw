---
description: 本節說明如何在您的應用程式中使用較高順序的基本專案。
ms.assetid: 7aa4f3ab-cfce-4f8f-a538-384f038fd324
title: '使用 Higher-Order 基本 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7d7a7b7f619c033665f8cb9894db5d60d5d6ecf9116de4ada230accc476c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797287"
---
# <a name="using-higher-order-primitives-direct3d-9"></a>使用 Higher-Order 基本 (Direct3D 9) 

本節說明如何在您的應用程式中使用較高順序的基本專案。

-   [判斷 Higher-Order 基本支援](#determining-higher-order-primitive-support)
-   [繪圖修補程式](#drawing-patches)
-   [產生法線和材質座標](#generating-normals-and-texture-coordinates)

## <a name="determining-higher-order-primitive-support"></a>判斷 Higher-Order 基本支援

您可以查詢 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 DevCaps 成員，以判斷涉及較高訂單基本專案之作業的支援層級。 下表列出 Direct3D 9 中與較高順序基本專案相關的裝置功能。



| 裝置功能             | 描述                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS \_ NPATCHES          | 裝置支援 N 個修補程式，並根據 [曲線的 PN 三角形](https://alex.vlachos.com/graphics/CurvedPNTriangles.pdf) (一種特殊的三次貝塞爾三角形) 。 |
| D3DDEVCAPS \_ QUINTICRTPATCHES  | 裝置支援 quintic 貝茲曲線和 B 曲線。                                                                                                         |
| D3DDEVCAPS \_ RTPATCHES         | 裝置支援 (RT-修補程式) 的矩形和三角形修補程式。                                                                                             |
| D3DDEVCAPS \_ RTPATCHHANDLEZERO | RT-修補程式可能會使用控制碼零來有效率地繪製。                                                                                                     |



 

請注意，D3DDEVCAPS \_ RTPATCHHANDLEZERO 並不表示可以繪製控制碼為零的修補程式。 不論是否已設定此裝置功能，都可以繪製控制碼零修補程式。 當設定這項功能時，硬體架構不需要快取任何資訊，且未快取的修補程式 (處理零) 會以快取的方式有效率地繪製。

## <a name="drawing-patches"></a>繪圖修補程式

Direct3D 9 支援兩種類型的高序位基本專案或修補程式。 這些稱為 N 修補程式和 Rect/三個修補程式。 N 修補程式可以使用任何三角形轉譯呼叫來呈現，方法是透過呼叫 [**IDirect3DDevice9：： SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) ( nSegments ) ，其 nSegments 值大於1.0。 Rect/三個修補程式必須使用下列明確的進入點來呈現。

您可以使用下列方法來繪製修補程式。

-   [**IDirect3DDevice9：:D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)。 若要進一步瞭解如何在頂點緩衝區中參考修補程式資料，請參閱 [**D3DRECTPATCH \_ 資訊**](d3drectpatch-info.md)。
-   [**IDirect3DDevice9：:D rawtripatch**](/windows/desktop/api)。 若要進一步瞭解如何在頂點緩衝區中參考修補程式資料，請參閱 [**D3DTRIPATCH \_ 資訊**](d3dtripatch-info.md)。

[**IDirect3DDevice9：:D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) 會使用目前設定的資料流程，繪製 pRectPatchInfo 參數所指定的矩形高序位修補程式。 控制碼參數是用來將修補程式關聯至控制碼，因此下次繪製修補程式時，不需要重新指定 pRectPatchInfo。 如此一來，就可以預先計算和快取向前差異係數或其他資訊，進而讓後續呼叫 IDirect3DDevice9：使用相同的控制碼有效率地執行 **：:D rawrectpatch** 。

它適用于靜態修補程式，應用程式會設定頂點著色器和適當的資料流程、在 pRectPatchInfo 參數中提供修補程式資訊，以及指定一個控制碼，讓 Direct3D 可以捕獲和快取資訊。 然後，應用程式可以呼叫 [**IDirect3DDevice9：:D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) 接著將 pRectPatchInfo 設定為 **Null** ，以有效率地繪製修補程式。 繪製快取的修補程式時，會忽略目前設定的資料流程。 不過，您可以藉由指定 pNumSegs 的新值來覆寫快取的 pNumSegs。 此外，在轉譯快取的修補程式時，也必須設定相同的頂點著色器（當它被捕捉時所設定）。

若為動態修補程式，修補程式資料會隨著修補程式的每個轉譯而變更，因此快取資訊的效率並不高。 應用程式可以將控制碼設定為0，以將此傳遞給 Direct3D。 在此情況下，Direct3D 會使用目前設定的資料流程和 pNumSegs 值來繪製修補程式，而不會快取任何資訊。 同時將控制碼設定為0，並將 pPatch 設定為 **Null**，是不正確。

藉由針對相同的控制碼 respecifying pRectPatchInfo，應用程式可以覆寫先前快取的資訊。

[**IDirect3DDevice9：:D rawtripatch**](/windows/desktop/api) 與 [**IDirect3DDevice9：:D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) 類似，不同之處在于它會繪製三角形的高序位修補程式。

## <a name="generating-normals-and-texture-coordinates"></a>產生法線和材質座標

如果您使用彈性頂點格式 (FVF) 著色器，就無法自動產生法線和材質座標。

針對法線，您可以直接提供它們，或讓 Direct3D 為您計算。

針對矩形修補程式產生的座標是以曲線為基礎的座標，如下列圖例所示。

![使用以曲線為基礎之座標的原始材質和材質圖例](images/texturespline.png)

為三角形修補程式產生的座標是以 barycentric 曲線為基礎的座標，如下圖所示。

![使用 barycentric 曲線座標的原始材質和材質圖例](images/texturebarycentricspline.png)

如果應用程式必須變更產生的材質座標範圍，則可以使用材質轉換來完成。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[較高順序的基本專案](higher-order-primitives.md)
</dt> </dl>

 

 
