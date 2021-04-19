---
title: Direct2D 結構
description: Direct2D 提供下列結構。 其他結構則是在 D2D1 命名空間中定義。
ms.assetid: 6c34a8c8-4b0b-4a95-8f13-25ca25c370ba
keywords:
- Direct2D，結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba4b668e143b3ab5b166582e504c68a05722da7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969706"
---
# <a name="direct2d-structures"></a>Direct2D 結構

Direct2D 提供下列結構。 其他結構則是在 [D2D1 命名空間](d2d1-namespace.md)中定義。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**D2D \_ 色 \_ F**](d2d-color-f.md) | 描述色彩的紅色、綠色、藍色和 Alpha 元件。 |
| [**D2D \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) | 表示 3 x 2 矩陣。 |
| [**D2D \_ 矩陣 \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f) | 描述 4 x 3 浮點數矩陣。 |
| [**D2D \_ 矩陣 \_ 4x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f) | 描述四個浮點數矩陣。 |
| [**D2D \_ 矩陣 \_ 5X4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f) | 描述五個浮點數矩陣。 |
| [**D2D \_ 點 \_ 2f**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f) | 表示在二維空間中以浮點數表示的 x 座標和 y 座標組（以浮點值表示）。 |
| [**D2D \_ 點 \_ 2L**](/previous-versions/windows/desktop/legacy/jj219217(v=vs.85)) | D2D \_ point \_ 2L 結構定義了某個點的 x 和 y 座標。 |
| [**D2D \_ 點 \_ 2u**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u) | 代表在二維空間中以不帶正負號32位整數值表示的 x 座標和 y 座標組。 |
| [**D2D \_ RECT \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) | 代表由左上角座標所定義的矩形， (左、上) 和右下角的座標 (右邊、下) 。  |
| [**D2D \_ RECT \_ L**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) | [**D2D \_ RECT \_ L**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85))結構會定義矩形左上角和右下角的座標。 |
| [**D2D \_ RECT \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_u) | 表示由左上角座標所定義的矩形， (左、上) 和右下角的座標， (右、下) 。 這些座標會以32位的整數值表示。 |
| [**D2D \_ 大小 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f) | 儲存一組已排序的浮點值，通常是矩形的寬度和高度。  |
| [**D2D \_ 大小 \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u) | 儲存已排序的整數配對，通常是矩形的寬度和高度。 |
| [**D2D \_ 向量 \_ 2f**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f) | 由兩個單精確度浮點值所組成的2D 向量 (x，y) 。  |
| [**D2D \_ 向量 \_ 3F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f) | 包含三個單精確度浮點數 (x、y、z) 的3D 向量。 |
| [**D2D \_ 向量 \_ 4F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f) | 由四個單精確度浮點數組成的4D 向量 (x、y、z、w) 。 |
| [**D2D1 \_ 弧形 \_ 區段**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_arc_segment) | 描述兩個點之間的橢圓形弧線。 |
| [**D2D1 \_ 貝塞爾 \_ 區段**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) | 表示在兩個點之間繪製的三次方貝塞爾區段。 |
| [**D2D1 \_ 點陣圖 \_ 筆刷 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) | 描述擴充模式和 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)的插補模式。 |
| [**D2D1 \_ 點陣圖 \_ 筆刷 \_ PROPERTIES1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_brush_properties1) | 描述擴充模式和 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)的插補模式。 |
| [**D2D1 \_ 點陣圖 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) | 描述點陣圖的像素格式和 DPI。 |
| [**D2D1 \_ 點陣圖 \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) | 此結構可讓您使用點陣圖選項和可用的色彩內容資訊來建立 [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1) 。  |
| [**D2D1 \_ BLEND \_ 描述**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) | 定義要在特定 blend 轉換中使用的 blend 描述。 |
| [**D2D1 \_ 筆刷 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties) | 描述筆刷的不透明度和轉換。 |
| [**D2D1 \_ 色彩 \_ F**](d2d1-color-f.md) | 描述色彩的紅色、綠色、藍色和 Alpha 元件。 |
| [**D2D1 \_ 建立 \_ 屬性**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_creation_properties) | 指定用來建立 [Direct2D](./direct2d-portal.md) 裝置、factory 和裝置內容的選項。  |
| [**D2D1 \_ 自訂 \_ 頂點 \_ 緩衝區 \_ 屬性**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_custom_vertex_buffer_properties) | 定義頂點著色器和輸入元素描述，以定義輸入配置。 |
| [**D2D1 \_ 繪圖 \_ 狀態 \_ 描述**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_drawing_state_description) | 描述呈現目標的繪圖狀態。  |
| [**D2D1 \_ 繪圖 \_ 狀態 \_ DESCRIPTION1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_drawing_state_description1) | 描述裝置內容的繪製狀態。 |
| [**D2D1 \_ 效果 \_ 輸入 \_ 描述**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_effect_input_description) | 描述效果的功能。 |
| [**D2D1 \_ 橢圓形**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) | 包含橢圓形的中心點、x 半徑和 y 半徑。 |
| [**D2D1 \_ FACTORY \_ 選項**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_factory_options) | 包含 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) 物件的調試層級。  |
| [**D2D1 \_ 功能 \_ 資料 \_ 雙精度浮點數**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_doubles) | 描述著色器中雙精度浮點數的支援。 |
| [**D2D1 \_ FEATURE \_ DATA \_ D3D10 \_ X \_ 硬體 \_ 選項**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_d3d10_x_hardware_options) | 描述計算著色器支援，這是 D3D10 功能層級的選項。 |
| [**D2D1 \_ 梯度 \_ 網格 \_ PATCH**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch) | 代表具有16個控制點、4個邊角色彩和界限旗標的 tensor 修補程式。 ID2D1GradientMesh 由1個或多個漸層網格修補程式組成。 使用 GradientMeshPatch 函式或 [**GradientMeshPatchFromCoonsPatch**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatchfromcoonspatch)函式來建立一個 [**函數**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatch)。  |
| [**D2D1 \_ 梯度 \_ 停駐點**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) | 包含漸層停駐點的位置和色彩。  |
| [**D2D1 \_ HWND \_ 轉譯 \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) | 包含 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)的 HWND、圖元大小和呈現選項。 |
| [**D2D1 \_ 筆墨 \_ 樣式 \_ 屬性**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_style_properties) | 定義 [**ID2D1InkStyle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle) 物件中所使用的一般畫筆提示圖形和轉換。  |
| [**D2D1 \_ 影像 \_ 筆刷 \_ 屬性**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_image_brush_properties) | 描述影像筆刷特徵。 |
| [**D2D1 \_ 筆墨 \_ 貝塞爾 \_ 區段**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment) | 表示用於建立 [**ID2D1Ink**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink) 物件的貝塞爾區段。 此結構與 [**D2D1 \_ 貝塞爾 \_ 線段**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) 不同之處在于，它是由 D2D1 的 [**\_ 筆墨 \_ 點**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point)s 所組成，其中包含半徑以及 x 和 y 座標。  |
| [**D2D1 \_ 筆墨 \_ 點**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point) | 代表組成 [**D2D1 \_ 筆跡 \_ 貝塞爾 \_ 線段**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment)一部分的點半徑組。 |
| [**D2D1 \_ 輸入 \_ 描述**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_description) | 描述在輸入材質上可能設定的轉換選項。 |
| [**D2D1 \_ 輸入 \_ 元素 \_ DESC**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_element_desc) | 頂點配置的單一元素描述。 |
| [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) | 包含圖層資源的內容界限、遮罩資訊、不透明度設定和其他選項。  |
| [**D2D1 \_ 圖層 \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) | 包含圖層資源的內容界限、遮罩資訊、不透明度設定和其他選項。 |
| [**D2D1 \_ 線性漸層 \_ \_ 筆刷 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) | 包含 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)之漸層軸的起始點和端點。  |
| [**D2D1 \_ 矩陣 \_ 3X2 \_ F**](d2d1-matrix-3x2-f.md) | 表示 3 x 2 矩陣。  |
| [**D2D1 \_ 矩陣 \_ 4X3 \_ F**](d2d1-matrix-4x3-f.md) | 代表 4 x 3 的矩陣。  |
| [**D2D1 \_ 矩陣 \_ 4x4 \_ F**](d2d1-matrix-4x4-f.md) | 代表4到4的矩陣。  |
| [**D2D1 \_ 矩陣 \_ 5X4 \_ F**](d2d1-matrix-5x4-f.md) | 表示5乘以4的矩陣。  |
| [**D2D1 \_ 對應的 \_ RECT**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_mapped_rect) | 描述 [**ID2D1Bitmap1：： Map**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-map) API 的對應記憶體。 |
| [**D2D1 \_ 圖元 \_ 格式**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) | 包含點陣圖或呈現目標的資料格式和 Alpha 模式。  |
| [**D2D1 \_ 點 \_ 2f**](d2d1-point-2f.md) | 表示在二維空間中的 x 座標和 y 座標組。 |
| [**D2D1 \_ 點 \_ 2L**](/previous-versions/windows/desktop/legacy/hh847948(v=vs.85)) | 點結構定義點的 x 和 y 座標。 |
| [**D2D1 \_ 點 \_ 2u**](d2d1-point-2u.md) | 表示在二維空間中的 x 座標和 y 座標組。  |
| [**D2D1 \_ 點 \_ 描述**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_point_description) | 描述路徑幾何上的點。 |
| [**D2D1 \_ 列印 \_ 控制項 \_ 屬性**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_print_control_properties) | [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)物件的建立屬性。 |
| [**D2D1 \_ 屬性系結 \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) | 定義屬性系結至一組函式，這些函數會取得並設定對應的屬性。  |
| [**D2D1 \_ 二次方 \_ 貝塞爾 \_ 區段**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_quadratic_bezier_segment) | 包含二次方貝塞爾線段的控制點和結束點。 |
| [**D2D1 \_ 放射狀漸層 \_ \_ 筆刷 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) | 包含漸層原點位移以及 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)之漸層橢圓的大小與位置。  |
| [**D2D1 \_ RECT \_ F**](d2d1-rect-f.md) | 代表由左上角座標所定義的矩形， (左、上) 和右下角的座標 (右邊、下) 。  |
| [**D2D1 \_ RECT \_ L**](/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)) | 矩形結構定義矩形左上角和右下角的座標。 |
| [**D2D1 \_ RECT \_ U**](d2d1-rect-u.md) | 代表由左上角座標所定義的矩形， (左、上) 和右下角的座標 (右邊、下) 。  |
| [**D2D1 \_ 資源 \_ 材質 \_ 屬性**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_resource_texture_properties) | 定義原始資源材質建立時的資源材質。 |
| [**D2D1 \_ 資源 \_ 使用量**](/previous-versions/windows/desktop/legacy/hh404326(v=vs.85)) | 描述影像紋理和著色器所使用的記憶體。 |
| [**D2D1 \_ 轉譯 \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) | 包含轉譯選項 (硬體或軟體) 、像素格式、DPI 資訊、遠端選項，以及轉譯目標的 Direct3D 支援需求。  |
| [**D2D1 \_ 轉譯 \_ 控制項**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_rendering_controls) | 描述要套用至影像效果轉譯器的限制。 |
| [**D2D1 \_ 圓角 \_ 矩形**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_rounded_rect) | 包含圓角矩形的尺寸和圓角半徑。 |
| [**D2D1 \_ 簡單 \_ 色彩 \_ 設定檔**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_simple_color_profile) | 色彩空間的簡單描述。 |
| [**D2D1 \_ 大小 \_ F**](d2d1-size-f.md) | 儲存一組排序的浮點數，通常是矩形的寬度和高度。 |
| [**D2D1 \_ 大小 \_ U**](d2d1-size-u.md) | 儲存已排序的整數配對，通常是矩形的寬度和高度。 |
| [**D2D1 \_ 筆觸 \_ 樣式 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_stroke_style_properties) | 描述勾勒出形狀的筆觸。  |
| [**D2D1 \_ 筆觸 \_ 樣式 \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_stroke_style_properties1) | 描述勾勒出形狀的筆觸。 |
| [**D2D1 \_ SVG \_ 長度**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_length) | 表示 SVG 長度。 |
| [**D2D1 \_ SVG \_ 保留 \_ 外觀 \_ 比例**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_preserve_aspect_ratio) | 代表所有 SVG preserveAspectRatio 設定。 |
| [**D2D1 \_ SVG \_ VIEWBOX**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_viewbox) | 表示 SVG viewBox。 |
| [**D2D1 \_ 轉換的 \_ 影像 \_ 來源 \_ 屬性**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_transformed_image_source_properties) | 已轉換之影像來源的屬性。 |
| [**D2D1 \_ 三角形**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_triangle) | 包含描述三角形的三個頂點。 |
| [**D2D1 \_ 向量 \_ 2f**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_2f) | 2浮點值的向量， (x，y) 。 |
| [**D2D1 \_ 向量 \_ 3F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_3f) | 三個 FLOAT 值的向量 (x、y、z) 。 |
| [**D2D1 \_ 向量 \_ 4F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_4f) | 4浮點值的向量， (x、y、z、w) 。 |
| [**D2D1 \_ 頂點 \_ 緩衝區 \_ 屬性**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_buffer_properties) | 定義所有頂點著色器定義的標準頂點緩衝區屬性。 |
| [**D2D1 \_ 頂點 \_ 範圍**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_range) | 定義在轉譯時，所使用的頂點範圍，小於頂點緩衝區的完整內容。 |
| [**D3DCOLORVALUE**](/previous-versions/windows/desktop/legacy/dd368193(v=vs.85)) | 儲存色彩和 Alpha 通道資訊。 |
| [*PD2D1 \_ 效果 \_ FACTORY*](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) | 描述效果的實作為效果。 |