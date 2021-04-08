---
description: 下表中的值會指定影片輸出的實體連接器類型。
ms.assetid: 93e816fb-1b40-4865-9c0c-24d96c83fb7f
title: 'OPM 連接器類型旗標 (Opmapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a3b14f1ba677822ec48cc85118fec156919794a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691640"
---
# <a name="opm-connector-type-flags"></a>OPM 連接器類型旗標

下表中的值會指定影片輸出的實體連接器類型。



| 常數/值                                                                                                                                                                                                                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CONNECTOR_TYPE_OTHER"></span><span id="opm_connector_type_other"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ 其他**</dt> <dt>-1</dt> </dl>                                                                    | 表示不在此清單上的實體連接器類型。<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="OPM_CONNECTOR_TYPE_VGA"></span><span id="opm_connector_type_vga"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ VGA**</dt> <dt>0</dt> </dl>                                                                           | 視頻圖形陣列 (VGA) 連接器。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="OPM_CONNECTOR_TYPE_SVIDEO"></span><span id="opm_connector_type_svideo"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ SVIDEO**</dt> <dt>1</dt> </dl>                                                                  | S-視頻連接器。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="OPM_CONNECTOR_TYPE_COMPOSITE_VIDEO"></span><span id="opm_connector_type_composite_video"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ 複合 \_ 影片**</dt> <dt>2</dt> </dl>                                      | 複合視頻連接器。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="OPM_CONNECTOR_TYPE_COMPONENT_VIDEO"></span><span id="opm_connector_type_component_video"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ 元件 \_ 影片**</dt> <dt>3</dt> </dl>                                      | 元件影片連接器。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="OPM_CONNECTOR_TYPE_DVI"></span><span id="opm_connector_type_dvi"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ DVI**</dt> <dt>4</dt> </dl>                                                                           | 數位視訊介面 (DVI) 連接器。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="OPM_CONNECTOR_TYPE_HDMI"></span><span id="opm_connector_type_hdmi"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ HDMI**</dt> <dt>5</dt> </dl>                                                                        | 高定義多媒體介面 (HDMI) 連接器。<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="OPM_CONNECTOR_TYPE_LVDS"></span><span id="opm_connector_type_lvds"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ LVDS**</dt> <dt>6</dt> </dl>                                                                        | 低電壓差異信號 (LVDS) connector 或 MIPI 數位序列介面 (DSI) 。<br/> 使用 LVDS 或 MIPI 數位序列介面 (DSI) 介面的連接器，以在內部連接到顯示裝置。 圖形介面卡與顯示裝置之間的連線為永久、非卸載式，且無法供使用者存取。 應用程式不應啟用此連接器的 High-Bandwidth 數位內容保護 (HDCP) 。<br/> |
| <span id="OPM_CONNECTOR_TYPE_D_JPN"></span><span id="opm_connector_type_d_jpn"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ D \_ JPN**</dt> <dt>8</dt> </dl>                                                                    | 日文 D 連接器。  (符合 EIAJ RC-5237 標準的連接器。 ) <br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="OPM_CONNECTOR_TYPE_SDI"></span><span id="opm_connector_type_sdi"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ SDI**</dt> <dt>9</dt> </dl>                                                                           | SDI (序列數位影像) 連接器。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="OPM_CONNECTOR_TYPE_DISPLAYPORT_EXTERNAL"></span><span id="opm_connector_type_displayport_external"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ DISPLAYPORT \_ 外部**</dt> <dt>10</dt> </dl>                      | 連接至顯示器設備的顯示埠。<br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="OPM_CONNECTOR_TYPE_DISPLAYPORT_EMBEDDED"></span><span id="opm_connector_type_displayport_embedded"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ DISPLAYPORT \_ EMBEDDED**</dt> <dt>11</dt> </dl>                      | 內嵌的顯示埠，會在內部連接到顯示裝置。 也稱為 *整合* 式顯示埠。<br/> 應用程式不應針對內嵌顯示埠啟用 High-Bandwidth 數位內容保護 (HDCP) 。<br/>                                                                                                                                                                                                                         |
| <span id="OPM_CONNECTOR_TYPE_UDI_EXTERNAL"></span><span id="opm_connector_type_udi_external"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ UDI \_ 外部**</dt> <dt>12</dt> </dl>                                              |  (UDI) 的整合顯示介面，可從外部連接到顯示裝置。<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="OPM_CONNECTOR_TYPE_UDI_EMBEDDED"></span><span id="opm_connector_type_udi_embedded"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ UDI \_ EMBEDDED**</dt> <dt>13</dt> </dl>                                              | 在內部連接至顯示裝置的內嵌 UDI。 也稱為 *整合* 式 UDI。<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="OPM_CONNECTOR_TYPE_RESERVED"></span><span id="opm_connector_type_reserved"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ 保留**</dt> <dt>14</dt> </dl>                                                           | 保留供未來使用。<br/> 在 Windows 8.1 和更新版本中支援。<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="OPM_CONNECTOR_TYPE_MIRACAST"></span><span id="opm_connector_type_miracast"></span><dl> <dt>**OPM \_連接器 \_ 類型 \_ MIRACAST**</dt> <dt>15</dt> </dl>                                                           | Miracast 無線連接器。<br/> 在 Windows 8.1 和更新版本中支援。<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL"></span><span id="opm_copp_compatible_connector_type_internal"></span><dl> <dt>**OPM \_COPP \_ 相容的 \_ 連接器 \_ 類型 \_ 內部**</dt> <dt>0x80000000</dt> </dl> | 內部連接器。 圖形介面卡與顯示裝置之間的連接是永久性的，而且無法供使用者存取。 此旗標只能用於 *COPP 模擬模式*。 它可以與其他值結合。<br/>                                                                                                                                                                                                                                    |



## <a name="remarks"></a>備註

如果連接器是以 *內嵌* 或 *整合* 方式描述，則表示連接器為內部連接器。 這些連接器在列舉常數的名稱中有「內嵌」。

應用程式應該忽略 **OPM \_ COPP \_ 相容的 \_ 連接器 \_ 類型 \_ 內部** 旗標，並改為檢查常數名稱中有 "EMBEDDED" 的連接器類型。

除了 **OPM \_ COPP \_ 相容的 \_ 連接器 \_ 類型 \_ 內部** 以外，此處所列的值並非位旗標，因此無法合併。

其中某些值相當於 **COPP \_ ConnectorType** 列舉中的值，這些值是在認證的輸出保護通訊協定 (COPP) 中使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[OPM 列舉](opm-enumerations.md)
</dt> </dl>

 

 




