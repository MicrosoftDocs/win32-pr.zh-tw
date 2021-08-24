---
title: 'TVM_GETNEXTITEM 訊息 (Commctrl .h) '
description: 抓取具有指定專案之指定關聯性的樹狀檢視專案。 您可以使用 TreeView GetNextItem 宏明確地傳送此訊息 \_ 。
ms.assetid: 505c713c-7728-4119-bc0e-482fe7e73193
keywords:
- TVM_GETNEXTITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETNEXTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dbbd39ca347bcf1084ddfaa46c997cc5c4e5dd4d52250136a230dd834ac836
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698678"
---
# <a name="tvm_getnextitem-message"></a>TVM \_ GETNEXTITEM 訊息

抓取具有指定專案之指定關聯性的樹狀檢視專案。 您可以使用 [**TreeView \_ GetNextItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定要取出之專案的旗標。 這個參數可以是下列其中一個值：



| 值                                                                                                                                                                              | 意義                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt>**TVGN \_ 插入號**</dt> </dl>                               | 抓取目前選取的專案。 您可以使用 [**TreeView \_ GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection) 宏來傳送此訊息。<br/>                                                                                                                                                                          |
| <span id="TVGN_CHILD"></span><span id="tvgn_child"></span><dl> <dt>**TVGN \_ 子系**</dt> </dl>                               | 抓取 *hitem* 參數所指定之專案的第一個子專案。 您可以使用 [**TreeView \_ system.windows.media.visualtreehelper.getchild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild) 宏來傳送此訊息。<br/>                                                                                                                                          |
| <span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt>**TVGN \_ DROPHILITE**</dt> </dl>                | 抓取做為拖放作業之目標的專案。 您可以使用 [**TreeView \_ GetDropHilight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight) 宏來傳送此訊息。<br/>                                                                                                                                         |
| <span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt>**TVGN \_ FIRSTVISIBLE**</dt> </dl>          | 抓取樹狀檢視視窗中可見的第一個專案。 您可以使用 [**TreeView \_ GetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) 宏來傳送此訊息。<br/>                                                                                                                                         |
| <span id="TVGN_LASTVISIBLE"></span><span id="tvgn_lastvisible"></span><dl> <dt>**TVGN \_ LASTVISIBLE**</dt> </dl>             | [版本 4.71](common-control-versions.md)。 抓取樹狀結構中最後展開的專案。 這不會取出樹狀檢視視窗中顯示的最後一個專案。 您可以使用 [**TreeView \_ GetLastVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible) 宏來傳送此訊息。<br/>                                            |
| <span id="TVGN_NEXT"></span><span id="tvgn_next"></span><dl> <dt>**TVGN \_ 下一步**</dt> </dl>                                  | 抓取下一個同級專案。 您可以使用 [**TreeView \_ GetNextSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling) 宏來傳送此訊息。<br/>                                                                                                                                                                            |
| <span id="TVGN_NEXTSELECTED"></span><span id="tvgn_nextselected"></span><dl> <dt>**TVGN \_ NEXTSELECTED**</dt> </dl>          | **WindowsVista 和更新版本。** 抓取下一個選取的專案。 您可以使用 [**TreeView \_ GetNextSelected**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected) 宏來傳送此訊息。<br/>                                                                                                                                            |
| <span id="TVGN_NEXTVISIBLE"></span><span id="tvgn_nextvisible"></span><dl> <dt>**TVGN \_ NEXTVISIBLE**</dt> </dl>             | 抓取位於指定專案後面的下一個可見專案。 指定的專案必須是可見的。 使用 [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) 訊息來判斷是否可以看到專案。 您可以使用 [**TreeView \_ GetNextVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible) 宏來傳送此訊息。<br/>   |
| <span id="TVGN_PARENT"></span><span id="tvgn_parent"></span><dl> <dt>**TVGN \_ 父系**</dt> </dl>                            | 抓取指定之專案的父系。 您可以使用 [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent) 宏來傳送此訊息。<br/>                                                                                                                                                                           |
| <span id="TVGN_PREVIOUS"></span><span id="tvgn_previous"></span><dl> <dt>**TVGN \_ 上一步**</dt> </dl>                      | 抓取上一個同級專案。 您可以使用 [**TreeView \_ GetPrevSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling) 宏來傳送此訊息。<br/>                                                                                                                                                                        |
| <span id="TVGN_PREVIOUSVISIBLE"></span><span id="tvgn_previousvisible"></span><dl> <dt>**TVGN \_ PREVIOUSVISIBLE**</dt> </dl> | 抓取指定專案之前的第一個可見專案。 指定的專案必須是可見的。 使用 [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) 訊息來判斷是否可以看到專案。 您可以使用 [**TreeView \_ GetPrevVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible) 宏來傳送此訊息。<br/> |
| <span id="TVGN_ROOT"></span><span id="tvgn_root"></span><dl> <dt>**TVGN \_ 根目錄**</dt> </dl>                                  | 抓取樹狀檢視控制項的最上層或第一個專案。 您可以使用 [**TreeView \_ GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot) 宏來傳送此訊息。 <br/>                                                                                                                                                       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

專案的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回專案的控制碼。 在大部分的情況下，訊息會傳回 **Null** 值以表示錯誤。 如需詳細資訊，請參閱＜備註＞一節。

## <a name="remarks"></a>備註

如果要抓取的專案是樹狀結構的根節點，此訊息將會傳回 **Null** 。 例如，如果您在 \_ 樹狀檢視根節點的第一個層級子系上，使用此訊息搭配 TVGN 父旗標，訊息將會傳回 **Null**。

您也可以使用下列其中一個相關宏：



|                                                               |
|---------------------------------------------------------------|
| [**TreeView \_ system.windows.media.visualtreehelper.getchild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)               |
| [**TreeView \_ GetDropHilight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)   |
| [**TreeView \_ GetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) |
| [**TreeView \_ GetLastVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)   |
| [**TreeView \_ GetNextSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)   |
| [**TreeView \_ GetNextVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)   |
| [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)             |
| [**TreeView \_ GetPrevSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)   |
| [**TreeView \_ GetPrevVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)   |
| [**TreeView \_ GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)                 |
| [**TreeView \_ GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





