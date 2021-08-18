---
description: 下表所列的旗標會指定圖形介面卡所使用的 i/o 匯流排類型。
ms.assetid: 6c8ec020-5f12-453b-bbeb-3baabb1ca213
title: 'OPM 匯流排類型旗標 (Opmapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4989a91c308a7dc82bb15e9cd577a6facd89a0a6de9a32f0ef95f400917ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972997"
---
# <a name="opm-bus-type-flags"></a>OPM 匯流排類型旗標

下表所列的旗標會指定圖形介面卡所使用的 i/o 匯流排類型。



| 常數/值                                                                                                                                                                                                                                                                                                                                                                                                      | 描述                                                                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_BUS_TYPE_OTHER"></span><span id="opm_bus_type_other"></span><dl> <dt>**OPM \_匯流排 \_ 類型 \_ 其他**</dt> <dt>0x00000000</dt> </dl>                                                                                                                                                                      | 指出此處所列類型以外的匯流排類型。<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="OPM_BUS_TYPE_PCI"></span><span id="opm_bus_type_pci"></span><dl> <dt>**OPM \_匯流排 \_ 類型 \_ PCI**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                                                            | PCI 匯流排。<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="OPM_BUS_TYPE_PCIX"></span><span id="opm_bus_type_pcix"></span><dl> <dt>**OPM \_匯流排 \_ 類型 \_ PCIX**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                                                         | PCI X 匯流排。<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="OPM_BUS_TYPE_PCIEXPRESS"></span><span id="opm_bus_type_pciexpress"></span><dl> <dt>**OPM \_匯流排 \_ 類型 \_ PCIEXPRESS**</dt> <dt>0x00000003</dt> </dl>                                                                                                                                                       | PCI Express 匯流排。<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="OPM_BUS_TYPE_AGP"></span><span id="opm_bus_type_agp"></span><dl> <dt>**OPM \_匯流排 \_ 類型 \_ AGP**</dt> <dt>0x00000004</dt> </dl>                                                                                                                                                                            | 高速圖形連接埠 (AGP) 匯流排。<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="opm_bus_implementation_modifier_inside_of_chipset"></span><dl> <dt>**OPM \_\_ \_ \_ \_ \_ 晶片0x00010000 內的匯流排執行修飾**</dt>詞 <dt></dt> </dl>                                                                      | 圖形介面卡的執行是在主機板晶片的北方 bridge 中。 此旗標表示資料永遠不會超出展開匯流排 (例如 PCI 或 AGP) 從主儲存體傳輸到圖形介面卡時。 <br/>                                                                                                                                     |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_chip"></span><dl> <dt>**OPM \_從 \_ \_ \_ \_ \_ \_ 主機板 \_ 到 \_ 晶片0x00020000 的匯流排執行修飾詞追蹤**</dt> <dt></dt> </dl>                            | 圖形介面卡會透過在主機板上進行追蹤，連接至主機板晶片的北方橋接器，而所有圖形介面卡的晶片 (整合電路) 會先焊接至主機板。 <br/>                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_socket"></span><dl> <dt>**OPM \_從 \_ \_ \_ \_ \_ \_ 主機板 \_ 到 \_ 通訊端0x00030000 的匯流排執行修飾詞追蹤**</dt> <dt></dt> </dl>                      | 圖形介面卡會透過在主機板上進行追蹤，連接至主機板晶片的北方橋接器，而所有圖形介面卡的晶片都會透過通訊端連接至主機板。<br/>                                                                                                                                                                               |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="opm_bus_implementation_modifier_daughter_board_connector"></span><dl> <dt>**OPM \_匯流排 \_ 執行 \_ 修飾詞 \_ 子 \_ 面板 \_ 連接器**</dt> <dt>0x00040000</dt> </dl>                                                 | 圖形介面卡透過 daughterboard 連接器連線至主機板。<br/>                                                                                                                                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="opm_bus_implementation_modifier_daughter_board_connector_inside_of_nuae"></span><dl> <dt>**OPM \_\_ \_ \_ \_ \_ \_ \_ \_ NUAE 0x00050000 內的匯流排執行修飾詞子面板連接器**</dt> <dt></dt> </dl> | 圖形介面卡透過 daughterboard 連接器連線至主機板，而圖形介面卡位於無法存取使用者的主機殼內。<br/>                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_NON_STANDARD"></span><span id="opm_bus_implementation_modifier_non_standard"></span><dl> <dt>**OPM \_匯流排 \_ 執行 \_ 修飾詞 \_ 非 \_ 標準**</dt> <dt>0x80000000</dt> </dl>                                                                                      | 非標準的修飾詞。 (選擇性。)<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="OPM_COPP_COMPATIBLE_BUS_TYPE_INTEGRATED"></span><span id="opm_copp_compatible_bus_type_integrated"></span><dl> <dt>**OPM \_COPP \_ 相容 \_ 匯流排 \_ 類型 \_ 整合**</dt>式的 <dt>0x80000000</dt> </dl>                                                                                                     | 整合式匯流排。 此旗標只能用於 COPP 模擬模式。 它指出在具有公用規格和標準連接器類型的擴充匯流排上，除非它是記憶體匯流排，否則圖形介面卡和電腦上其他子系統之間的命令和狀態信號無法使用。 此旗標可以與 **OPM \_ BUS \_ TYPE \_ Xxx** 旗標合併使用。<br/> |



## <a name="remarks"></a>備註

使用位 **or** 可以設定最多三個旗標。 從0x00 到0x04 範圍中的旗標 (**OPM \_ 匯流排 \_ 類型 \_ Xxx** ，) 提供基本匯流排類型。 範圍0x10000 到0x50000 的旗標 (**OPM \_ 匯流排 \_ 實 \_ 修飾詞 \_ Xxx**) 修改基本描述。 驅動程式會設定一個匯流排類型旗標，並可選擇性地設定為一個修飾詞旗標。 此外，驅動程式也可以選擇性地設定 **OPM \_ 匯流排 \_ 執行 \_ 修飾詞 \_ 非 \_ 標準** 旗標。

在 COPP 模擬模式中，驅動程式不會使用修飾詞旗標，但它可能會設定 **OPM \_ COPP \_ 相容 \_ 匯流排 \_ 類型 \_ 整合** 旗標。

OPM \_ BUG \_ 類型 \_ Xxxx 旗標和 **OPM \_ COPP \_ 相容 \_ 匯流排 \_ 類型 \_ 整合** 旗標相當於認證輸出保護通訊協定 (BusType) 中所使用的 [**COPP \_ COPP**](/windows/win32/api/dxva9typ/ne-dxva9typ-copp_bustype) 列舉值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[OPM 列舉](opm-enumerations.md)
</dt> </dl>

 

 
