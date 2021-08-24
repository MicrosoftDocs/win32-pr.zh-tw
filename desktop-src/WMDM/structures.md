---
title: WMDM 結構
description: 本文包含 Windows 媒體裝置管理員（例如 _BITMAPINFOHEADER 和 MTP_COMMAND_DATA_IN）所定義之結構的相關參考文章。
ms.assetid: 3068359f-5ac0-41e0-a09b-283b439527a0
keywords:
- Windows媒體裝置管理員，結構
- 裝置管理員，結構
- 程式設計參考，結構
- Windows 媒體裝置管理員、結構的參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd0048a7cf3b87f09bb46ef6f6db74531b4b67a7364acd28099feed04bb8dec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865538"
---
# <a name="wmdm-structures"></a>WMDM 結構

Windows媒體裝置管理員定義下列結構。



| 結構                                                   | 描述                                                                                                                                                                                                                                              |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)             | 定義影片框架的格式。                                                                                                                                                                                                                       |
| [**\_ \_ 中的 MTP 命令資料 \_**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_in)       | 包含媒體傳輸通訊協定 (MTP) 使用 [**IWMDMDevice3：:D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) 方法傳送至裝置的自訂命令。                                                                           |
| [**MTP \_ 命令 \_ 資料 \_ 輸出**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_out)     | 包含媒體傳輸通訊協定 (設備磁碟機所填滿的 MTP) 回應。                                                                                                                                                                  |
| [**OPAQUECOMMAND**](opaquecommand.md)                      | 包含命令的資料，這些命令會透過 Windows 媒體裝置管理員傳遞至裝置，但不能透過 Windows 媒體裝置管理員來處理。                                                                                       |
| [**\_VIDEOINFOHEADER**](-videoinfoheader.md)               | 定義影片資料流程的格式。                                                                                                                                                                                                                    |
| [**\_WAVEFORMATEX**](-waveformatex.md)                     | 定義波形音訊資料的格式。                                                                                                                                                                                                               |
| [**WMDM \_ 格式 \_ 功能**](wmdm-format-capability.md)  | 描述特定格式之裝置的功能。 此結構在 [**WMDM \_ \_ 配置**](wmdm-prop-config.md) 結構的陣列中包含一組屬性設定。                                                       |
| [**WMDM \_ \_ 配置設定**](wmdm-prop-config.md)              | 針對特定格式，在裝置支援的所有屬性上描述一組相容的屬性值。 此結構在 [**WMDM 屬性 \_ \_ DESC**](wmdm-prop-desc.md) 結構的陣列中包含許多屬性描述。 |
| [**WMDM 的一種 \_ \_ DESC**](wmdm-prop-desc.md)                  | 描述特定屬性設定中的有效屬性值。                                                                                                                                                                             |
| [**WMDM 的 \_ 主張 \_ 值 \_ 列舉**](wmdm-prop-values-enum.md)   | 針對特定屬性設定中的特定屬性，包含有效值的列舉集合。                                                                                                                                             |
| [**WMDM \_ 的 \_ 值 \_ 範圍**](wmdm-prop-values-range.md) | 描述特定屬性設定中特定屬性的有效值範圍。                                                                                                                                                        |
| [**WMDMDATETIME**](wmdmdatetime.md)                        | 包含日期和時間。                                                                                                                                                                                                                                |
| [**WMDMID**](wmdmid.md)                                    | 描述序號和群組識別碼。                                                                                                                                                                                                                  |
| [**WMDMMetadataView**](wmdmmetadataview.md)                | 定義元資料檢視。                                                                                                                                                                                                                               |
| [**WMDMRIGHTS**](wmdmrights.md)                            | 描述內容使用權利。                                                                                                                                                                                                                            |
| [**WMFILECAPABILITIES**](wmfilecapabilities.md)            | 描述 MIME 類型。                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

 




