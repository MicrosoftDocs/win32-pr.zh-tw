---
title: 'Tree-View 控制項專案狀態 (CommCtrl .h) '
description: 此區段會列出用來指出樹狀檢視控制項中專案狀態的專案狀態旗標。
ms.assetid: 5b11d575-6dfd-47a8-b959-b19aaeeca70e
topic_type:
- apiref
api_name:
- TVIS_BOLD
- TVIS_CUT
- TVIS_DROPHILITED
- TVIS_EXPANDED
- TVIS_EXPANDEDONCE
- TVIS_EXPANDPARTIAL
- TVIS_SELECTED
- TVIS_OVERLAYMASK
- TVIS_STATEIMAGEMASK
- TVIS_USERMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5adb0371e3796c5d512ff3582a5c65850dc6cf8261f138934d46640aa57bf28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045958"
---
# <a name="tree-view-control-item-states"></a>Tree-View 控制項專案狀態

此區段會列出用來指出樹狀檢視控制項中專案狀態的專案狀態旗標。



| 常數                                                                                                                                                                        | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <dt>**TVIS \_ 粗體**</dt> </dl>                               | 專案為粗體。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <dt>**TVIS \_ 剪下**</dt> </dl>                                  | 選取專案做為剪下和貼上作業的一部分。 <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <dt>**TVIS \_ DROPHILITED**</dt> </dl>          | 專案會選取為拖放目標。<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <dt>**展開的 TVIS \_**</dt> </dl>                   | 專案的子專案清單目前已展開;也就是說，可以看到子專案。 這個值只適用于父代專案。<br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <dt>**TVIS \_ EXPANDEDONCE**</dt> </dl>       | 專案的子專案清單至少已展開一次。 [Izdebski \_ ITEMEXPANDING](tvn-itemexpanding.md)和 [izdebski \_ ITEMEXPANDED](tvn-itemexpanded.md)通知碼不會針對已設定此狀態以回應 [**TVM \_ 展開**](tvm-expand.md)訊息的父專案產生。 使用 \_ \_ 具有 **TVM \_ EXPAND** 的 TVE 折迭和 TVE COLLAPSERESET 將會重設此狀態。 這個值只適用于父代專案。 <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <dt>**TVIS \_ EXPANDPARTIAL**</dt> </dl>    | **版本 4.70**。 部分擴充的樹狀檢視專案。 在此狀態下，部分（但不是全部）的子專案會顯示出來，而且會顯示父專案的加號。 <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <dt>**TVIS 已 \_ 選取**</dt> </dl>                   | 這個項目已選取。 其外觀取決於它是否具有焦點。 將會使用系統色彩來繪製專案以供選取。 <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <dt>**TVIS \_ OVERLAYMASK**</dt> </dl>          | 用來指定專案之重迭影像索引之位的遮罩。<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <dt>**TVIS \_ STATEIMAGEMASK**</dt> </dl> | 用來指定專案的狀態影像索引之位的遮罩。<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <dt>**TVIS \_ USERMASK**</dt> </dl>                   | 與 **TVIS \_ STATEIMAGEMASK** 相同。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a>備註

當您設定或抓取專案的重迭影像索引或狀態影像索引時，您必須在 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **stateMask** 成員中指定下列遮罩：

-   **TVIS \_ OVERLAYMASK**
-   **TVIS \_ STATEIMAGEMASK**
-   **TVIS \_ USERMASK**

這些值也可以用來遮罩不感興趣的狀態位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

 





