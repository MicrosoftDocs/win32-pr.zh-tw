---
title: 'Rebar 控制項樣式 (CommCtrl .h) '
description: 除了標準視窗樣式之外，Rebar 控制項還支援各種控制項樣式。
ms.assetid: 9690a4bd-51bd-4df9-8988-7da3ece7899f
topic_type:
- apiref
api_name:
- RBS_AUTOSIZE
- RBS_BANDBORDERS
- RBS_DBLCLKTOGGLE
- RBS_FIXEDORDER
- RBS_REGISTERDROP
- RBS_TOOLTIPS
- RBS_VARHEIGHT
- RBS_VERTICALGRIPPER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e40a2f93820391d0c2b928c67784157c1f58d7995d42c51df5373d642bd796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078522"
---
# <a name="rebar-control-styles"></a>Rebar 控制項樣式

除了標準視窗樣式之外，Rebar 控制項還支援各種控制項樣式。



| 常數                                                                                                                                                                        | 描述                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RBS_AUTOSIZE"></span><span id="rbs_autosize"></span><dl> <dt>**RBS 自動 \_ 調整**</dt> </dl>                      | [版本 4.71](common-control-versions.md)。 當控制項的大小或位置變更時，Rebar 控制項將會自動變更群組的版面配置。 當發生這種情況時，將會傳送 [RBN \_ AUTOSIZE](rbn-autosize.md) 通知。<br/>                                                                                              |
| <span id="RBS_BANDBORDERS"></span><span id="rbs_bandborders"></span><dl> <dt>**RBS \_ BANDBORDERS**</dt> </dl>             | [版本 4.71](common-control-versions.md)。 Rebar 控制項會顯示窄行以分隔連續的群組。<br/>                                                                                                                                                                                                                                 |
| <span id="RBS_DBLCLKTOGGLE"></span><span id="rbs_dblclktoggle"></span><dl> <dt>**RBS \_ DBLCLKTOGGLE**</dt> </dl>          | [版本 4.71](common-control-versions.md)。 當使用者按兩下此寬線時，Rebar 波段會切換其最大化或最小化的狀態。 如果沒有這種樣式，當使用者按一下此寬線時，就會切換最大化或最小化的狀態。<br/>                                                                                          |
| <span id="RBS_FIXEDORDER"></span><span id="rbs_fixedorder"></span><dl> <dt>**RBS \_ FIXEDORDER**</dt> </dl>                | [版本 4.70](common-control-versions.md)。 Rebar 控制項一律會以相同的順序顯示群組。 您可以將多個群組移至不同的資料列，但帶狀順序是靜態的。<br/>                                                                                                                                                                      |
| <span id="RBS_REGISTERDROP"></span><span id="rbs_registerdrop"></span><dl> <dt>**RBS \_ REGISTERDROP**</dt> </dl>          | [版本 4.71](common-control-versions.md)。 當物件拖曳到控制項中的波段上方時，Rebar 控制項會產生 [RBN 的 \_ GETOBJECT](rbn-getobject.md) 通知代碼。 若要接收 RBN 的 \_ GETOBJECT 通知，請呼叫 [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) 或 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize)來初始化 OLE。<br/> |
| <span id="RBS_TOOLTIPS"></span><span id="rbs_tooltips"></span><dl> <dt>**RBS \_ 工具提示**</dt> </dl>                      | [版本 4.71](common-control-versions.md)。 尚不支援。<br/>                                                                                                                                                                                                                                                                                  |
| <span id="RBS_VARHEIGHT"></span><span id="rbs_varheight"></span><dl> <dt>**RBS \_ VARHEIGHT**</dt> </dl>                   | [版本 4.71](common-control-versions.md)。 如果可能的話，Rebar 控制項會以最小的必要高度顯示群組。 如果沒有這個樣式，Rebar 控制項會使用最高可見寬線的高度來顯示所有的條紋，以判斷其他條紋的高度。<br/>                                                   |
| <span id="RBS_VERTICALGRIPPER"></span><span id="rbs_verticalgripper"></span><dl> <dt>**RBS \_ VERTICALGRIPPER**</dt> </dl> | [版本 4.71](common-control-versions.md)。 大小的底框將會垂直顯示，而不是在垂直 Rebar 控制項中以水準方式顯示。 如果沒有 [**CCS \_ 垂直**](common-control-styles.md) 樣式的 Rebar 控制項，則會忽略這個樣式。<br/>                                                                            |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

