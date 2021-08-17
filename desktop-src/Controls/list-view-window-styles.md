---
title: 'List-View 視窗樣式 (CommCtrl .h) '
description: 下列視窗樣式是清單視圖控制項的特定樣式。
ms.assetid: 8b57239b-112e-4fb6-b394-15501bd3f5b3
topic_type:
- apiref
api_name:
- LVS_ALIGNLEFT
- LVS_ALIGNMASK
- LVS_ALIGNTOP
- LVS_AUTOARRANGE
- LVS_EDITLABELS
- LVS_ICON
- LVS_LIST
- LVS_NOCOLUMNHEADER
- LVS_NOLABELWRAP
- LVS_NOSCROLL
- LVS_NOSORTHEADER
- LVS_OWNERDATA
- LVS_OWNERDRAWFIXED
- LVS_REPORT
- LVS_SHAREIMAGELISTS
- LVS_SHOWSELALWAYS
- LVS_SINGLESEL
- LVS_SMALLICON
- LVS_SORTASCENDING
- LVS_SORTDESCENDING
- LVS_TYPEMASK
- LVS_TYPESTYLEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e326f4508d08f1052747e64ea5eba184f45f7e73a1cb55539255a27fd8c8c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412023"
---
# <a name="list-view-window-styles"></a>List-View 視窗樣式

下列視窗樣式是清單視圖控制項的特定樣式。



| 常數                                                                                                                                                                        | 描述                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVS_ALIGNLEFT"></span><span id="lvs_alignleft"></span><dl> <dt>**LVS) \_ ALIGNLEFT**</dt> </dl>                   | 專案會以圖示和小型圖示視圖靠左對齊。 <br/>                                                                                                                                                                                                                                                                                             |
| <span id="LVS_ALIGNMASK"></span><span id="lvs_alignmask"></span><dl> <dt>**LVS) \_ ALIGNMASK**</dt> </dl>                   | 控制項目前的對齊方式。 <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="LVS_ALIGNTOP"></span><span id="lvs_aligntop"></span><dl> <dt>**LVS) \_ ALIGNTOP**</dt> </dl>                      | 專案會與清單視圖控制項頂端的圖示和小型圖示視圖對齊。 <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_AUTOARRANGE"></span><span id="lvs_autoarrange"></span><dl> <dt>**LVS) \_ AUTOARRANGE**</dt> </dl>             | 圖示會自動以圖示和小型圖示視圖的形式保持排列。 <br/>                                                                                                                                                                                                                                                                              |
| <span id="LVS_EDITLABELS"></span><span id="lvs_editlabels"></span><dl> <dt>**LVS) \_ EDITLABELS**</dt> </dl>                | 專案文字可以就地編輯。 父視窗必須處理 [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) 通知碼。 <br/>                                                                                                                                                                                                               |
| <span id="LVS_ICON"></span><span id="lvs_icon"></span><dl> <dt>**LVS) \_ 圖示**</dt> </dl>                                  | 此樣式會指定圖示視圖。 <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_LIST"></span><span id="lvs_list"></span><dl> <dt>**LVS) \_ 清單**</dt> </dl>                                  | 此樣式會指定清單視圖。 <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_NOCOLUMNHEADER"></span><span id="lvs_nocolumnheader"></span><dl> <dt>**LVS) \_ NOCOLUMNHEADER**</dt> </dl>    | 欄位標題不會顯示在報表檢視中。 依預設，資料行在報表檢視中有標題。 <br/>                                                                                                                                                                                                                                               |
| <span id="LVS_NOLABELWRAP"></span><span id="lvs_nolabelwrap"></span><dl> <dt>**LVS) \_ NOLABELWRAP**</dt> </dl>             | 專案文字會顯示在圖示視圖的單一行上。 依預設，專案文字可能會在圖示視圖中換行。 <br/>                                                                                                                                                                                                                                              |
| <span id="LVS_NOSCROLL"></span><span id="lvs_noscroll"></span><dl> <dt>**LVS) \_ NOSCROLL**</dt> </dl>                      | 滾動已停用。 所有專案都必須在工作區中。 此樣式與 **lvs) \_ 清單** 或 **lvs) \_ 報表** 樣式不相容。 如需進一步討論，請參閱知識庫文章 Q137520。 <br/>                                                                                                                                      |
| <span id="LVS_NOSORTHEADER"></span><span id="lvs_nosortheader"></span><dl> <dt>**LVS) \_ NOSORTHEADER**</dt> </dl>          | 欄標題的運作方式不像按鈕。 如果按一下報表檢視中的資料行標頭不會執行動作（例如排序），就可以使用這個樣式。 <br/>                                                                                                                                                                                       |
| <span id="LVS_OWNERDATA"></span><span id="lvs_ownerdata"></span><dl> <dt>**LVS) \_ OWNERDATA**</dt> </dl>                   | [版本 4.70](common-control-versions.md)。 此樣式會指定虛擬清單視圖控制項。 如需此清單控制項樣式的詳細資訊，請參閱 [關於 List-View 控制項](list-view-controls-overview.md)。 <br/>                                                                                                                             |
| <span id="LVS_OWNERDRAWFIXED"></span><span id="lvs_ownerdrawfixed"></span><dl> <dt>**LVS) \_ OWNERDRAWFIXED**</dt> </dl>    | 擁有者視窗可以在報表檢視中繪製專案。 清單視圖控制項會傳送 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息來繪製每個專案，而不會為每個子專案傳送個別的訊息。 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的 **iItemData** 成員包含所指定清單視圖專案的專案資料。 <br/> |
| <span id="LVS_REPORT"></span><span id="lvs_report"></span><dl> <dt>**LVS) \_ 報表**</dt> </dl>                            | 此樣式會指定報表檢視。 搭配使用 LVS) \_ 報表樣式與清單視圖控制項時，第一個資料行一律為靠左對齊。 您無法使用 LVCFMT \_ 許可權來變更這種對齊方式。 如需資料行對齊的詳細資訊，請參閱 [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) 。 <br/>                                                                      |
| <span id="LVS_SHAREIMAGELISTS"></span><span id="lvs_shareimagelists"></span><dl> <dt>**LVS) \_ SHAREIMAGELISTS**</dt> </dl> | 當控制項損毀時，不會刪除影像清單。 此樣式可讓您使用具有多個清單視圖控制項的相同影像清單。 <br/>                                                                                                                                                                                          |
| <span id="LVS_SHOWSELALWAYS"></span><span id="lvs_showselalways"></span><dl> <dt>**LVS) \_ SHOWSELALWAYS**</dt> </dl>       | 如果有的話，一律會顯示選取範圍（如果有的話），即使控制項沒有焦點也一樣。 <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SINGLESEL"></span><span id="lvs_singlesel"></span><dl> <dt>**LVS) \_ SINGLESEL**</dt> </dl>                   | 一次只能選取一個專案。 依預設，您可以選取多個專案。 <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SMALLICON"></span><span id="lvs_smallicon"></span><dl> <dt>**LVS) \_ SMALLICON**</dt> </dl>                   | 此樣式會指定小圖示視圖。 <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="LVS_SORTASCENDING"></span><span id="lvs_sortascending"></span><dl> <dt>**LVS) \_ SORTASCENDING**</dt> </dl>       | 專案索引會根據專案文字以遞增順序排序。 <br/>                                                                                                                                                                                                                                                                                  |
| <span id="LVS_SORTDESCENDING"></span><span id="lvs_sortdescending"></span><dl> <dt>**LVS) \_ SORTDESCENDING**</dt> </dl>    | 專案索引會根據專案文字以遞減順序排序。 <br/>                                                                                                                                                                                                                                                                                 |
| <span id="LVS_TYPEMASK"></span><span id="lvs_typemask"></span><dl> <dt>**LVS) \_ TYPEMASK**</dt> </dl>                      | 判斷控制項目前的視窗樣式。 <br/>                                                                                                                                                                                                                                                                                                  |
| <span id="LVS_TYPESTYLEMASK"></span><span id="lvs_typestylemask"></span><dl> <dt>**LVS) \_ TYPESTYLEMASK**</dt> </dl>       | 決定控制專案對齊和標頭外觀和行為的視窗樣式。 <br/>                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>備註

針對 **lvs) \_ SORTASCENDING** 和 **lvs) \_ SORTDESCENDING** 樣式，專案索引會以遞增或遞減順序的專案文字為基礎來排序。 因為 **lvs) \_ 清單** 和 **lvs) \_ 報表** 視圖會以與其索引相同的順序顯示專案，所以使用者可以立即看見排序結果。 **Lvs) \_ 圖示** 和 **lvs) \_ SMALLICON** views 不會使用專案索引來決定圖示的位置。 使用這些視圖時，使用者看不到排序的結果。

您可以使用 **lvs) \_ TYPEMASK** mask 來隔離對應至目前 view 的視窗樣式： **lvs) \_ 圖示**、 **lvs) \_ 清單**、 **lvs) \_ 報表** 和 **lvs) \_ SMALLICON**。

您可以使用 **lvs) \_ ALIGNMASK** mask 來隔離指定專案對齊方式的視窗樣式： **lvs) \_ ALIGNLEFT** 和 **lvs) \_ ALIGNTOP**。

您可以使用 **lvs) \_ TYPESTYLEMASK** mask 來隔離控制專案對齊 (**lvs) \_ ALIGNLEFT** 和 **lvs) \_ ALIGNTOP**) 的視窗樣式，以及控制標頭外觀和行為 (**lvs) \_ NOCOLUMNHEADER** 和 **lvs) \_ NOSORTHEADER**) 的視窗樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[清單-視圖樣式和視圖](list-view-controls-overview.md)
</dt> </dl>

 

 





