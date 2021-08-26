---
title: 平面捲軸
description: 本節包含用來控制一般捲軸之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf1c1d49bf4b54d65adbe784d1e4da62adfe35c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466595"
---
# <a name="flat-scroll-bar"></a>平面捲軸

本節包含用來控制一般捲軸之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                    | 目錄                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [平面捲軸](flat-scroll-bars.md) | Microsoft Internet Explorer 4.0 推出了一個新的視覺技術，稱為「一般捲軸」。 功能上，一般捲軸的行為就像標準捲軸。 不同之處在于，您可以自訂其外觀，以比標準捲軸更大的範圍。<br/> |



 

### <a name="functions"></a>函式




| 主題 | 目錄 | 
|-------|----------|
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a> | 啟用或停用一或兩個平面捲軸方向按鈕。 如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> 函式。 <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a> | 取得平面捲軸的資訊。 如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> 函式。 <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a> | 取得平面捲軸的捲動方塊位置。 如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> 函式。 <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a> | 取得平面捲軸的屬性。 這個函數也可以用來判斷是否已針對此視窗呼叫 <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> 。 <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a> | 取得平面捲軸的屬性。 這個函數也可以用來判斷是否已針對此視窗呼叫 <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> 。<blockquote>[!Note]<br />這等同于 <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>。</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a> | 取得平面捲軸的捲軸範圍。 如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> 函式。 <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a> | 設定一般捲軸的資訊。 如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> 函式。 <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a> | 將 thumb 的目前位置設定為平面捲軸。 如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> 函式。 <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a> | 設定平面捲軸的屬性。 <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a> | 設定平面捲軸的捲軸範圍。 如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> 函式。 <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a> | 顯示或隱藏平面捲軸。 如果未針對視窗初始化一般捲軸，則此函式會呼叫標準 <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> 函式。 <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> | 初始化特定視窗的平面捲軸。 <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a> | 取消初始化特定視窗的平面捲軸。 指定的視窗將會還原為標準捲軸。 <br /> | 




 

 

 





