---
description: 材質引數常數會當做 D3DTEXTURESTAGESTATETYPE 列舉型別之下列成員的值使用：
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe6dd62ce7fc7fe4d438290af1ddb33a75813f0
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343013"
---
# <a name="d3dta"></a>D3DTA

材質引數常數會當做 [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) 列舉型別之下列成員的值使用：

-   D3DTSS \_ ALPHAARG0
-   D3DTSS \_ ALPHAARG1
-   D3DTSS \_ ALPHAARG2
-   D3DTSS \_ COLORARG0
-   D3DTSS \_ COLORARG1
-   D3DTSS \_ COLORARG2
-   D3DTSS \_ RESULTARG

藉由呼叫 [**SetTextureStageState**](/windows/desktop/api) 和 [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) 方法來設定和取出材質引數。

引數旗標

您可以結合引數旗標與修飾詞，但無法結合兩個引數旗標。



| \#定義          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DTA \_ 常數   | 從材質階段選取一個常數。 預設值為0xffffffff。                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| D3DTA \_ 目前    | 材質引數是上一個混合階段的結果。 在第一個材質階段 (階段 0) ，此引數相當於 D3DTA \_ 擴散。 如果上一個混合階段使用 (的 D3DTOP \_) BUMPENVMAP 作業，則系統會在距離地圖材質之前選擇階段中的材質。 如果 s 代表目前的材質階段，而 s-1 包含凹凸地圖材質，則這個引數會成為紋理階段 s-2 的結果輸出。 許可權為讀取/寫入。 |
| D3DTA \_ 擴散    | 材質引數是在 Gouraud 網底期間，從頂點元件插入的擴散色彩。 如果頂點未包含擴散色彩，預設色彩為0xffffffff。 許可權是唯讀的。                                                                                                                                                                                                                                                                                          |
| D3DTA \_ SELECTMASK | 所有引數的遮罩值;設定材質引數時未使用。                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| D3DTA \_ 反光   | 材質引數是在 Gouraud 網底期間，從頂點元件插入的反射色彩。 如果頂點未包含反射色彩，預設色彩為0xffffffff。 許可權是唯讀的。                                                                                                                                                                                                                                                                                        |
| D3DTA \_ TEMP       | 材質引數是用來讀取或寫入的臨時暫存器色彩。 \_如果有[D3DPMISCCAPS \_ TSSARGTEMP](d3dpmisccaps.md)裝置功能，則支援 D3DTA TEMP。 註冊的預設值是 (0.0、0.0、0.0、0.0) 。 許可權為讀取/寫入。                                                                                                                                                                                                                                   |
| D3DTA \_ 材質    | 材質引數是此材質階段的材質色彩。 許可權是唯讀的。                                                                                                                                                                                                                                                                                                                                                                                                               |
| D3DTA \_ TFACTOR    | 材質引數是在上一次呼叫 [**graphicsdevice**](/windows/desktop/api) 時設定的材質因數，並具有 [**D3DRS \_ TEXTUREFACTOR**](./d3drenderstatetype.md) 轉譯狀態值。 許可權是唯讀的。                                                                                                                                                                                                                                                       |



 

修飾詞旗標

引數旗標可以與下列其中一個修飾詞旗標合併。



| \#定義              | Description                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| D3DTA \_ ALPHAREPLICATE | 在作業完成之前，將 Alpha 資訊複寫至所有色彩通道。 這是讀取修飾詞。 |
| D3DTA \_ 補數     | 取得引數 x 的補數， (1.0-x) 。 這是讀取修飾詞。                                     |



 

## <a name="constant-information"></a>常數資訊



|   需求                       |  值           |
|--------------------------|-------------|
| 標頭                   | d3d9types。h |
| 最低作業系統 | Windows 98  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
