---
description: 就概念而言，視口是投影出3D 場景的二維 (2D) 矩形。
ms.assetid: eddadaa1-9181-47fa-8530-44aa46fea286
title: " (Direct3D 9) 的區形和剪切"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6ed7cd5e5a8a3116c07c5b88f3e665e7ba7de7c6dd1d3cd7bf55f936e60386
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068840"
---
# <a name="viewports-and-clipping-direct3d-9"></a> (Direct3D 9) 的區形和剪切

就概念而言，視口是投影出3D 場景的二維 (2D) 矩形。 在 Direct3D 中，矩形在 Direct3D 表面中以座標的形式存在，系統會使用矩形作為轉譯目標。 投影轉換將頂點轉換至用於檢視區的座標系統。 檢視區也用於指定轉譯目標表面 (場景轉譯目標) 上深度值的範圍 (通常是 0.0 到 1.0)。

## <a name="the-viewing-frustum"></a>檢視範圍

檢視範圍是場景中相對於檢視區相機放置的 3D 體積。 體積形狀影響模型如何從相機空間投影到螢幕。 最常見的投射類型，透視投影，負責讓靠近相機的物件看起來比遠方物件更大。 針對透視檢視，檢視範圍可視為金字塔，相機位於塔頂，如下圖所示。 此金字塔與前端和背景裁剪平面相交。 金字塔內前端和背景裁剪平面之間的體積是檢視範圍。 唯有在這個體積中，物件才會顯示。

![前端和背景裁剪平面之間檢視範圍的圖例](images/frustum.png)

如果您想像站在暗房裡，並看出方窗外，就會視覺化檢視範圍。 在這個類比，近裁剪平面是窗戶，背景裁剪平面是最後中斷檢視的任何東西 - 對街的摩天大樓、遠方山脈，或空無一物。 您可以看到被截斷金字塔內的所有東西，從窗戶開始到中斷檢視的任何東西結束，而且您看不到其他任何東西。

檢視範圍是由 fov（視野），以及前端和背景裁剪平面之間的距離 (在 z 座標中指定) 所定義，如下圖顯示。

![檢視範圍圖](images/fovdiag.png)

在這個圖，變數 D 是從相機到空間原點 (此空間定義在幾何管線最後一部分 - 檢視轉換) 之間的距離。 圍繞這個空間，您排列檢視範圍的限制。 如需有關如何使用此 D 變數來建立投射矩陣的詳細資訊，請參閱 [ (Direct3D 9 的投射轉換) ](projection-transform.md)

## <a name="viewport-rectangle"></a>檢視區矩形

您可以使用 [**D3DVIEWPORT9**](d3dviewport9.md) 結構，在 c + + 中定義區的矩形。 D3DVIEWPORT9 結構會與 IDirect3DDevice9 介面所公開的下列視口操作方法搭配使用。

-   [**IDirect3DDevice9::GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
-   [**IDirect3DDevice9::SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)

D3DVIEWPORT9 結構包含四個成員（X、Y、寬度、高度），可定義要呈現場景的呈現目標介面區域。 這些值對應目的地矩形或檢視區矩形，如下圖顯示。

![檢視區矩形圖](images/destrect.png)

指定的 X、Y、寬度、高度成員值是相對於轉譯目標表面左上角的螢幕座標。 結構定義兩個額外成員（MinZ 和 MaxZ），表示場景轉譯到的深度範圍。

Direct3D 假設檢視區裁剪體積的範圍是從 -1.0 到 1.0 (在 X 中) 以及從 1.0 到 -1.0 (在 Y 中)。這些是應用程式過去最常使用的設定。 裁剪之前，您可以使用[投影轉換](projection-transform.md)調整檢視區的長寬比例。

> [!Note]  
> MinZ 和 MaxZ 指出將呈現場景的深度範圍，而不會用於剪切。 大部分的應用程式都會將這些成員設定為0.0 和1.0，讓系統能夠轉譯成深度緩衝區中的整個深度值範圍。 有時候，您可以使用其他深度範圍達成特殊效果。 例如，若要在遊戲中轉譯平視顯示器，您可以將這兩個值設定為 0.0，強迫在場景的前景中轉譯物件，或者您可以將這兩個值設定為 1.0，轉譯永遠應該會在背景中的物件。

 

在 [**D3DVIEWPORT9**](d3dviewport9.md) 結構的 X、Y、Width、Height 成員中使用的維度，會定義呈現目標介面上的位置和大社區。 這些值是在螢幕座標中，相對於表面左上角。

Direct3D 使用檢視區位置和維度來縮放頂點，讓轉譯的場景放在目標表面上的適當位置。 內部，Direct3D 會將這些值插入下列套用到每個頂點的矩陣中。

![套用到每個頂點之矩陣的方程式](images/vpscale.png)

這個矩陣依據檢視區維度和您想要的深度範圍縮放頂點，並將它們轉移到轉譯目標表面上的適當位置。 矩陣也翻轉 y 座標，隨著 y 向下漸增，以反映左上角的螢幕原點。 套用這個矩陣之後，頂點仍是同質的，也就是說，它們仍會以 \[ x、y、z、w 頂點的形式存在， \] 而且必須先轉換成非同質座標，才能傳送到轉譯器。

> [!Note]  
> 區域調整矩陣會併入 [**D3DVIEWPORT9**](d3dviewport9.md) 結構的 MinZ 和 MaxZ 成員，以縮放頂點以符合深度範圍 \[ MinZ、MaxZ \] 。 這代表舊版 DirectX 的不同語義，其中這些成員是用來剪切。

 

> [!Note]  
> 應用程式通常會分別將 MinZ 和 MaxZ 設定為0.0 和1.0，讓系統轉譯成整個深度範圍。 不過，您可以使用其他值達到特定效果。 例如，您可以將這兩個值設為 0.0，強制所有物件到前景，或都設為 1.0 將所有物件轉譯到背景。

 

## <a name="clearing-a-viewport"></a>清除檢視區

清除檢視區會重設轉譯目標表面上檢視區矩形的內容。 它也會清除深度和樣板緩衝區表面中的矩形。

使用 [**IDirect3DDevice9：： clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) 可清除此區。 方法會接受一個或多個矩形，以定義要清除之介面上的區域。 將 Count 參數設定為1，而將 pRects 參數設定為單一矩形的位址（涵蓋整個視窗區區域）將會清除整個視表單。 清除整個視口的另一種方式是將 pRects 參數設定為 **Null** ，並將 Count 參數設定為0。

[**IDirect3DDevice9：： Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)可以用來清除深度緩衝區內的樣板位。 只要設定 Flags 參數，即可決定 **IDirect3DDevice9：： Clear** 如何搭配轉譯目標和任何相關聯的深度或樣板緩衝區。 D3DCLEAR \_ 目標旗標將會使用您在 color 引數中提供的任意 RGBA 色彩來清除此區， (這不是材質色彩) 。 D3DCLEAR \_ ZBUFFER 旗標會將深度緩衝區清除為您在 Z：0.0 中指定的任意深度最接近的距離，而1.0 是最遠的。 D3DCLEAR 樣板 \_ 旗標會將樣板位重設為您在樣板引數中提供的值。 您可以使用範圍從0到 2n-1 的整數，其中 n 是樣板緩衝區位深度。

在某些情況下，您可能只會轉譯成轉譯目標和深度緩衝區表面的小部分。 Clear 方法也可讓您在單一呼叫中清除介面的多個區域。 若要這麼做，請將 Count 參數設定為您想要清除的矩形數目，並在 pRects 參數中指定矩形陣列中第一個矩形的位址。

## <a name="set-up-the-viewport-for-clipping"></a>設定裁剪的檢視區

投影矩陣的結果決定投影空間中的裁剪體積為：

-w<sub>c</sub><= x<sub>c</sub><= w<sub>c</sub>

-w<sub>c</sub><= y<sub>c</sub><= w<sub>c</sub>

0 <= z<sub>c</sub><= w<sub>c</sub>

其中：x、y 和 w 代表套用投影轉換後的頂點座標。 x、y 或 z 元件在這些範圍外的任何頂點都會被裁剪，如果裁剪已啟用（預設行為）。

除了頂點緩衝區例外之外，應用程式也會透過 [**D3DRS \_ 剪切**](./d3drenderstatetype.md) 轉譯狀態來啟用或停用裁剪。 在處理期間，會產生頂點緩衝區的剪輯資訊。 如需詳細資訊，請參閱 [ (direct3d 9 的固定函式頂點處理) ](fixed-function-vertex-processing.md) 和可程式化的 [頂點處理 (direct3d 9) ](programmable-vertex-processing.md)。

除非來自 [**IDirect3DDevice9：:P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices)，否則 Direct3D 不會從頂點緩衝區裁剪基本的已轉換頂點。 如果您要執行自己的轉換，而且需要 Direct3D 進行裁剪，則不應使用頂點緩衝區。 在此情況下，應用程式會將資料進行轉換。 Direct3D 會第二次流經資料來裁剪資料，然後驅動程式會轉譯資料，而這種情況沒有效率。 因此，如果應用程式轉換資料，也應該要裁剪資料。

當裝置接收到預先轉換和亮頂點 (T&需要裁剪的頂點) 時，為了執行裁剪作業，頂點會使用頂點的交互同質 w (RHW) 和資料格資訊，重新轉換成剪切空間。 然後會執行剪切。 並非所有裝置都能夠執行此反向轉換，以裁剪 T&L 頂點。

D3DPMISCCAPS \_ CLIPTLVERTS 裝置功能指出裝置是否能夠裁剪 T&L 頂點。 如果未設定這項功能，應用程式會負責將它要向下傳送至要轉譯之裝置的 T&L 頂點。 無論裝置是在軟體頂點處理模式中建立，還是切換至軟體頂點處理模式) ，裝置一律都能在軟體頂點處理模式中裁剪 T&L 頂點 (。

設定轉譯裝置之視口參數的唯一需求是設定視口的剪切量。 若要這樣做，您可以針對裁剪磁片區和轉譯目標介面，初始化並設定裁剪值。 您通常會將多個區域設定為轉譯為轉譯目標表面的完整區域，但這不是必要條件。

您可以針對 [**D3DVIEWPORT9**](d3dviewport9.md) 結構的成員使用下列設定，以在 c + + 中達成這個目的。


```
D3DVIEWPORT9 viewData = { 0, 0, width, height, 0.0f, 1.0f };
```



設定 [**D3DVIEWPORT9**](d3dviewport9.md) 結構中的值之後，請呼叫其 [**IDirect3DDevice9：： SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) 方法，將資料區參數套用至裝置。 下列程式碼範例會顯示這個呼叫的外觀。


```
HRESULT hr;

hr = pd3dDevice->SetViewport(&viewData);
if(FAILED(hr))
    return hr;
```



如果呼叫成功，則會設定視口參數，並且會在下次呼叫轉譯方法時生效。 若要變更視口參數，請只更新 [**D3DVIEWPORT9**](d3dviewport9.md) 結構中的值，然後再次呼叫 [**IDirect3DDevice9：： SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) 。

> [!Note]  
> [**D3DVIEWPORT9**](d3dviewport9.md)結構成員 MinZ 和 MaxZ 指出將呈現場景的深度範圍，而不會用於裁剪。 大部分的應用程式都會將這些成員設定為0.0 和1.0，讓系統能夠轉譯成深度緩衝區中的整個深度值範圍。 有時候，您可以使用其他深度範圍達成特殊效果。 例如，若要在遊戲中轉譯平視顯示器，您可以將這兩個值設定為 0.0，強迫在場景的前景中轉譯物件，或者您可以將這兩個值設定為 1.0，轉譯永遠應該會在背景中的物件。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速入門](getting-started.md)
</dt> </dl>

 

 
