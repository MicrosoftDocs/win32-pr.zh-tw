---
title: IMsRdpClientAdvancedSettings PerformanceFlags 屬性
description: 指定可在伺服器上設定的一組功能，以改善效能。
ms.assetid: dbbc7c13-ad8a-461d-9d2e-c454bf4b9dea
ms.tgt_platform: multiple
keywords:
- PerformanceFlags 屬性遠端桌面服務
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，PerformanceFlags 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PerformanceFlags
- IMsRdpClientAdvancedSettings.get_PerformanceFlags
- IMsRdpClientAdvancedSettings.put_PerformanceFlags
- IMsRdpClientAdvancedSettings2.PerformanceFlags
- IMsRdpClientAdvancedSettings2.get_PerformanceFlags
- IMsRdpClientAdvancedSettings2.put_PerformanceFlags
- IMsRdpClientAdvancedSettings3.PerformanceFlags
- IMsRdpClientAdvancedSettings3.get_PerformanceFlags
- IMsRdpClientAdvancedSettings3.put_PerformanceFlags
- IMsRdpClientAdvancedSettings4.PerformanceFlags
- IMsRdpClientAdvancedSettings4.get_PerformanceFlags
- IMsRdpClientAdvancedSettings4.put_PerformanceFlags
- IMsRdpClientAdvancedSettings5.PerformanceFlags
- IMsRdpClientAdvancedSettings5.get_PerformanceFlags
- IMsRdpClientAdvancedSettings5.put_PerformanceFlags
- IMsRdpClientAdvancedSettings6.PerformanceFlags
- IMsRdpClientAdvancedSettings6.get_PerformanceFlags
- IMsRdpClientAdvancedSettings6.put_PerformanceFlags
- IMsRdpClientAdvancedSettings7.PerformanceFlags
- IMsRdpClientAdvancedSettings7.get_PerformanceFlags
- IMsRdpClientAdvancedSettings7.put_PerformanceFlags
- IMsRdpClientAdvancedSettings8.PerformanceFlags
- IMsRdpClientAdvancedSettings8.get_PerformanceFlags
- IMsRdpClientAdvancedSettings8.put_PerformanceFlags
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1731afc6d58cede5da055da8cacaf11c8712d3c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384301"
---
# <a name="imsrdpclientadvancedsettingsperformanceflags-property"></a>IMsRdpClientAdvancedSettings：:P erformanceFlags 屬性

指定可在伺服器上設定的一組功能，以改善效能。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PerformanceFlags(
  [in]  LONG DisableList = TS_PERF_DISABLE_NOTHING
);

HRESULT get_PerformanceFlags(
  [out] LONG *pDisableList
);
```



## <a name="property-value"></a>屬性值

新的旗標。 預設值為 0 (**TS \_ 效能 \_ 停用 \_ 任何** 專案。 ) 

<dt>

<span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>

<span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS \_效能 \_ 停用 \_ 任何** (0x00000000) 


</dt> <dd>

未停用任何功能。

</dd> <dt>

<span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>

<span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS \_效能 \_ 停用 \_ 壁紙** (0x00000001) 


</dt> <dd>

桌面上不會顯示壁紙。

</dd> <dt>

<span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>

<span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS \_效能 \_ 停用 \_ FULLWINDOWDRAG** (0x00000002) 


</dt> <dd>

全視窗拖曳已停用;移動視窗時只會顯示視窗大綱。

</dd> <dt>

<span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>

<span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS \_PERF \_ DISABLE \_ MENUANIMATIONS** (0x00000004) 


</dt> <dd>

功能表動畫已停用。

</dd> <dt>

<span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>

<span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS \_效能 \_ 停用 \_ 主題** (0x00000008) 


</dt> <dd>

主題已停用。

</dd> <dt>

<span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>

<span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS \_效能 \_ 啟用 \_ 增強的圖形** (0x00000010) 


</dt> <dd>

啟用增強的圖形。

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>

<span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS \_效能 \_ 停用資料 \_ 指標 \_ 陰影** (0x00000020) 


</dt> <dd>

沒有顯示資料指標的陰影。

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>

<span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS \_PERF \_ DISABLE \_ CURSORSETTINGS** (0x00000040) 


</dt> <dd>

資料指標閃爍已停用。

</dd> <dt>

<span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>

<span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS \_效能 \_ 啟用 \_ 字型 \_ 平滑** 處理 (0x00000080) 


</dt> <dd>

啟用字型平滑處理。

</dd> <dt>

<span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>

<span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS \_效能 \_ 啟用 \_ 桌上型電腦 \_ 組合** (0x00000100) 


</dt> <dd>

啟用桌面組合。

</dd> <dt>

<span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>

<span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS \_效能 \_ 預設 \_ NONPERFCLIENT \_ 設定** (0x40000000) 


</dt> <dd>

在內部針對不知道此設定的用戶端設定。

</dd> <dt>

<span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>

<span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS \_效能 \_ RESERVED1** (0x80000000) 


</dt> <dd>

由用戶端在內部保留和使用。

</dd> </dl>

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                        |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                  |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





