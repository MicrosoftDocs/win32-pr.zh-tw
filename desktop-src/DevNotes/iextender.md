---
description: IExtender 介面會提供一組新增至控制項介面的基本屬性。 程式設計人員可以使用這些屬性，就像是控制項的一部分一樣。
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: IExtender 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender
- IExtender.Align
- IExtender.get_Align
- IExtender.put_Align
- IExtender.Enabled
- IExtender.get_Enabled
- IExtender.put_Enabled
- IExtender.Height
- IExtender.get_Height
- IExtender.put_Height
- IExtender.Left
- IExtender.get_Left
- IExtender.put_Left
- IExtender.TabStop
- IExtender.get_TabStop
- IExtender.put_TabStop
- IExtender.Top
- IExtender.get_Top
- IExtender.put_Top
- IExtender.Visible
- IExtender.get_Visible
- IExtender.put_Visible
- IExtender.Width
- IExtender.get_Width
- IExtender.put_Width
- IExtender.Name
- IExtender.get_Name
- IExtender.Parent
- IExtender.get_Parent
- IExtender.Hwnd
- IExtender.get_Hwnd
- IExtender.Container
- IExtender.get_Container
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: a341f5d8a0ec554f008232f44156486df83d0fd8
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625108"
---
# <a name="iextender-interface"></a>IExtender 介面

**IExtender** 介面會提供一組新增至控制項介面的基本屬性。 程式設計人員可以使用這些屬性，就像是控制項的一部分一樣。

## <a name="members"></a>成員

**IExtender** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IExtender** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IExtender** 介面具有這些方法。



| 方法                         | 描述                                    |
|:-------------------------------|:-----------------------------------------------|
| [**移動**](iextender-move.md) | 移動 MDIForm、表單或控制項。<br/> |



 

### <a name="properties"></a>屬性

**IExtender** 介面具有這些屬性。



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >屬性</th>
<th >存取類型</th>
<th >描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td >對齊<br/></td>
<td >讀取/寫入<br/></td>
<td >傳回或設定值，這個值會決定物件在表單上的任何位置，或是顯示在表單的頂端、底部、左方或右方時，會自動調整大小以符合表單的寬度。<br/> 
<table>
<thead>
<tr class="header">
<th>常數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vbAlignNone 0</td>
<td>非 MDI 格式的 (預設值) 無：大小和位置可以在設計階段或在程式碼中設定。 如果物件是在 MDI 表單上，則會忽略此設定。</td>
</tr>
<tr class="even">
<td>vbAlignTop 1</td>
<td> (MDI 表單中的預設值) Top-物件位於表單頂端，而其寬度等於表單的 ScaleWidth 屬性設定。</td>
</tr>
<tr class="odd">
<td>vbAlignBottom 2</td>
<td>底部：物件位於表單底部，其寬度等於表單的 [ScaleWidth] 屬性設定。</td>
</tr>
<tr class="even">
<td>vbAlignLeft 3</td>
<td>左方：物件位於表單的左邊，而其寬度等於表單的 ScaleWidth 屬性設定。</td>
</tr>
<tr class="odd">
<td>vbAlignRight 4</td>
<td>Right：物件位於表單的右邊，而且其寬度等於表單的 ScaleWidth 屬性設定。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><p>容器</p></td>
<td ><p>唯讀</p></td>
<td ><p>傳回表單上控制項的容器。</p></td>
</tr>
<tr class="odd">
<td ><p>啟用</p></td>
<td ><p>讀取/寫入</p></td>
<td ><p>傳回或設定值，這個值會決定表單或控制項是否可以回應使用者產生的事件。</p></td>
</tr>
<tr class="even">
<td ><p>高度</p></td>
<td ><p>讀取/寫入</p></td>
<td ><p>傳回或設定物件的高度。</p></td>
</tr>
<tr class="odd">
<td ><p>Hwnd</p></td>
<td ><p>唯讀</p></td>
<td ><p>傳回表單或控制項的控制碼。</p></td>
</tr>
<tr class="even">
<td ><p>Left</p></td>
<td ><p>讀取/寫入</p></td>
<td ><p>傳回或設定物件的內部左邊緣和其容器左邊緣之間的距離。</p></td>
</tr>
<tr class="odd">
<td ><p>名稱</p></td>
<td ><p>唯讀</p></td>
<td ><p>傳回程序代碼中用來識別表單、控制項或資料存取物件的名稱。</p></td>
</tr>
<tr class="even">
<td ><p>父代</p></td>
<td ><p>唯讀</p></td>
<td ><p>傳回包含控制項或另一個物件或集合的表單、物件或集合。</p></td>
</tr>
<tr class="odd">
<td ><p>TabStop</p></td>
<td ><p>讀取/寫入</p></td>
<td ><p>傳回或設定值，這個值表示使用者是否可以使用 <strong>Tab</strong> 鍵將焦點提供給物件。</p></td>
</tr>
<tr class="even">
<td ><p>頁首</p></td>
<td ><p>讀取/寫入</p></td>
<td ><p>傳回或設定物件的內部上邊緣和其容器的上邊緣之間的距離。</p></td>
</tr>
<tr class="odd">
<td ><p>可見</p></td>
<td ><p>讀取/寫入</p></td>
<td ><p>傳回或設定值，這個值表示物件是否為可見或隱藏。</p></td>
</tr>
<tr class="even">
<td ><p>寬度</p></td>
<td ><p>讀取/寫入</p></td>
<td ><p>傳回或設定物件的寬度。</p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll;</dt><dt>Oleaut32.dll</dt> </dl> |



 

 
