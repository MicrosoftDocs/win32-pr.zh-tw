---
description: OPM 狀態要求
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: OPM 狀態要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf7338fe1309feb49fd191e3f4a1a22f3639b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120173"
---
# <a name="opm-status-requests"></a>OPM 狀態要求

本節列出 [輸出保護管理員](output-protection-manager.md) (OPM) 可用的狀態要求。 若要傳送 OPM 狀態要求，請呼叫 [**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)。 針對每個要求，會列出下列資訊。



| 值             | 描述                                                                                                                                                           |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 要求 GUID | 識別要求。 將 [**OPM \_ GET \_ INFO \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)結構的 **guidSetting** 成員設定為等於此值。 |
| 輸入資料   | 指定如何解讀 [**OPM \_ 取得 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)結構中的 **abParameters** 陣列。                      |
| 輸出資料  | 指定如何在 [**OPM 所 \_ 要求的 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)結構中解讀 **abRequestedInformation** 陣列。         |



 

系統會定義下列狀態要求：



| 狀態要求                                                                                      | 描述                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OPM \_ 取得 \_ ACP \_ 和 \_ CGMSA \_ 信號**](opm-get-acp-and-cgmsa-signaling.md)                     | 傳回關於影片輸出的下列資訊：                                                                                               |
| [**OPM \_ 取得 \_ 實際 \_ 輸出 \_ 格式**](opm-get-actual-output-format.md)                            | 傳回透過連接器傳輸之視訊訊號的描述。                                                               |
| [**OPM \_ 取得 \_ 實際的 \_ 保護 \_ 層級**](opm-get-actual-protection-level.md)                      | 傳回所指定保護機制的全域保護層級。                                                                             |
| [**OPM \_ 取得 \_ 介面卡 \_ 匯流排 \_ 類型**](opm-get-adapter-bus-type.md)                                    | 傳回影片輸出所使用的 i/o 匯流排型別。                                                                                                 |
| [**OPM \_ 取得 \_ 編解碼器 \_ 資訊**](opm-get-codec-info.md)                                                 | 取得硬體編解碼器的業績值。                                                                                                             |
| [**OPM \_ 取得 \_ 已連線的 \_ HDCP \_ 裝置 \_ 資訊**](opm-get-connected-hdcp-device-information.md) | 取得連接至影片輸出 High-Bandwidth 數位內容保護 (HDCP) 裝置的相關資訊。 會傳回下列資訊： |
| [**OPM \_ 取得 \_ 連接器 \_ 類型**](opm-get-connector-type.md)                                         | 傳回影片輸出的實體接點類型。                                                                                              |
| [**OPM \_ 取得 \_ 目前的 \_ HDCP \_ SRM \_ 版本**](opm-get-current-hdcp-srm-version.md)                   | 傳回目前影片輸出所使用 (SRM) 的系統 renewability 訊息版本號碼。                                               |
| [**OPM \_ 取得 \_ DVI \_ 特性**](opm-get-dvi-characteristics.md)                               | 查詢數位視訊介面 (DVI) 連接器是否支援 DVI 1.1 版或更新版本。                                                          |
| [**OPM \_ 取得 \_ 輸出 \_ 識別碼**](opm-get-output-id.md)                                                   | 傳回與此影片輸出相關聯之監視的唯一識別碼。                                                                       |
| [**OPM \_ 取得 \_ 支援的 \_ 保護 \_ 類型**](opm-get-supported-protection-types.md)                | 傳回連接器所支援的保護機制清單。                                                                        |
| [**OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 層級**](opm-get-virtual-protection-level.md)                    | 傳回所指定保護機制的虛擬保護層級。                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[OPM 程式設計參考](opm-programming-reference.md)
</dt> <dt>

[輸出保護管理員](output-protection-manager.md)
</dt> </dl>

 

 



