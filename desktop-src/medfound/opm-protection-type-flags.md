---
description: 下表中的旗標指定輸出保護管理員 (OPM) 的輸出保護機制。
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: 'OPM 保護類型旗標 (Opmapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc8b30a18f5c7bf68fb01775751aa56e1e619f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977803"
---
# <a name="opm-protection-type-flags"></a>OPM 保護類型旗標

下表中的旗標指定輸出保護管理員 (OPM) 的輸出保護機制。



| 常數/值                                                                                                                                                                                                                                                                                                     | Description                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <dt>**OPM \_保護 \_ 類型 \_ 其他**</dt> <dt>0x80000000</dt> </dl>                                                | 未知的保護機制。<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <dt>**OPM \_保護 \_ 類型 \_ NONE**</dt> <dt>0x00000000</dt> </dl>                                                   | 沒有防護機制。<br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <dt>**OPM \_保護 \_ 類型 \_ COPP \_ 相容的 \_ HDCP**</dt> <dt>0x00000001</dt> </dl> | High-Bandwidth 數位內容保護 (HDCP) 。 當模擬經認證的輸出保護通訊協定 (COPP) 時，會使用此旗標。 如需詳細資訊，請參閱＜備註＞。 OPM 語義不支援此旗標。<br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <dt>**OPM \_保護 \_ 類型 \_ ACP**</dt> <dt>0x00000002</dt> </dl>                                                      | 類比禁止複製 (ACP) 。<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <dt>**OPM \_保護 \_ 類型 \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>                                                | 複製世代管理系統—類比 (CGMS-A) 。<br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <dt>**OPM \_保護 \_ 類型 \_ HDCP**</dt> <dt>0x00000008</dt> </dl>                                                   | 觀看. 當 OPM 物件具有 OPM 語義時，會使用這個旗標。 COPP 語義不支援此功能。<br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <dt>**OPM \_保護 \_ 類型 \_ DPCP**</dt> <dt>0x00000010</dt> </dl>                                                   | DisplayPort 內容保護 (DPCP) 。<br/>                                                                                                                                                                           |



## <a name="remarks"></a>備註

下列 OPM 命令和狀態要求會使用這些旗標。

-   [OPM \_ SET \_ 保護 \_ 等級](opm-set-protection-level.md)
-   [OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 層級](opm-get-virtual-protection-level.md)
-   [OPM \_ 取得 \_ 實際的 \_ 保護 \_ 層級](opm-get-actual-protection-level.md)

### <a name="hdcp"></a>觀看

下列兩個旗標為 HDCP 定義。



| 值                                         | 描述                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| OPM \_ 保護 \_ 類型 \_ HDCP                   | 如果已使用 OPM 語義建立了 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 指標，請使用此旗標。                                                                        |
| OPM \_ 保護 \_ 類型 \_ COPP \_ 相容的 \_ HDCP | 如果已使用 COPP 語義建立了 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 指標，請使用此旗標。 此旗標對應于 \_ COPP 中的 COPP Set-protectiontype \_ HDCP 旗標。 |



 

這兩種模式 (OPM 語義和 COPP 語義) 支援適用于 HDCP 的下列作業：

-   使用 [OPM \_ SET \_ PROTECTION \_ LEVEL](opm-set-protection-level.md) 命令啟用或停用 HDCP。
-   使用 [OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 等級](opm-get-virtual-protection-level.md) 或 [OPM \_ 取得 \_ 實際的 \_ 保護 \_ 等級](opm-get-actual-protection-level.md) 狀態要求，以查詢是否已啟用 HDCP。

OPM 語義也支援下列各項：

-   HDCP 中繼器。 *Hdcp 中繼器* 是一種 hdcp 裝置，可以接收 hdcp 內容，也可以重新加密及傳輸相同的內容。
-   HDCP 撤銷。 如果已撤銷的 HDCP 裝置已附加至 OPM video 輸出，則影片輸出不會傳輸影片。 應用程式不需要剖析 HDCP 系統 renewability 訊息 (SRMs) 或判斷是否已撤銷輸出裝置。 如需詳細資訊，請參閱 [**OPM \_ SET \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) 命令。

使用 COPP 的語法時， [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 介面不支援 HDCP 中繼器。 此外，它也不會處理 HDCP 撤銷。 相反地，應用程式必須剖析 SRM，以判斷是否已撤銷 HDCP 裝置。

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

 

 




