---
description: 描述介面卡重新整理速率與目前或目前作業完成率之間的關聯性。 這些值也可作為 D3DCAPS9 之 PresentationIntervals 欄位的旗標值。
ms.assetid: a7d774c1-93c0-47d8-a8a7-e66e394726a3
title: D3DPRESENT (D3d9.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f71c89304a82344b6217a44f3d625200b03a286
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472778"
---
# <a name="d3dpresent"></a>D3DPRESENT

描述介面卡重新整理速率與 [**目前**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) 或 [**目前**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) 作業完成率之間的關聯性。 這些值也可作為 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)之 PresentationIntervals 欄位的旗標值。


| 常數 | 描述 | 
|----------|-------------|
| <span id="D3DPRESENT_DONOTFLIP"></span><span id="d3dpresent_donotflip"></span><dl><dt><strong>D3DPRESENT_DONOTFLIP</strong></dt></dl> | 在轉譯期間，使用前端緩衝區作為來源和目標介面。 已排程框架同步處理，但顯示的介面不會變更。 只有當應用程式處於全螢幕模式且已指定 D3DSWAPEFFECT_FLIPEX 時，才能使用此旗標。 <br /> 此旗標僅適用于 Direct3D 9Ex。<br /> | 
| <span id="D3DPRESENT_DONOTWAIT"></span><span id="d3dpresent_donotwait"></span><dl><dt><strong>D3DPRESENT_DONOTWAIT</strong></dt></dl> | Hal 裝置無法排程簡報。 如果這個旗標是在 <a href="/windows/desktop/api"><strong>出現</strong></a>的呼叫中設定，而且硬體正在忙於處理或等候垂直同步間隔，則顯示會傳回 D3DERR_WASSTILLDRAWING，表示 array.blit 作業不完整。<br /> | 
| <span id="D3DPRESENT_FLIPRESTART"></span><span id="d3dpresent_fliprestart"></span><dl><dt><strong>D3DPRESENT_FLIPRESTART</strong></dt></dl> | 保留的。<br /> | 
| <span id="D3DPRESENT_FORCEIMMEDIATE"></span><span id="d3dpresent_forceimmediate"></span><dl><dt><strong>D3DPRESENT_FORCEIMMEDIATE</strong></dt></dl> | D3DPRESENT_INTERVAL_IMMEDIATE 會在此 <a href="/windows/desktop/api"><strong>目前</strong></a> 的呼叫上強制執行。 只有在使用 D3DSWAPEFFECT_FLIPEX 時，才能指定此旗標。 視窗化和全螢幕呈現行為相同。 如果媒體應用程式想要捨棄已偵測為最晚的框架，並在組合時顯示後續的畫面格，這特別有用。 如果未正確指定此旗標，則會傳回不正確參數錯誤。 當有多個具有 D3DPRESENT_FORCEIMMEDIATEs 的連續框架排入佇列時，只會顯示最後一個畫面格，同時顯示視窗和全螢幕簡報。<br /> 此旗標可在 Windows 7 或更新版本作業系統上的 Direct3D 9Ex 中取得。<br /> 使用 D3DSWAPEFFECT_FLIPEX 時，使用 D3DPRESENT_INTERVAL_IMMEDIATE 或 D3DPRESENT_INTERVAL_FORCEIMMEDIATE 所顯示的每個框架都會覆寫上一個畫面格的目前間隔。 例如，如果您使用下列交換效果將下列畫面格排在佇列中：框架 A (D3DPRESENT_INTERVAL_ONE) 、框架 B (D3DPRESENT_INTERVAL_ONE) 、框架 C (D3DPRESENT_INTERVAL_ONE) 、框架 D (D3DPRESENT_INTERVAL_FORCEIMMEDIATE) ，框架 D 將會覆寫框架 C 的目前間隔。 每個出現間隔的顯示畫面格為框架 A、框架 B (框架 C，) 框架 D 覆寫。<br /> 請參閱＜備註＞。<br /> | 
| <span id="D3DPRESENT_INTERVAL_DEFAULT"></span><span id="d3dpresent_interval_default"></span><dl><dt><strong>D3DPRESENT_INTERVAL_DEFAULT</strong></dt></dl> | 這幾乎相當於 D3DPRESENT_INTERVAL_ONE。 請參閱＜備註＞。<br /> | 
| <span id="D3DPRESENT_INTERVAL_ONE"></span><span id="d3dpresent_interval_one"></span><dl><dt><strong>D3DPRESENT_INTERVAL_ONE</strong></dt></dl> | 驅動程式會等候垂直回溯期間 (執行時間將會「接下來」以防止卸載) 。 <a href="/windows/desktop/api"><strong>目前</strong></a> 的作業不會比螢幕重新整理更頻繁地受到影響;執行時間會在每個介面卡重新整理期間最多完成一項作業。 這相當於使用 DirectX 8.1 中的 D3DSWAPEFFECT_COPYVSYNC。 此選項一律適用于視窗型和全螢幕交換鏈。 請參閱＜備註＞。<br /> | 
| <span id="D3DPRESENT_INTERVAL_TWO"></span><span id="d3dpresent_interval_two"></span><dl><dt><strong>D3DPRESENT_INTERVAL_TWO</strong></dt></dl> | 驅動程式會等候垂直回溯期間。 <a href="/windows/desktop/api"><strong>目前</strong></a> 的作業不會受到比每秒螢幕重新整理更頻繁的影響。 檢查 PresentationIntervals cap (查看 <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) ，查看驅動程式是否支援 D3DPRESENT_INTERVAL_TWO。<br /> | 
| <span id="D3DPRESENT_INTERVAL_THREE"></span><span id="d3dpresent_interval_three"></span><dl><dt><strong>D3DPRESENT_INTERVAL_THREE</strong></dt></dl> | 驅動程式會等候垂直回溯期間。 <a href="/windows/desktop/api"><strong>目前</strong></a> 的作業不會受到比每個第三個螢幕重新整理更頻繁的影響。 檢查 PresentationIntervals cap (查看 <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) ，查看驅動程式是否支援 D3DPRESENT_INTERVAL_THREE。<br /> | 
| <span id="D3DPRESENT_INTERVAL_FOUR"></span><span id="d3dpresent_interval_four"></span><dl><dt><strong>D3DPRESENT_INTERVAL_FOUR</strong></dt></dl> | 驅動程式會等候垂直回溯期間。 <a href="/windows/desktop/api"><strong>目前</strong></a> 的作業不會受到比每四個螢幕重新整理更頻繁的影響。 檢查 PresentationIntervals 成員 (查看 <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) ，查看驅動程式是否支援 D3DPRESENT_INTERVAL_FOUR。<br /> | 
| <span id="D3DPRESENT_INTERVAL_IMMEDIATE"></span><span id="d3dpresent_interval_immediate"></span><dl><dt><strong>D3DPRESENT_INTERVAL_IMMEDIATE</strong></dt></dl> | 執行時間會立即更新視窗用戶端區域，而且在介面卡重新整理期間可能會超過一次。 這相當於使用 DirectX 8 中的 D3DSWAPEFFECT_COPY。 <a href="/windows/desktop/api"><strong>目前</strong></a> 的作業可能會立即受到影響。 此選項一律適用于視窗型和全螢幕交換鏈。 請參閱＜備註＞。<br /> | 
| <span id="D3DPRESENT_LINEAR_CONTENT"></span><span id="d3dpresent_linear_content"></span><dl><dt><strong>D3DPRESENT_LINEAR_CONTENT</strong></dt></dl> | 要呈現的背景緩衝區內容是線上性色彩空間中。 <br /><ul><li>此簡報會從線性空間隱含地轉換為 sRGB (gamma = 2.2) 。 這是唯一支援的轉換。</li><li>由於此旗標代表後緩衝區內容的屬性，因此可以在 <a href="/windows/desktop/api"><strong>目前</strong></a> 的呼叫期間指定旗標。 換句話說，應用程式可以在某個框架中呈現線性內容，然後在下一個畫面中切換到更正的內容。</li><li>當交換鏈為全螢幕時，會忽略此旗標。  (請注意，此旗標只適用于 <a href="/windows/desktop/api"><strong>目前</strong></a>的明確交換鏈版本。 <a href="/windows/desktop/api"><strong>目前</strong></a>的方法不會採用旗標參數。 ) </li><li>一律接受此旗標，但只有在驅動程式公開 D3DCAPS3_LINEAR_TO_SRGB_PresentATION 時，才會生效 &gt; 。</li><li>唯一支援的背景緩衝區格式為 <a href="d3dformat.md">X8R8G8B8</a>。</li></ul>查看 <a href="gamma.md">視窗型交換鏈</a>。<br /> | 
| <span id="D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR"></span><span id="d3dpresent_video_restrict_to_monitor"></span><dl><dt><strong>D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR</strong></dt></dl> | 將轉譯的內容裁剪至介面卡設為目標的監視器/裝置，並顯示 Flip3D 視圖中的內容縮圖，以及其他監視器的工作列縮圖。 <br /> 此旗標僅適用于 Direct3D 9Ex。<br /> 如需 Windows Vista 這項功能的進一步詳細資料，請參閱<a href="/windows/desktop/dwm/dwm-overview">桌面視窗管理員</a>。 如果您不是在桌面撰寫模式中執行，旗標會提供與 <a href="d3dpresentflag.md">D3DPRESENTFLAG_DEVICECLIP</a>相同的行為。<br /><blockquote>[!Note]<br />此旗標只能搭配 D3DSWAPEFFECT_FLIPEX 交換效果使用。 此旗標與<em>其他</em>交換效果的用法已被取代，在未來的 Windows 版本中可能無法運作。</blockquote><br /> | 
| <span id="D3DPRESENT_UPDATEOVERLAYONLY"></span><span id="d3dpresent_updateoverlayonly"></span><dl><dt><strong>D3DPRESENT_UPDATEOVERLAYONLY</strong></dt></dl> | 更新覆迭位置或 >colorkey 資料，而不會造成實際的翻轉，而不會變更顯示影像的持續時間。<br /> 此旗標僅適用于 Direct3D 9Ex。<br /> | 
| <span id="D3DPRESENT_HIDEOVERLAY"></span><span id="d3dpresent_hideoverlay"></span><dl><dt><strong>D3DPRESENT_HIDEOVERLAY</strong></dt></dl> | 關閉覆蓋硬體。<br /> 此旗標僅適用于 Direct3D 9Ex。<br /> | 
| <span id="D3DPRESENT_UPDATECOLORKEY"></span><span id="d3dpresent_updatecolorkey"></span><dl><dt><strong>D3DPRESENT_UPDATECOLORKEY</strong></dt></dl> | 重新繪製 >colorkey 的資料。<br /> 此旗標僅適用于 Direct3D 9Ex。<br /> | 


## <a name="remarks"></a>備註

視窗模式支援 D3DPRESENT \_ 間隔 \_ 預設值、D3DPRESENT \_ 間隔 \_ 立即和 D3DPRESENT \_ 間隔 \_ 一。 D3DPRESENT \_ 間隔 \_ 預設值和 D3DPRESENT \_ 間隔 \_ 是幾乎相等的 (請參閱以下有關計時器解析度的資訊) 。 它們的執行方式類似于複製 VSYNC，因為 \_ 每個畫面都只會有一個畫面格，而且它們會防止使用橫樑來卸載-如下所示。 相反地，D3DPRESENT \_ 間隔 \_ 會立即嘗試提供無限制的表示速率。

全螢幕模式支援類似視窗模式的使用方式，方法是直接支援 D3DPRESENT 間隔，不論重新整理 \_ \_ 速率或交換效果為何。 D3DPRESENT \_ 間隔 \_ 預設會使用預設的系統計時器解析度，而 D3DPRESENT \_ 間隔會 \_ 呼叫 [**timeBeginPeriod**](/windows/win32/api/timeapi/nf-timeapi-timebeginperiod) 以增強系統計時器解析度。 這可改善垂直同步的品質，但會耗用稍微多一點的處理時間。 這兩個參數都會嘗試垂直同步處理。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9。h</dt> </dl> |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
