---
description: 下列結構適用于輸出保護管理員 (OPM) 。
ms.assetid: 676a60ca-393e-4b5d-89d3-50cf4b771492
title: OPM 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35d72c5a5301dbc07b990aa4076f14fc221a1fde6af9c81e1f4a37fb424e24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737645"
---
# <a name="opm-structures"></a>OPM 結構

下列結構適用于 [輸出保護管理員](output-protection-manager.md) (OPM) 。



| 結構                                                                                              | Description                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GRL \_ 標頭**](grl-header.md)                                                                      | 包含 (GRL) 標頭的全域撤銷清單。                                                                                                          |
| [**MF \_ 簽章**](mf-signature.md)                                                                  | 包含 (GRL) 簽章的全域撤銷清單。                                                                                                         |
| [**OPM \_ ACP \_ 和 \_ CGMSA \_ 信號**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)                                 | 包含來自 [**OPM \_ GET \_ ACP \_ 和 \_ CGMSA \_ 信號**](opm-get-acp-and-cgmsa-signaling.md) 查詢的結果。                                         |
| [**OPM \_ 實際 \_ 輸出 \_ 格式**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)                                        | 包含 OPM 取得輸出保護管理員中 [**\_ \_ 實際 \_ 輸出 \_ 格式**](opm-get-actual-output-format.md) 查詢的結果， (OPM) 。               |
| [**OPM \_ 設定 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)                                         | 包含 OPM 或認證的輸出保護管理員 (COPP) 命令。                                                                                     |
| [**OPM \_ 連線的 \_ HDCP \_ 裝置 \_ 資訊**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)             | 包含 [**OPM \_ 取得 \_ CONNECTED \_ HDCP \_ 裝置 \_ 資訊**](opm-get-connected-hdcp-device-information.md) 查詢的結果。                     |
| [**OPM \_ COPP \_ 相容的 \_ GET \_ INFO \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_copp_compatible_get_info_parameters)        | 包含 [**IOPMVideoOutput：： COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) 方法的參數。 |
| [**OPM \_ 加密的 \_ 初始化 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters)          | 包含 OPM 會話的初始化參數。                                                                                                     |
| [**OPM \_ 取得 \_ 編解碼器 \_ 資訊 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)                           | 包含 [**OPM \_ 取得 \_ 編解碼器 \_ 資訊**](opm-get-codec-info.md) 查詢的結果。                                                                     |
| [**OPM \_ 取得 \_ 編解碼器 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)                             | 包含 [**OPM \_ 取得 \_ 編解碼器 \_ 資訊**](opm-get-codec-info.md) 命令的資訊。                                                                  |
| [**OPM \_ 取得 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)                                          | 包含 [**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) 方法的參數。                             |
| [**OPM \_ HDCP \_ 金鑰 \_ 選取 \_ 向量**](/windows/desktop/api/opmapi/ns-opmapi-opm_hdcp_key_selection_vector)                             | 包含 High-Bandwidth 數位內容保護 (HDCP) 接收器 (KSV) 的索引鍵選取向量。                                                   |
| [**OPM \_ OMAC**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_omac)                                                                          | 包含 OPM 訊息的訊息驗證碼 (MAC) 。                                                                                           |
| [**OPM \_ 輸出 \_ 識別碼 \_ 資料**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)                                                    | 包含 [**OPM \_ 取得 \_ 輸出 \_ 識別碼**](opm-get-output-id.md) 狀態要求的結果。                                                              |
| [**OPM \_ 隨機 \_ 數位**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number)                                                       | 包含與 OPM 搭配使用的128位亂數字。                                                                                                         |
| [**OPM \_ 要求的 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)                                       | 包含 OPM 狀態要求的結果。                                                                                                              |
| [**OPM \_ SET \_ ACP \_ 和 \_ CGMSA \_ 信號 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) | 包含 OPM 中 [**OPM \_ SET \_ ACP \_ 和 \_ CGMSA \_ 信號**](opm-set-acp-and-cgmsa-signaling.md) 命令的資訊。                               |
| [**OPM \_ 設定 \_ HDCP \_ SRM \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)                                 | 包含 [**OPM \_ SET \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) 命令的參數。                                                                       |
| [**OPM \_ SET \_ 保護 \_ 等級 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)                 | 在 OPM 中包含 [OPM \_ SET \_ PROTECTION \_ LEVEL](opm-set-protection-level.md) 命令的資料。                                                          |
| [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                         | 包含 OPM 狀態要求的結果。                                                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[OPM 程式設計參考](opm-programming-reference.md)
</dt> <dt>

[輸出保護管理員](output-protection-manager.md)
</dt> </dl>

 

 



