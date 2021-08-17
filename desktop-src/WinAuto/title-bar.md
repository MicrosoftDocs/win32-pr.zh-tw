---
title: '標題列 (MSAA UI 元素參考) '
description: 視窗頂端的標題列會顯示應用程式定義的圖示和文字行。
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9183e4c4f5364fb45ba2a73dd2d40509c03c7838bbb248e1d95765b675f50cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993998"
---
# <a name="title-bar-msaa-ui-element-reference"></a>標題列 (MSAA UI 元素參考) 

> [!Note]  
> 本主題描述用於 MSAA UI 元素參考的 **標題列** 物件。 此處未說明如何在各種 UI 架構中建立 **標題列** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

視窗頂端的標題列會顯示應用程式定義的圖示和文字行。 文字會指定應用程式的名稱，並指出視窗的用途。 標題列也可以讓使用者使用滑鼠或其他指標裝置來移動視窗。

標題列至少包含三個小按鈕，可最小化、最大化或還原，以及關閉與標題列相關聯的視窗。 標題列也包含即時線上說明按鈕。 在 Far-East 版本的 Windows 作業系統中執行的應用程式也可能包含輸入法編輯器 (IME) 按鈕。 Microsoft Active Accessibility 會將這些按鈕公開為標題列的子項目。

## <a name="iaccessible-methods"></a>IAccessible 方法

標題列支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

標題列支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>註解</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></td>
<td><strong>ChildCount</strong>屬性為五。 <strong>ChildCount</strong>屬性包含輸入法和上下文相關的 [說明] 按鈕（即使未顯示）。 未顯示的按鈕具有 [ <strong>狀態</strong> ] 屬性 <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>。</td>
</tr>
<tr class="even">
<td><strong>get_accDescription</strong></td>
<td>標題列本身的 [ <strong>描述</strong> ] 屬性是： &quot; 顯示視窗的名稱，並且包含操作控制項的控制項。 &quot; 標題列中的子按鈕具有下列描述：<br/>
<ul>
<li>&quot;將視窗移出</li>
<li>&quot;讓視窗填滿</li>
<li>&quot;將最小化或</li>
<li>&quot;關閉視窗&quot;</li>
<li>&quot;進入或離開內容-</li>
<li>&quot;按下按鍵時顯示鍵盤&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>get_accName</strong></td>
<td>標題列本身不支援 <strong>Name</strong> 屬性。 標題列中的子按鈕具有下列名稱：
<ul>
<li>&quot;最小化&quot;</li>
<li>&quot;最大化 &quot; 或 &quot; 還原 &quot;</li>
<li>&quot;關閉&quot;</li>
<li>&quot;內容說明&quot;</li>
<li>&quot;IME&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>get_accParent</strong></td>
<td>標題列的 <strong>父</strong> 屬性是主應用程式視窗 ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) 與標題列具有相同的應用程式定義視窗類別名稱。</td>
</tr>
<tr class="odd">
<td><strong>get_accRole</strong></td>
<td><strong>Role</strong>屬性為<a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>。 標題列中的子按鈕具有 <strong>角色</strong> 屬性 <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>。</td>
</tr>
<tr class="even">
<td><strong>get_accState</strong></td>
<td>標題列和子按鈕的 [<strong>狀態</strong>] 屬性可以是下列一或多個<a href="object-state-constants.md">值</a>的組合： <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a><br/></td>
</tr>
<tr class="odd">
<td><strong>get_accValue</strong></td>
<td><strong>Value</strong>屬性是與標題列中顯示的文字相同的字串。</td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a>備註

-   雖然應用程式的標題列具有 [**狀態] 屬性旗** 標 [**狀態系統可 \_ \_ 設定**](object-state-constants.md)目標，但 **它的狀態旗標**[**狀態系統並沒有 \_ \_ 焦點**](object-state-constants.md)。 將焦點設定為標題列物件將焦點放在應用程式視窗。
-   因為標題列物件不支援 [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)，所以標題列上的按鈕是簡單的元素。 它們本身不支援 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。 標題列物件提供這些子按鈕的相關資訊。
-   由於標題列無法取得焦點且沒有預設動作，因此不支援此控制項的 [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) 和 [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





