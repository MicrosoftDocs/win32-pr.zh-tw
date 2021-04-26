---
description: 儲存和建立效果的選項。
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9077c8c7e3da479dd8963484bc289b84093ac0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995075"
---
# <a name="d3dxfx"></a>D3DXFX

儲存和建立效果的選項。

下表中的常數定義于 d3dx9effect 中。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>效果狀態儲存和還原旗標</td>
<td>Description</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESTATE</td>
<td>呼叫<a href="id3dxeffect--end.md"><strong>End</strong></a>時呼叫<a href="id3dxeffect--begin.md"><strong>Begin</strong></a>或還原時，不會儲存任何狀態。</td>
</tr>
<tr class="odd">
<td>D3DXFX_DONOTSAVESAMPLERSTATE</td>
<td>當呼叫<a href="id3dxeffect--end.md"><strong>End</strong></a>時，stateblock 會儲存<a href="id3dxeffect--begin.md"><strong>開始</strong></a>和還原狀態的狀態。</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESHADERSTATE</td>
<td>Stateblock 會將狀態 (儲存) 著色器和著色器常數，但在呼叫<a href="id3dxeffect--end.md"><strong>End</strong></a>時呼叫<a href="id3dxeffect--begin.md"><strong>Begin</strong></a>和還原狀態。</td>
</tr>
<tr class="odd">
<td>效果建立旗標</td>
<td>Description</td>
</tr>
<tr class="even">
<td>D3DXFX_NOT_CLONEABLE</td>
<td>效果將為非 cloneable，且不會包含任何著色器二進位資料。 <a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> 不會傳回著色器函式指標。 設定此旗標可減少大約50% 的效果記憶體使用量，因為它不需要讓效果系統將著色器的複本保留在記憶體中。 <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>、 <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>和<a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>會使用這個旗標。</td>
</tr>
<tr class="odd">
<td>D3DXFX_LARGEADDRESSAWARE</td>
<td>可將效果資源配置到電腦的 uppder 位址空間。 其中一項重要的限制是，您無法使用字串和控制碼交換。 例如，下列程式將無法再運作。 <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

相反地，您必須使用 [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) 之類的方法來儲存參數的控制碼，然後用它來將變數傳遞給效果。</td>
</tr>
</tbody>
</table>



 

下表中的常數預設未定義，且必須由開發人員定義。



| 效果預處理器 \# 定義 | Description                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXFX \_ LARGEADDRESS \_ 控制碼   | 在包含 d3dx9 之前定義此值，讓您的應用程式在嘗試將字串傳遞至 D3DXHANDLE 參數時無法編譯。 這有助於確保將有效的資訊傳遞給執行時間。 |
| 效果連結器旗標            | Description                                                                                                                                                                                                                          |
| 大型 \_ 位址 \_ 感知          | 設定連結器旗標大型 \_ 位址 \_ 感知 = 1 將可讓應用程式在需要時配置超過2gb 位址限制的資源。                                                                                      |



 

效果系統會使用狀態欄塊來自動儲存和還原狀態。 如需狀態欄塊的詳細資訊，請參閱 [ (Direct3D 9) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果常數](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



