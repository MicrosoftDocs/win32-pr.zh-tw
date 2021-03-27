---
description: 本節描述 IActiveDesktop 介面方法所使用的旗標。
title: 'IActiveDesktop 旗標 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d1a2f69-0730-4805-8b50-071332ff7070
api_name:
- AD_APPLY_ALL
- AD_APPLY_BUFFERED_REFRESH
- AD_APPLY_DYNAMICREFRESH
- AD_APPLY_FORCE
- AD_APPLY_HTMLGEN
- AD_APPLY_REFRESH
- AD_APPLY_SAVE
- COMP_ELEM_ALL
- COMP_ELEM_CHECKED
- COMP_ELEM_CURITEMSTATE
- COMP_ELEM_FRIENDLYNAME
- COMP_ELEM_NOSCROLL
- COMP_ELEM_ORIGINAL_CSI
- COMP_ELEM_POS_LEFT
- COMP_ELEM_POS_TOP
- COMP_ELEM_POS_ZINDEX
- COMP_ELEM_RESTORED_CSI
- COMP_ELEM_SIZE_HEIGHT
- COMP_ELEM_SIZE_WIDTH
- COMP_ELEM_SOURCE
- COMP_ELEM_TYPE
- COMP_TYPE_CFHTML
- COMP_TYPE_CONTROL
- COMP_TYPE_HTMLDOC
- COMP_TYPE_MAX
- COMP_TYPE_PICTURE
- COMP_TYPE_WEBSITE
- COMPONENT_TOP
- WPSTYLE_CENTER
- WPSTYLE_MAX
- WPSTYLE_STRETCH
- WPSTYLE_TILE
- WPSTYLE_SPAN
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dae164c696ae54963f802a6ddd5cb1f6862b2f14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974837"
---
# <a name="iactivedesktop-flags"></a>IActiveDesktop 旗標

本節描述 [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) 介面方法所使用的旗標。

<dl> <dt>

<span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD \_ \_ 全部套用**
</dt> <dd> <dl> <dt>



* * * * AD \_ apply \_ SAVE * * * *、* * * * ad apply \_ \_ HTMLGEN * * * * 和 * * * * ad \_ apply REFRESH * * * \_ * 值的匯總。


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD 套用緩衝的重新整理 \_ \_ \_**
</dt> <dd> <dl> <dt>



啟動計時器，並將在該時間間隔內使用此旗標所做的所有重新整理要求匯總成單一重新整理。 此間隔設定為5秒。 At the end of the interval, or if a refresh is requested during the interval without an ****AD\_APPLY\_BUFFERED\_REFRESH**** flag, the refresh is made and the timer is stopped. 此旗標必須與 * * * * AD \_ APPLY REFRESH * * * 旗標合併 \_ 。


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD \_ APPLY \_ DYNAMICREFRESH**
</dt> <dd> <dl> <dt>



[版本 5.0](versions.md)。 使用動態 HTML，只重新整理自上次重新整理之後變更的專案，而不是整個桌面。


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD \_ APPLY \_ FORCE**
</dt> <dd> <dl> <dt>



強制 Active Desktop 變更。


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD \_ APPLY \_ HTMLGEN**
</dt> <dd> <dl> <dt>



重新產生桌面 HTML 檔案。


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD \_ APPLY \_ REFRESH**
</dt> <dd> <dl> <dt>



重新整理桌面專案。


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD \_ 套用 \_ 儲存**
</dt> <dd> <dl> <dt>



儲存桌面專案。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP \_ ELEM \_ ALL**
</dt> <dd> <dl> <dt>



複合 \_ ELEM 值的匯總 \_ \* 。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**\_ \_ 已檢查的複合 ELEM**
</dt> <dd> <dl> <dt>



已核取此專案。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP \_ ELEM \_ CURITEMSTATE**
</dt> <dd> <dl> <dt>



桌面專案的目前狀態。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP \_ ELEM \_ FRIENDLYNAME**
</dt> <dd> <dl> <dt>



專案的易記名稱。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP \_ ELEM \_ NOSCROLL**
</dt> <dd> <dl> <dt>



專案不可滾動。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP \_ ELEM \_ 原始 \_ CSI**
</dt> <dd> <dl> <dt>



原始桌面專案狀態資訊。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP \_ ELEM \_ POS \_ 左方**
</dt> <dd> <dl> <dt>



專案的水準位置。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP \_ ELEM \_ POS \_ TOP**
</dt> <dd> <dl> <dt>



專案的垂直位置。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP \_ ELEM \_ POS \_ ZINDEX**
</dt> <dd> <dl> <dt>



專案的 z-索引。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP \_ ELEM \_ 還原的 \_ CSI**
</dt> <dd> <dl> <dt>



還原的桌面專案狀態資訊。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**COMP \_ ELEM \_ 大小 \_ 高度**
</dt> <dd> <dl> <dt>



項目的高度。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**COMP \_ ELEM \_ 大小 \_ 寬度**
</dt> <dd> <dl> <dt>



項目的寬度。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**COMP \_ ELEM \_ 來源**
</dt> <dd> <dl> <dt>



專案的原始來源。


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**COMP \_ ELEM \_ 類型**
</dt> <dd> <dl> <dt>



項目類型。


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**複合 \_ 類型 \_ CFHTML**
</dt> <dd> <dl> <dt>



壓縮格式的 HTML。


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**COMP \_ 類型 \_ 控制項**
</dt> <dd> <dl> <dt>



專案是控制項。


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**複合 \_ 類型 \_ HTMLDOC**
</dt> <dd> <dl> <dt>



專案是 HTML 檔案。 只有在絕對必要時，才應該使用此旗標。 它會讓 HTML 檔案逐字插入 htt 檔案，用來控制桌面的版面配置。 For most cases, you should use the ****COMP\_TYPE\_WEBSITE**** flag to add items to the desktop.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**\_ \_ 最大的複合類型**
</dt> <dd> <dl> <dt>



複合類型旗標的最大值 \_ \_ \* 。


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**複合 \_ 類型 \_ 圖片**
</dt> <dd> <dl> <dt>



專案是一張圖片。


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**COMP \_ 類型 \_ 網站**
</dt> <dd> <dl> <dt>



專案是網站。


</dt> </dl> </dd> <dt>

<span id="COMPONENT_TOP"></span><span id="component_top"></span>**元件 \_ TOP**
</dt> <dd> <dl> <dt>



Z 順序值，表示專案位於頂端。


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**WPSTYLE \_ 中心**
</dt> <dd> <dl> <dt>



背景圖樣的中心。


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE \_ MAX**
</dt> <dd> <dl> <dt>



WPSTYLE 旗標的最大值 \_ \* 。


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE \_ STRETCH**
</dt> <dd> <dl> <dt>



背景圖樣會伸展以容納整個螢幕。


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**WPSTYLE \_ 圖格**
</dt> <dd> <dl> <dt>



背景圖樣會並排顯示。


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**WPSTYLE \_ 範圍**
</dt> <dd> <dl> <dt>



**Windows 8 和更新版本**：背景圖樣橫跨多個監視器。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
