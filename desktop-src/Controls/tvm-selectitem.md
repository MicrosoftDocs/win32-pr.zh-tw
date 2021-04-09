---
title: 'TVM_SELECTITEM 訊息 (Commctrl .h) '
description: 選取指定的樹狀檢視專案、將專案滾動到視圖，或是以用來表示拖放作業目標的樣式來重繪專案。
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- TVM_SELECTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843244"
---
# <a name="tvm_selectitem-message"></a>TVM \_ SELECTITEM 訊息

選取指定的樹狀檢視專案、將專案滾動到視圖，或是以用來表示拖放作業目標的樣式來重繪專案。 您可以明確地傳送此訊息，或使用 [**treeview \_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select)、 [**treeview \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)或 [**treeview \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

動作旗標。 這個參數可以是下列其中一個值：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt><strong>TVGN_CARET</strong></dt> </dl></td>
<td>將選取範圍設定為指定的專案。 樹狀檢視控制項的父視窗會接收 <a href="tvn-selchanging.md">TVN_SELCHANGING</a> 並 <a href="tvn-selchanged.md">TVN_SELCHANGED</a> 通知碼。 <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt><strong>TVGN_DROPHILITE</strong></dt> </dl></td>
<td>以用來表示拖放作業目標的樣式來重繪指定的專案。<br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </dl></td>
<td>確定指定的專案是可見的，如果可能的話，會將它顯示在控制項視窗的頂端。 樹狀檢視控制項會在視窗中顯示任意數量的專案。 如果指定的專案位於控制項階層專案的底部附近，它可能不會成為第一個可見的專案，視視窗中容納的專案數目而定。<br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </dl></td>
<td>選取單一專案時，會確保 treeview 不會展開該專案的子系。 只有搭配 TVGN_CARET 旗標使用時才有效。 <br/>
<blockquote>
[!Note]<br />
若要使用此旗標，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 <a href="cookbook-overview.md">啟用視覺化樣式</a>。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

專案的控制碼。 如果 *lParam* 為 **Null**，則控制項設定為沒有選取的專案。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如果指定的專案是折迭父項目的子系，則會展開父代的子專案清單，以顯示指定的專案。 在此情況下，控制項的父視窗會收到 [izdebski \_ ITEMEXPANDING](tvn-itemexpanding.md) 和 [izdebski \_ ITEMEXPANDED](tvn-itemexpanded.md) 通知碼。

使用 [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)宏相當於將 *wParam* 設定為 TVGN 插入號值的 **TVM \_ SelectItem** 訊息傳送 \_ 。 使用 [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget)宏相當於將 *wParam* 設定為 TVGN DROPHILITE 值的 **TVM \_ SELECTITEM** 訊息傳送 \_ 。 使用 [**TreeView \_ SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible)相當於將 *wParam* 設定為 TVGN FIRSTVISIBLE 值的 **TVM \_ SELECTITEM** 訊息傳送 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





