---
title: Direct3D 10 常見問題集
description: 本文包含有關 Direct3D 10 的一些常見問題，從 Direct3D 9 (D3D9) 移植現有的應用程式，到 Direct3D 10 (D3D10) 。
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092860"
---
# <a name="direct3d-10-frequently-asked-questions"></a>Direct3D 10 常見問題集

本文包含有關 Direct3D 10 的一些常見問題，從 Direct3D 9 (D3D9) 移植現有的應用程式，到 Direct3D 10 (D3D10) 。

-   [常數緩衝區](#constant-buffers)
-   [State](#state)
-   [格式](#formats)
-   [著色器連結](#shader-linkage)
-   [繪製呼叫](#draw-calls)
-   [資源](#resources)
-   [深度為材質](#depth-as-texture)
-   [MSAA](#msaa)
-   [損毀](#crashes)
-   [前提轉譯](#predicated-rendering)
-   [幾何著色器](#geometry-shader)
-   [HLSL](#hlsl)

## <a name="constant-buffers"></a>常數緩衝區

<dl> <dt>

<span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>更新常數緩衝區的最佳方式是什麼？
</dt> <dd>

使用捨棄的 UpdateSubresource 和 Map 應該會有相同的速度。 根據哪一個複製最少的記憶體量，在兩者之間進行選擇。 如果您已將資料儲存在記憶體中的一個連續區塊中，請使用 UpdateSubresource。 如果您需要從其他位置累積資料，請使用 Map 來捨棄。

</dd> <dt>

<span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>組織常數緩衝區最差的方式為何？
</dt> <dd>

將特定著色器的所有常數放入一個常數緩衝區，可實現最差的效能。 雖然這通常是從 D3D9 移植至 D3D10 最簡單的方式，但它可能會使效能癱瘓。 例如，假設有一個使用下列常數緩衝區的案例：

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

緩衝區為6560個位元組。 假設有一個應用程式具有要轉譯的1000物件，100個是 skinned 網格，而900則為靜態網格。 此外，假設此應用程式使用陰影對應搭配一個光源。 這表示有兩個行程，一個用於從光源所呈現的深度地圖，另一個用於向前轉譯行程。 這會導致2000繪製呼叫。 雖然每個繪製呼叫不需要更新常數緩衝區的每個部分，但是整個常數緩衝區仍會更新並傳送到卡片。 這會導致每個畫面格更新 13 MB 的資料， (2000 繪製呼叫乘以 6560 KB) 。

</dd> <dt>

<span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>組織常數緩衝區的最佳方式是什麼？
</dt> <dd>

最佳方式是依更新頻率來組織常數緩衝區。 以類似頻率更新的常數應該在相同的緩衝區中。 例如，請考慮以下的案例：「組織常數緩衝區有何最差的方法？」，但有更好的配置：

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

常數緩衝區依其更新頻率分割，但這只是解決方案的一半。 應用程式需要正確更新常數緩衝區，才能充分利用分割。 我們會假設與上面相同的場景：900靜態網格、100 skinned 網格、一次輕量，以及一次向前傳遞。 我們也會假設會儲存每個物件的一些常數緩衝區。 這表示，每個物件都會包含 VSPerSkinnedCB 或 VSPerStaticCB，視其為 skinned 或靜態而定。 這麼做是為了避免透過管線傳送的矩陣數量加倍。

我們將框架分成三個階段。 第一個階段是框架的開頭，且不包含任何轉譯，而只是持續更新。

<dl> <dt>

<span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**開始畫面格**
</dt> <dd>

-    (4 個位元組的應用程式時間更新 VSGlobalPerFrameCB) 
-   100 skinned 物件的更新 100 VSPerSkinnedCB (640000 個位元組) 
-   900靜態物件的更新 VSPerStaticCB (57600 位元組) 

接下來是陰影地圖傳遞。 請注意，實際更新的唯一常數緩衝區是 VSPerPassCB。 所有其他常數緩衝區都已在開始框架傳遞期間更新。 雖然我們仍然需要系結這些常數緩衝區，但傳遞至視訊卡的資訊量很少，因為已更新緩衝區。

</dd> <dt>

<span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**陰影傳遞**
</dt> <dd>

-   更新 VSPerPassCB (72 個位元組) 
-   繪製 100 skinned 網格 (100 系結，沒有更新) 
-   繪製900靜態網格 (100 系結，沒有更新) 

同樣地，向前轉譯傳遞只需要更新每個材質的資料，因為它不會儲存在每個網格中。 假設在場景中使用500材質：

</dd> <dt>

<span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**向前傳遞**
</dt> <dd>

-   更新 VSPerPassCB (72 個位元組) 
-   更新 500 VSPerMaterialCBs (10000 位元組) 

這會導致總共只有 707 KB。 雖然這是非常假設的案例，但它會透過依更新頻率排序常數，來說明可減少多少常數的更新負擔。

</dd> </dl> </dd> <dt>

<span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>如果我沒有足夠的空間來儲存網格、材質等的個別常數緩衝區，該怎麼辦？ 
</dt> <dd>

您一律可以使用常數緩衝區的分層式系統。 建立變動大小的常數緩衝區 (16 個位元組、32個位元組、64個位元組，依此類推，) 最多需要最大的常數緩衝區大小。 當您將常數緩衝區系結至著色器時，請選取可保存著色器所需資料的最小常數緩衝區。 雖然這種方法的效率稍微低，但這是不錯的中間步驟。

</dd> <dt>

<span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>我在不同的著色器之間共用了常數緩衝區。 一個著色器可能會使用所有常數，但另一個著色器可能會使用某些常數。 更新這些專案的最佳方式是什麼？ 
</dt> <dd>

其中一個方法是更進一步分割常數緩衝區。 不過，有太多常數緩衝區系結的點。 在此情況下，請將很多著色器未使用的常數，移至常數緩衝區的結尾。 從著色器取得變數資料時，請使用 \_ \_ D3D10 著色器變數 DESC 中的 D3D10 SVF 使用旗標 \_ \_ \_ 來判斷變數是否已使用。 藉由在常數緩衝區的結尾放置未使用的變數，您可以將較小的緩衝區系結至不使用這些變數的著色器，藉此節省更新成本。

</dd> <dt>

<span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>如果每個畫面上只上傳一次字元的骨骼，而不是每次通過/繪製一次，則可以改善畫面播放速率的大小？ 
</dt> <dd>

您可以根據多餘的資料量，改善介於8% 到50% 之間的畫面播放速率。 在最糟的情況下，效能不會降低。

</dd> <dt>

<span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>我應該同時系結多少常數緩衝區？ 
</dt> <dd>

系結取得所有資料到著色器所花費的常數緩衝區數目下限。 在實際案例中，建議使用五個常數緩衝區數目。 在著色器之間共用常數緩衝區 (將相同的 CB 系結至 VS 和 PS) 也可以改善效能。

</dd> <dt>

<span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>系結常數緩衝區是否有成本，而不使用它們？ 
</dt> <dd>

是的，如果您不想要使用緩衝區，請不要呼叫 VSSetConsantBuffer 或 PSSetConstantBuffer。 這項額外的 API 額外負荷可能會在多個繪製呼叫的過程中增加。

</dd> </dl>

## <a name="state"></a>狀態

<dl> <dt>

<span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>在 D3D10 中管理狀態的最佳方式為何？ 
</dt> <dd>

最好的解決方法是事先瞭解所有的狀態，然後事先建立狀態物件。 這表示在轉譯時期，狀態系結是唯一需要發生的作業。 D3D10 也會篩選出重複的專案。

</dd> <dt>

<span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>我的遊戲動態載入或具有使用者產生的內容。 我無法提前載入所有的狀態物件。 我該怎麼辦？ 
</dt> <dd>

這裡有兩個解決方案。 第一種方式是立即建立狀態物件，並讓 D3D10 篩選出重複的專案。 但是，不建議在每個畫面上有許多狀態物件變更的案例中使用。 更好的解決方法是在雜湊表中找不到符合需求的狀態物件時自行進行雜湊處理，並建立狀態物件。 使用自訂雜湊表的原因是，應用程式可以根據特定應用程式的使用案例來選取快速雜湊。 例如，如果應用程式只變更 BlendState 中的 rendertargetwritemask，並保留所有其他值，則應用程式可以從 rendertargetwritemask 產生雜湊，而不是整個結構。

</dd> <dt>

<span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>AlphaTest 狀態已消失。 它在哪裡？ 
</dt> <dd>

AlphaTest 現在應該是著色器中的效能。 請參閱 FixedFuncEMU 範例。

</dd> <dt>

<span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>使用者裁剪平面發生什麼事？ 
</dt> <dd>

使用者裁剪平面已移至著色器。 有兩種方式可以處理這種情況。 第一個是 \_ 從頂點著色器或幾何著色器輸出 SV ClipDistance。 另一個選項是在圖元著色器中使用 [捨棄]，並根據頂點著色器或幾何著色器所傳遞的某個值。 進行這兩者的實驗，以查看您的特定案例更快。 使用 SV \_ ClipDistance 可能會導致硬體使用以幾何為基礎的裁剪常式，而這可能會造成幾何系結繪製呼叫的執行速度變慢。 同樣地，使用「捨棄」會將工作移至圖元著色器，這可能會造成圖元系結的繪製呼叫執行速度較慢。

</dd> <dt>

<span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>清除不遵守任何狀態設定，例如我的轉譯器狀態中的剪式矩形設定。 
</dt> <dd>

清除已與管線狀態分開。 為了取得 D3D9 樣式的行為，請藉由繪製全螢幕的四種方式來清除。

</dd> <dt>

<span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>我將狀態設回預設值，以嘗試診斷轉譯錯誤。 現在我的畫面只會顯示黑色，雖然我知道要在螢幕上繪製物件。 
</dt> <dd>

將狀態設回預設值 (Null) 時，請確定 OMSetBlendState 呼叫中的 SampleMask 永遠不會是零。 如果 SampleMask 設定為零，則所有範例都會以邏輯方式與零。 在此案例中，沒有任何範例會通過 blend 測試。

</dd> <dt>

<span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>D3DSAMP \_ SRGBTEXTURE 狀態在哪裡？ 
</dt> <dd>

已移除 SRGB 作為取樣器狀態的一部分，現在會系結至材質格式。 如果您 \_ 在 Direct3D 9 中指定了 D3DSAMP SRGBTEXTURE，系結 SRGB 材質將會產生相同的取樣。

</dd> </dl>

## <a name="formats"></a>格式

<dl> <dt>

<span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>哪一種 D3D9 格式對應至哪個 D3D10 格式？ 
</dt> <dd>

如需詳細資訊，請參閱 [direct3d 9 至 direct3d 10 考慮](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations)。

</dd> <dt>

<span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>A8R8G8B8 紋理格式有何變化？ 
</dt> <dd>

它們在 D3D10 中已被取代。 您可以將紋理以 R8G8B8A8 的形式重新來源，或者可以在載入時 swizzle，也可以在著色器中 swizzle。

</dd> <dt>

<span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>如何? 使用調色盤材質？ 
</dt> <dd>

將您的色板置於材質或常數緩衝區，並將其系結至管線。 在圖元著色器中，使用調色盤材質中的索引進行間接查閱。

</dd> <dt>

<span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>這些新的 SRGB 格式有哪些？ 
</dt> <dd>

已將 SRGB 移除為取樣器狀態的一部分，而且現在已系結至材質格式。 如果您 \_ 在 Direct3D 9 中指定了 D3DSAMP SRGBTEXTURE，系結 SRGB 材質將會產生相同的取樣。

</dd> <dt>

<span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>三角形風扇在哪裡去了？ 
</dt> <dd>

三角形在 D3D10 中已被取代。 三角形的風扇必須在內容管線或載入時進行轉換。

</dd> </dl>

## <a name="shader-linkage"></a>著色器連結

<dl> <dt>

<span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>我的 Direct3D 9 著色器可以編譯為著色器模型4.0，但是當我將它們系結至管線時，會出現在偵錯工具中使用偵錯工具執行時間顯示的連結錯誤。 
</dt> <dd>

著色器連結在 D3D10 中更嚴格。 後續階段中的元素必須以其從上一個階段輸出的順序來讀取。 例如：

頂點著色器輸出：

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

圖元著色器會讀取：

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

雖然圖元著色器中不需要位置，但這會導致連結錯誤，因為位置是從頂點著色器輸出，而不是由圖元著色器讀取。 更正確的版本看起來會像這樣：

頂點著色器輸出：

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

圖元著色器會讀取：

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

在此情況下，頂點著色器會輸出相同的資訊，但現在圖元著色器會在訂單輸出中讀取專案。 由於圖元著色器在 Tex 之後不會讀取任何內容，因此我們不需要擔心 VS 所輸出的資訊會比 PS 正在讀取的還多。

</dd> <dt>

<span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>我需要著色器簽章才能建立輸入版面配置，但我會在建立著色器之前載入網格，並建立版面配置。 該怎麼辦？ 
</dt> <dd>

其中一個解決方法是在載入網格之前切換訂單和載入著色器。 不過，這種方式比完成的簡單得多。 您隨時都可以視需要建立應用程式所需的輸入版面配置。 您必須保留一個版本的著色器簽章。 您應該根據著色器和緩衝區配置建立雜湊，而且只有當相符專案尚未存在時，才會建立輸入版面配置。

</dd> </dl>

## <a name="draw-calls"></a>繪製呼叫

<dl> <dt>

<span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>D3D10 到達 60 Hz 的繪製通話限制為何？ 30 Hz？ 
</dt> <dd>

由於每個繪製呼叫的 CPU 成本，Direct3D 9 對繪製呼叫的數目有限制。 在 Direct3D 10 上，每個繪製呼叫的成本都已減少。 不過，繪製呼叫和畫面播放速率之間不再有明確的關聯性。 由於繪製呼叫通常需要許多支援呼叫 ( 常數緩衝區更新、材質系結、狀態設定等等) 因此，API 的畫面播放速率影響現在更相依于整體的 API 使用方式，而不只是繪製呼叫計數。

</dd> </dl>

## <a name="resources"></a>資源

<dl> <dt>

<span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>我應該使用何種資源使用類型來執行哪些作業？ 
</dt> <dd>

使用下列內容頁：

-   CPU 會每個畫面更新一次以上的資源： D3D10 \_ 使用量 \_ 動態
-   CPU 會將每個畫面格的資源更新為小於一次： D3D10 \_ 使用量 \_ 預設值
-   CPU 不會更新資源： D3D10 使用方式 \_ \_ 不可變
-   CPU 需要讀取資源： D3D10 \_ 使用量 \_ 暫存

因為常數緩衝區一律會經常更新，所以它們不符合「操作簡介」。 針對要用於常數緩衝區的資源類型，請參閱 [常數緩衝區](#constant-buffers) 區段。

</dd> <dt>

<span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>DrawPrimitiveUP 和 DrawIndexedPrimitiveUP 會發生什麼事？ 
</dt> <dd>

它們 D3D10。 若為動態幾何，請使用大型 D3D10 \_ 使用 \_ 動態緩衝區。 在框架的開頭，將它與 D3D10 \_ map \_ WRITE 捨棄進行對應 \_ 。 針對每個後續的繪製呼叫，將寫入指標提前超過先前繪製頂點的位置，並將緩衝區與 D3D10 \_ 對應 \_ 寫入 [ \_ 不覆寫] \_ 。 如果您接近框架結尾之前的緩衝區結尾，請將寫入指標包裝到開頭和 map，並 D3D10 \_ 對應 \_ 寫入 \_ 捨棄。

</dd> <dt>

<span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>我可以將16位的索引和32位索引寫入相同的動態幾何緩衝區嗎？ 
</dt> <dd>

是的，您可以，但這可能會對特定硬體造成效能上的影響。 針對動態16位索引資料和32位索引資料建立不同的緩衝區是比較安全的做法。

</dd> <dt>

<span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>如何? 從 GPU 將資料讀取回 CPU？ 
</dt> <dd>

您必須使用暫存資源。 使用 CopyResource 將資料從 GPU 資源複製到預備資源。 對應暫存資源以讀取資料。

</dd> <dt>

<span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>我的應用程式相依于 StretchRect 功能。 
</dt> <dd>

因為這本質上是基本 Direct3D 功能的包裝函式，所以已從 API 中移除。 部分 StretchRect 功能已移至 D3DX10LoadTextureFromTexture。 針對格式轉換和複製材質，D3DX10LoadTextureFromTexture 可能會進行工作。 不過，從某個大小轉換成另一種大小的作業，可能需要在應用程式中轉譯成材質。

</dd> <dt>

<span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>資源的地圖呼叫沒有位移或大小。 這些都是在 Direct3D 9 上的鎖定呼叫;為何會變更？ 
</dt> <dd>

在 Direct3D 9 上鎖定呼叫的位移和大小基本上是 API 雜亂的，且驅動程式通常會忽略此情形。 您應改為從 Map 呼叫中傳回的指標來計算位移。

</dd> </dl>

## <a name="depth-as-texture"></a>深度為材質

<dl> <dt>

<span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>速度更快？ 使用深度作為材質或將深度寫到 Alpha 並閱讀 
</dt> <dd>

這是應用程式和硬體特有的。 使用哪一個可節省最多頻寬。 如果您已經使用多個轉譯目標並有額外的通道，則從著色器寫入深度可能是較佳的解決方案。 此外，將深度寫到 Alpha 或其他轉譯目標，可讓您撰寫線性深度值，以加速需要存取深度緩衝區的計算。

</dd> <dt>

<span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>是否可以將材質系結為輸入，並將其系結為深度樣板材質（只要我停用深度寫入）？ 
</dt> <dd>

不在 D3D10 中。

</dd> </dl>

## <a name="msaa"></a>MSAA

<dl> <dt>

<span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>我可以解析 MSAA 深度樣板材質嗎？ 
</dt> <dd>

不在 D3D10 中。 不過，您可以從 MSAA 材質取樣個別樣本。 如需詳細資訊，請參閱 [HLSL](#hlsl) 一節。

</dd> <dt>

<span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>為什麼我的應用程式在啟用 MSAA 時立即損毀？ 
</dt> <dd>

確定您要啟用由驅動程式所列舉的 MSAA 樣本計數和品質數位。

</dd> </dl>

## <a name="crashes"></a>損毀

<dl> <dt>

<span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>我的應用程式在 D3D10 或驅動程式中損毀，但我不知道原因。 
</dt> <dd>

第一個步驟是啟用將偵錯工具執行時間 ([**D3D10 \_ 建立 \_ 裝置 \_ 調試**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) 程式旗標傳入 [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)) 。 這會將最常見的錯誤公開為 debug 輸出。

</dd> <dt>

<span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>當我嘗試搭配使用我的應用程式與應用程式時，PIX 會當機。 
</dt> <dd>

第一個步驟是啟用將偵錯工具執行時間 ([**D3D10 \_ 建立 \_ 裝置 \_ 調試**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) 程式旗標傳入 [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)) 。 如果偵錯工具輸出不幹淨，PIX 有更高的損毀可能性。

</dd> <dt>

<span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>我的遊戲在 D3D10 的32位 Vista 上的虛擬位址空間不足。 在 D3D9 上沒有任何問題。 
</dt> <dd>

D3D10 和虛擬位址空間有一些問題。 這已在 [KB940105](https://support.microsoft.com/kb/940105)中修正。 如果這無法修正您的問題，請確定您未在 D3D10 中建立更多可對應 (鎖定) 的資源，而不是在 D3D9 中建立。 也請考慮移植到64位，因為這會在未來更普遍。

</dd> </dl>

## <a name="predicated-rendering"></a>前提轉譯

<dl> <dt>

<span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>我使用前提轉譯 (根據遮蔽查詢結果) 。 為什麼我的應用程式仍然是一樣的速度？ 
</dt> <dd>

首先，請確定您想要跳過的呈現實際上是應用程式瓶頸。 如果不是瓶頸，則略過轉譯將無法協助畫面播放速率。

其次，請確定在您想要述詞的查詢和轉譯的問題之間，已經過足夠的時間。 如果查詢在轉譯呼叫到達 GPU 時未完成，則仍會進行轉譯。

第三，predication 只會略過特定的呼叫。 略過的呼叫為 Draw、Clear、Copy、Update、ResolveSubresource 和 GenerateMips。 狀態設定、IA 安裝、對應和建立呼叫不遵守 predication。 如果要前提繪製呼叫周圍有許多狀態設定呼叫，仍會設定這些狀態。

</dd> </dl>

## <a name="geometry-shader"></a>幾何著色器

<dl> <dt>

<span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>我應該使用幾何著色器來 tessellate 我的 (在此處插入任何內容) ？ 
</dt> <dd>

不會。 幾何著色器不應該用於鑲嵌式。

</dd> <dt>

<span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>我可以使用幾何著色器來建立幾何嗎？ 
</dt> <dd>

是，在極少數的案例中。 目前 D3D10 中的幾何著色器 (2008) 元件並沒有處理許多擴充的能力。 未來可能會變更。 由於現有的點 sprite 硬體，視訊卡廠商可能會有一到四個擴充的特殊路徑。 任何其他擴充都必須非常有限。 ParticlesGS 和 PipesGS 範例只會執行有限的擴充，以達到高框架速率。 每個畫面格只會展開一些點。

</dd> <dt>

<span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>如何使用幾何著色器？ 
</dt> <dd>

需要對整個基本類型進行作業的任何作業，例如側面程式偵測、barycentric 座標等等。 也可以用來選取要將基本類型傳送至其中的轉譯目標陣列配量。

</dd> <dt>

<span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>我可以從幾何著色器輸出可變數量的幾何嗎？ 
</dt> <dd>

是的，但這可能會導致效能問題。 針對一個叫用輸出1點，並為另一個叫用4點。 在擴充方針內進行調整時，這可能會導致幾何著色器執行緒循序執行。

</dd> <dt>

<span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>D3D10 如何知道如何為我的網格產生連續的索引？ 或者，當我指定幾何著色器需要相鄰資訊時，為什麼 D3D10 無法正確轉譯。 
</dt> <dd>

相鄰資訊不是由 D3D10 所建立，而是由應用程式所建立。 鄰接索引是由應用程式產生的，而且每個基本必須包含六個索引;在六個中，奇數編號的索引是邊緣相鄰頂點。 ID3DX10Mesh：： GenerateAdjacencyAndPointsReps 可以用來產生此資料。

</dd> </dl>

## <a name="hlsl"></a>HLSL

<dl> <dt>

<span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>整數和位指令是否慢？ 
</dt> <dd>

它們可以是。 不同的 D3D10 卡可能只能針對可用的 ALU 單位子集發出整數運算。 這會高度依賴硬體。 請參閱您的個人硬體廠商，以取得如何處理該特定硬體上的整數作業的建議。 此外，請務必小心轉換類型。

</dd> <dt>

<span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>VPOS 發生什麼事？ 
</dt> <dd>

如果您將圖元著色器的輸入宣告為 SV \_ 位置，則會得到與將它宣告為 VPOS 相同的行為。

</dd> <dt>

<span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>如何? MSAA 材質範例？ 
</dt> <dd>

在您的著色器中，將材質宣告為 Texture2DMS。 然後，您可以使用 Texture2DMS 物件以外的範例方法來提取個別的範例。

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>如何? 告訴您是否真的使用常數緩衝區中的著色器變數？ 
</dt> <dd>

查看 \_ 針對該變數反映的 D3D10 著色器 \_ 變數 \_ DESC 結構。 uFlags 應 \_ 設定 D3D10 SVF \_ 使用旗標。

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>如何? 知道常數緩衝區中的著色器變數是否真的使用 FX10？ 
</dt> <dd>

目前無法使用 FX10。

</dd> <dt>

<span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>我無法控制 FX10 所建立的常數緩衝區。 他們如何建立和更新？ 
</dt> <dd>

所有 FX10 管理的常數緩衝區都會建立為 D3D10 \_ 使用量 \_ 預設資源，並使用 UpdateSubresource 進行更新。 因為 FX10 會保留所有常數資料的備份存放區，所以 UpdateSubresource 是更新這些資料的最佳方法。

</dd> <dt>

<span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>如何? 使用著色器模擬 fixed 函數管線？ 
</dt> <dd>

請參閱 FixedFuncEMU 範例。

</dd> <dt>

<span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>我應該使用新的 \[ 展開 \] 、 \[ 迴圈 \] 、 \[ 分支等 \] 編譯器提示嗎？ 
</dt> <dd>

一般而言不行。 編譯器通常會嘗試這兩種方式，並選擇最快的方法。 在某些情況下，可能需要使用 \[ 展開 \] ，例如，當迴圈內的材質提取需要存取漸層時。

</dd> <dt>

<span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>部分有效位數會對 D3D10 有任何差異嗎？ 我可以在我的 D3D9 HLSL 中指定部分有效位數，但不能在我的 D3D10 HLSL 中指定。 
</dt> <dd>

所有 D3D10 作業都指定為以32位浮點精確度執行。 因此，部分有效位數不應該在 D3D10 中產生任何差異。

</dd> <dt>

<span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>在 D3D9 中，我可以藉由將深度緩衝區系結為材質並使用一般 tex2d hlsl 指示，來進行 HW PCF 影子篩選。 如何? 在 D3D10 上這樣做呢？ 
</dt> <dd>

您必須使用比較取樣器狀態，並使用 SampleCmp 指令。

</dd> <dt>

<span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>此 register 關鍵字在 D3D10 中的運作方式為何？ 
</dt> <dd>

D3D10 中的 register 關鍵字現在適用于特定資源系結至的位置。 在此情況下，資源可以是緩衝區 (常數或) 、材質或取樣器。

-   針對常數緩衝區，請使用語法： register (bN) ，其中 N 是輸入位置 (0-15) 
-   針對材質，請使用語法： register (tN) ，其中 N 是輸入位置 (0-127) 
-   針對取樣器，請使用語法： register (sN) ，其中 N 是輸入位置 (0-127) 

</dd> <dt>

<span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>如果 register 只是用來指定要系結整個緩衝區的位置，如何? 在常數緩衝區內放置變數呢？ 
</dt> <dd>

使用 packoffset 關鍵字。 Packoffset 的引數是 c 0-4095 的形式 \[ \] 。 \[x、y、z、w \] 。 例如：

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

在這個常數緩衝區中，IWaste2Floats 會放在常數緩衝區中的第三個 float (第12個位元組) 。 IWasteMore 會放在常數緩衝區中的第13個 float4 或52nd 浮點數。

</dd> </dl>

 

 