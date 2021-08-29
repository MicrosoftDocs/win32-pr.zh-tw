---
title: DirectComposition 詞彙
description: 本主題定義 Microsoft DirectComposition 條款。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3B9932EA-3182-41D0-B64A-7699EC98A714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d6a6f39de62339bf5de0ea7b4976fa19f60c4bd2ff549a732acee43d546256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985428"
---
# <a name="directcomposition-glossary"></a>DirectComposition 詞彙

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 Windows 的撰寫 api，而不是 DirectComposition。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

本主題定義 Microsoft DirectComposition 條款。

<dl> <dt>

<span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**動畫函數**
</dt> <dd>

指定如何在一段時間內變更單一物件屬性值的結構。

</dd> <dt>

<span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**動畫物件**
</dt> <dd>

物件，表示用來建立另一個物件之屬性動畫的函式。

</dd> <dt>

<span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**動畫區段**
</dt> <dd>

動畫函數的基本計時定義;它們是建立更複雜和更高層級動畫函式的基本類型。

</dd> <dt>

<span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**背景緩衝區**
</dt> <dd>

應用程式可直接寫入的記憶體矩形。 背景緩衝區永遠不會直接顯示在監視器上。

</dd> <dt>

<span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**批**
</dt> <dd>

以原子方式處理的 DirectComposition 方法呼叫群組。

</dd> <dt>

<span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**點陣圖**
</dt> <dd>

位於系統或視訊記憶體中的色彩緩衝區（不論有無 Alpha 色板）。

</dd> <dt>

<span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**框線模式**
</dt> <dd>

Microsoft DirectComposition 視覺效果的屬性，此屬性會影響點陣圖轉換時，點陣圖邊緣的組成方式，讓邊緣不會與整數座標組齊軸。 它也會影響在具有圓角的剪輯角落以及已轉換之剪輯邊緣的內容裁剪方式，讓邊緣與整數座標不對齊軸。

</dd> <dt>

<span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**剪輯物件**
</dt> <dd>

表示剪輯矩形的物件。

</dd> <dt>

<span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**裁剪矩形**
</dt> <dd>

一組座標，定義轉譯點陣圖時在螢幕上繪製的視覺效果點陣圖內容區域。

</dd> <dt>

<span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**斗篷**
</dt> <dd>

若要暫時防止桌面視窗管理員 (DWM) 將視窗繪製至顯示器。 應用程式通常會在 DirectComposition 使用組合中的視窗點陣圖時，遮蓋視窗。

</dd> <dt>

<span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**提交**
</dt> <dd>

將一批命令提交至 DirectCompositionDirectComposition 以進行處理。

</dd> <dt>

<span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**複合模式**
</dt> <dd>

有幾種方式可以將兩個位圖混合 (來源和目的地) ，以達成特定效果。

</dd> <dt>

<span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**組成**
</dt> <dd>

在應用程式 UI 中套用各種轉換、效果和動畫來產生預期的視覺效果結果，結合和操作的點陣圖集合。

</dd> <dt>

<span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**撰寫目標視窗**
</dt> <dd>

視覺化樹狀結構所系結的視窗，也是繪製產生的組合。

</dd> <dt>

<span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**影響**
</dt> <dd>

修改視覺化樹狀結構點陣圖如何進行柵格化的作業，通常是藉由套用圖元著色器。

</dd> <dt>

<span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**效果群組**
</dt> <dd>

一組點陣圖效果，會一起套用以修改視覺效果子樹狀結構的點陣化。

</dd> <dt>

<span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**框架**
</dt> <dd>

組合引擎的反復專案，會產生視覺化樹狀結構的點陣化。

</dd> <dt>

<span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**前端緩衝區**
</dt> <dd>

由圖形介面卡轉譯並顯示在監視器上的記憶體矩形。

</dd> <dt>

<span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**插補模式**
</dt> <dd>

屬性，決定點陣圖在轉換時的組成方式，讓點陣圖中的圖元與螢幕上的圖元之間沒有一對一的對應關係。

</dd> <dt>

<span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**根視覺效果**
</dt> <dd>

視覺化樹狀結構中所有其他視覺效果的來源視覺效果。

</dd> <dt>

<span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**交換鏈**
</dt> <dd>

一或多個後置緩衝區的集合，可連續呈現給前端緩衝區

</dd> <dt>

<span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**表面**
</dt> <dd>

顯示記憶體的線性區域表示，通常位於顯示配接器的顯示記憶體中，雖然表面可以存在於系統記憶體中。

</dd> <dt>

<span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**變換**
</dt> <dd>

矩陣，表示二維或三維空間中的座標轉換。

</dd> <dt>

<span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**轉換群組**
</dt> <dd>

在套用至視覺效果之前，其矩陣會以集合中指定的順序相乘的轉換集合。

</dd> <dt>

<span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**視覺**
</dt> <dd>

物件，其中包含點陣圖物件的選擇性參考，以及決定點陣圖如何轉譯至螢幕的一組屬性。

</dd> <dt>

<span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**視覺物件**
</dt> <dd>

請參閱 [*視覺效果*](/windows)。

</dd> <dt>

<span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**視覺化子樹**
</dt> <dd>

視覺化樹狀結構的一部分，其中包含特定視覺效果及其所有子系和附屬視覺效果。

</dd> <dt>

<span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**視覺化樹狀結構**
</dt> <dd>

用來建立組合的視覺效果階層式集合。

</dd> <dt>

<span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**無視窗交換鏈**
</dt> <dd>

與 DirectComposition 視覺物件（而非視窗）相關聯的交換鏈。

</dd> </dl>

 

 