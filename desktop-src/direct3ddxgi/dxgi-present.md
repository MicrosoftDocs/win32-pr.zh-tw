---
description: DXGI \_ 存在常數指定了在輸出中呈現畫面格的選項。
ms.assetid: 1ddf8643-ea3e-4c9f-8439-c245942f7333
title: 'DXGI_PRESENT (DXGI. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a21d53159572a52b372774e4988e775744ede5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992707"
---
# <a name="dxgi_present"></a>DXGI \_ 存在

**DXGI \_ 存在** 常數指定了在輸出中呈現畫面格的選項。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">常數/值</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span></span><dl> <dt><strong></strong></dt><dt>0</dt> </dl></td>
<td style="text-align: left;">顯示每個緩衝區的框架 (從目前的緩衝區) 到輸出。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_SEQUENCE"></span><span id="dxgi_present_do_not_sequence"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_SEQUENCE</strong></dt> <dt>0x00000002UL</dt> </dl></td>
<td style="text-align: left;">將目前緩衝區中的畫面格呈現給輸出。 使用這個旗標，讓簡報可以使用垂直空白的同步處理，而不是以一般方式來排序鏈中的緩衝區。<br/>
<blockquote>
[!Note]<br />
如果呼叫的應用程式在第一個目前的作業上設定 DXGI_PRESENT_DO_NOT_SEQUENCE 常數 (亦即，當沒有目前的緩衝區) 時，執行時間會忽略目前的作業，而不會呼叫驅動程式。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_TEST"></span><span id="dxgi_present_test"></span><dl> <dt><strong>DXGI_PRESENT_TEST</strong></dt> <dt>0x00000001UL</dt> </dl></td>
<td style="text-align: left;">不要將框架呈現在輸出中。 交換鏈的狀態將會經過測試，並傳回適當的錯誤。 DXGI_PRESENT_TEST 僅適用于從閒置狀態切換時：請勿使用它來判斷何時切換為閒置狀態，因為這樣做可能會讓交換鏈無法結束全螢幕模式。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTART"></span><span id="dxgi_present_restart"></span><dl> <dt><strong>DXGI_PRESENT_RESTART</strong></dt> <dt>0x00000004UL</dt> </dl></td>
<td style="text-align: left;">指定執行時間將捨棄未完成的佇列呈現。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_WAIT"></span><span id="dxgi_present_do_not_wait"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_WAIT</strong></dt> <dt>0x00000008UL</dt> </dl></td>
<td style="text-align: left;">指定執行時間將會使簡報失敗 (也就是當呼叫的執行緒遭到封鎖時，將呼叫 <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>IDXGISwapChain1：:P resent1</strong></a>) ，並 <a href="dxgi-error.md">DXGI_ERROR_WAS_STILL_DRAWING</a> 錯誤碼。執行時間會傳回 DXGI_ERROR_WAS_STILL_DRAWING 而非睡眠，直到解決相依性為止。<br/> <strong>Direct3D 11：</strong> 從 Windows 8 開始支援這個列舉值。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTRICT_TO_OUTPUT"></span><span id="dxgi_present_restrict_to_output"></span><dl> <dt><strong>DXGI_PRESENT_RESTRICT_TO_OUTPUT</strong></dt> <dt>0x00000010UL</dt> </dl></td>
<td style="text-align: left;">表示只會在特定輸出上顯示簡報內容。 內容將不會顯示在其他輸出上。 例如，如果使用者嘗試在其他輸出上重新放置影片內容，則不會顯示影片內容。 <br/> <strong>Direct3D 11：</strong> 從 Windows 8 開始支援這個列舉值。 <br/>
<blockquote>
[!Note]<br />
此旗標只能搭配 <a href="/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> 或 DXGI_SWAP_EFFECT_FLIP_DISCARD 的交換效果使用。 此旗標與 <em>其他</em> 交換效果的用法已被取代，在未來的 Windows 版本中可能無法運作。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_PREFER_RIGHT"></span><span id="dxgi_present_stereo_prefer_right"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_PREFER_RIGHT</strong></dt> <dt>0x00000020UL</dt> </dl></td>
<td style="text-align: left;">指出如果身歷聲存在必須縮小為 mono，則會使用靠右的觀賞，而不是左方的觀賞。<br/> <strong>Direct3D 11：</strong> 從 Windows 8 開始支援這個列舉值。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_TEMPORARY_MONO"></span><span id="dxgi_present_stereo_temporary_mono"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_TEMPORARY_MONO</strong></dt> <dt>0x00000040UL</dt> </dl></td>
<td style="text-align: left;">指出簡報應使用左邊的緩衝區做為 mono 緩衝區。 應用程式會呼叫 <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported"><strong>IDXGISwapChain1：： IsTemporaryMonoSupported</strong></a> 方法，以判斷交換鏈是否支援 &quot; 暫存 mono &quot; 。<br/> <strong>Direct3D 11：</strong> 從 Windows 8 開始支援這個列舉值。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_USE_DURATION"></span><span id="dxgi_present_use_duration"></span><dl> <dt><strong>DXGI_PRESENT_USE_DURATION</strong></dt> <dt>0x00000100UL</dt> </dl></td>
<td style="text-align: left;">此旗標必須由目前使用自訂持續時間 (自訂重新整理頻率) 的媒體應用程式設定。 請參閱 <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia"><strong>IDXGISwapChainMedia</strong></a>。<br/>
<blockquote>
[!Note]<br />
從 Windows 8.1 開始支援此值。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_ALLOW_TEARING"></span><span id="dxgi_present_allow_tearing"></span><dl> <dt><strong>DXGI_PRESENT_ALLOW_TEARING</strong></dt> <dt>0x00000200UL</dt> </dl></td>
<td style="text-align: left;">允許卸載是變數重新整理頻率顯示的需求。<br/> 在目前使用 DXGI_PRESENT_ALLOW_TEARING 的條件如下所示：<br/>
<ul>
<li>交換鏈必須使用 <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag"><strong>DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</strong></a> 旗標來建立。</li>
<li>傳入 <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>的同步間隔 (或</strong></a> <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) 必須是0。</li>
<li>DXGI_PRESENT_ALLOW_TEARING 旗標不能用在目前處於全螢幕獨佔模式的應用程式中 (由呼叫 <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate"><strong>SetFullscreenState (TRUE) </strong></a>) 來設定。 只能在視窗模式中使用。 若要在全螢幕 Win32 應用程式中使用此旗標，應用程式應該會出現在全螢幕無邊框的視窗中，並使用 <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation"><strong>IDXGIFactory：： MakeWindowAssociation</strong></a>停用自動 ALT + ENTER 全螢幕切換。 藉由呼叫進入全螢幕模式的 UWP 應用程式 <code>Windows::UI::ViewManagement::ApplicationView::TryEnterFullscreen()</code> 是全螢幕無邊框的視窗，而且可能會使用旗標。</li>
</ul>
使用這個旗標 <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>來呼叫 (</strong></a> 或 <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) ，而不符合上述條件，將會導致 DXGI_ERROR_INVALID_CALL 錯誤傳回給呼叫的應用程式。<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

在 IDXGISwapChain 期間會提供展示選項 [**：:P**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) 重新傳送或 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) 呼叫。 緩衝區會在交換鏈描述中指定 (請參閱 [**DXGI \_ 交換 \_ 鏈 \_ DESC**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) 或 [**dxgi \_ 交換 \_ 鏈 \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)) 。

DXGI \_ 存在 \_ 重新開機僅適用于翻轉模型交換鏈和全螢幕。 應用程式可以使用 DXGI \_ 存在 \_ 重新開機來復原播放中的問題，以及捨棄之前排入佇列的簡報。 如果已排入佇列的簡報是視窗化的案例，捨棄之前排入佇列的簡報會很 特別是，先前排入佇列的簡報可能會假設視窗是舊的大小 (也就是在提交) 之後發生調整大小作業。

DXGI \_ 存在 \_ 限制 \_ \_ 輸出僅適用于指定特定輸出的交換鏈，可在建立這些交換鏈時限制內容， ([**IDXGIFactory2：： CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)) 。 如果沒有要限制的輸出，旗標就會無效。

DXGI \_ 出現 \_ \_ 的立體慣用 \_ ，表示如果身歷聲存在必須縮減為 mono，則應該使用適當的眼睛，而不是左方 (預設) 眼。 如果有一側的品質較高，您可以使用此旗標 (例如，如果身歷聲組是從標準映射合成的，則為 < ) 

DXGI \_ 目前 \_ \_ 的立體暫存 \_ MONO 指出目前的緩衝區應使用左邊的緩衝區作為 MONO 緩衝區。 您可以使用此旗標，以避免在應用程式暫時沒有任何身歷聲內容時更新正確的緩衝區。 您應該盡可能使用此旗標，因為它能讓作業系統大幅優化，而且在某些情況下，它可以避免可見的模式變更成品。

您應該 \_ 在喜好設定中使用 DXGI 目前的 \_ 身歷聲 \_ 暫存 \_ MONO 旗標，以切換至您預期會再次使用身歷聲的大部分應用程式的 MONO 交換鏈。 您必須在應用程式中使用此旗標，而這些應用程式的執行時間非常長，或是很少會針對未使用記憶體的缺點顯示身歷聲。

> [!Note]  
> 切換至 mono 交換鏈的全螢幕應用程式會造成通常有可見成品 (的模式變更，例如「閃爍」 ) 。 不過，全螢幕交換鏈可能不支援暫存 mono。

 

DXGI \_ 出現 \_ 身歷聲 \_ 慣用 \_ ，而 dxgi \_ 目前有 \_ 身歷聲 \_ 暫存 \_ MONO 旗標只適用于身歷聲交換鏈。 如果您在顯示 mono 交換鏈時使用它們，就會發生不正確作業。

如果您在 \_ \_ \_ \_ 呈現不支援臨時 MONO 的身歷聲交換鏈時使用 DXGI 出現身歷聲暫存 MONO 旗標，則會發生錯誤，交換鏈不會顯示，且簡報會傳回 [DXGI \_ 錯誤不正確 \_ \_ 呼叫](dxgi-error.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>DXGI。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DXGI 常數](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 
