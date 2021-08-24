---
description: 您可以在這裡找到 Direct3D 10 中可用的功能清單。 此頁面列出 Direct3D 10 中已不再支援的 Direct3D 9 功能。
ms.assetid: ad3eff8e-a225-47c0-a53f-b1a3c94bcaac
title: " (Direct3D 10) 的已淘汰功能"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ce1750e6d8f98785bf87fb92169e56f0b4ca4e8a6dfdd34c6174a8c3087eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852768"
---
# <a name="deprecated-features-direct3d-10"></a> (Direct3D 10) 的已淘汰功能

您可以在 [這裡](d3d10-graphics-programming-guide-api-features.md)找到 Direct3D 10 中可用的功能清單。 此頁面列出 Direct3D 10 中已不再支援的 Direct3D 9 功能。

Direct3D 10 中最大的功能變更包括：

- Direct3D 10 不再支援固定函式轉換和光源管線。
- Direct3D 10 不再支援固定函式材質 blender (有時也稱為固定函式圖元著色器) 。
- Direct3D 10 會實作為新的點陣化規則，這些規則比 Direct3D 9 中執行的舊版 GDI 規則更簡單且更簡潔。 例如，不再支援線條的最後圖元控制項。

以下是 direct3d 10 中已被取代的 Direct3D 9 功能完整清單。

- **Alpha blend**。 Alpha blend 現在與彩色 blend 的程式設計無關。 Direct3D 10 會新增預設啟用的 Alpha blend 啟用切換。 如需詳細資訊，請參閱 [ (Direct3D 10) 的狀態物件 ](d3d10-graphics-programming-guide-api-features-state-objects.md) 。
- **Alpha 測試**。 Alpha 測試是 Direct3D 9 的固定功能圖元行為。 適用于 Direct3D 10 和更新版本的 Alpha 測試會移至可程式化的圖元著色器。 如需有關在 Direct3D 10 和更高版本中模擬 Direct3D 9 Alpha 測試功能的詳細資訊，請參閱 [2010 年6月的 DIRECTX SDK](https://www.microsoft.com/download/en/details.aspx?id=6812)中的 FixedFuncEMU 範例。
- **Blend 模式選項**。 BOTHSRCALPHA 已從 D3D10 BLEND 中移除 \_ ，因為它在 BOTHINVSRCALPHA 中是多餘的。 如需詳細資訊，請參閱 [**D3D10 \_ BLEND**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend) 。
- **封鎖壓縮格式**。 在 Direct3D 10 中，預乘的 Alpha 或非預乘 Alpha 沒有任何差異。 這些 Direct3D 9 格式對應至下列 Direct3D 10 格式： 

    | Direct3D 9 | Direct3D 10 |
    |------------|-------------|
    | DXT1       | BC1\*       |
    | DXT2,DXT3  | BC2\*       |
    | DXT4、DXT5  | BC3\*       |

    

     

    如需其他資訊，請參閱 [區塊壓縮 (Direct3D 10) ](d3d10-graphics-programming-guide-resources-block-compression.md) 。

-   **剪輯平面**。 Direct3D 10 不會使用剪輯平面來實行剪輯距離和挑選距離，最多可有8個元件，每個元件最多可包含2個頂點屬性元素。 如需其他資訊，請參閱 [ (DIRECTX HLSL) 的語法 ](../direct3dhlsl/dx-graphics-hlsl-semantics.md) 。 [FixedFuncEMU 範例](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) 提供在 Direct3D 10 中模擬剪輯平面的範例。
-   **遞色**。 Direct3D 10 不支援將遞色資料寫入轉譯目標。
-   **固定函式轉換和燈光管線無法使用**。 相反地，您必須使用著色器。 如需其他資訊，請參閱 [ (Direct3D 10) 著色器階段 ](/previous-versions//bb205146(v=vs.85)) 。
-   **固定函式材質 blender (也稱為固定函式圖元著色器)**。 相反地，您必須使用著色器。 如需其他資訊，請參閱 [ (Direct3D 10) 著色器階段 ](/previous-versions//bb205146(v=vs.85)) 。
-   **填滿模式** 已變更。 Direct3D 10 會實作為純色和框線填滿模式。 已移除 D3DFILLMODE 點，如有必要，請使用幾何著色器來模擬點模式。 [FixedFuncEMU 範例](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) 提供在 Direct3D 10 中模擬 D3DFILLMODE 點的範例。 如需其他資訊，請參閱 [ (Direct3D 10)](/previous-versions//bb205146(v=vs.85))的 [**D3D10 \_ 填滿 \_ 模式**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode)和著色器階段。
-   **格式**。 硬體可以使用 API 所公開的格式。 不會再實行亮度格式。
-   **Mipmap 篩選**。 已移除選取 [無篩選模式] 的選項。 相反地，只使用單一 mipmap 的材質，或將 MaxLOD 取樣器狀態設定為0。 如需其他資訊，請參閱 [ (Direct3D 10) 的狀態物件 ](d3d10-graphics-programming-guide-api-features-state-objects.md) 。
-   **調色板**。 應用程式應該改為使用讀取的相依材質。
-   **圖元和頂點著色器模型**： 1 \_ x、2 \_ x 和 3 \_ 0。 Direct3D 10 支援著色器模型4。 如需其他資訊，請參閱 [著色器模型 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md) 。
-   **點 sprite**。 請改用幾何著色器。 如需其他資訊，請參閱 [ (Direct3D 10) 著色器階段 ](/previous-versions//bb205146(v=vs.85)) 。
-   **柵格化規則**。 舊版 GDI 行的點陣化規則會以更簡潔、更簡單的規則取代。 不再支援線條的最後圖元控制項。 如需其他資訊，請參閱 [ (Direct3D 10) 的點陣化規則 ](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-rules.md) 。
-   **陰影模式**。 已移除支援 gouraud/phong 陰影) 的 D3DSHADEMODE (。 Direct3D 10 會改為針對頂點著色器輸出來執行兩個插補修飾詞。 如需在 Direct3D 10 中模擬 Direct3D 9 gouraud 和平面陰影模式的範例，請參閱 [FixedFuncEMU 範例](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) 。
-   **texldp** 指令。 應用程式必須使用額外的 HLSL 語句來執行投射的材質負載。 如需其他資訊，請參閱 [HLSL 的參考](../direct3dhlsl/dx-graphics-hlsl-reference.md) 。 [FixedFuncEMU 範例](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) 提供在 Direct3D 10 中模擬 texldp 的範例。
-   已不再支援 **材質座標-index** (TCI) 材質階段狀態 (D3DTSS \_ TEXCOORDINDEX) 。
-   **三角形風扇**。 應用程式必須將現有的三角形（電扇）轉換成三角形清單或三角形的條紋。 若要使用舊版 Api 中的 DrawPrimitive 來模擬某些行為，請嘗試在 Direct3D 10 中使用 DrawIndexed。 如需其他資訊，請參閱 [ (Direct3D 10) 的基本拓撲 ](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) 。
-   **W 緩衝** 處理。 不保證硬體支援;建議應用程式改為使用高精確度的深度緩衝區。 如需其他資訊，請參閱 [ (Direct3D 10) 設定 Depth-Stencil 功能 ](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md) 。
-    (材質座標換行) **換行模式**。  (的材質位址換行，例如 wrap、鏡像、夾具等 ) 仍然存在。 請參閱 [**D3D10 \_ 取樣器 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) 和 [**D3D10 \_ 材質 \_ 位址 \_ 模式**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texture_address_mode)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的 API 功能 ](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
