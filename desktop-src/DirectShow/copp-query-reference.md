---
description: COPP 查詢參考
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: COPP 查詢參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41de36f3cdcc37a38e2ebc53caa7b6b37c204d9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025793"
---
# <a name="copp-query-reference"></a>COPP 查詢參考

本節說明經認證的輸出保護通訊協定所支援的狀態查詢 (COPP) 。 針對每個查詢，會列出用來定義查詢的 GUID，以及輸入資料和傳回資料。



| 查詢                   | GUID                                     |
|-------------------------|------------------------------------------|
| 匯流排資料                | **DXVA \_ COPPQueryBusData**               |
| 連接器類型          | **DXVA \_ COPPQueryConnectorType**         |
| 顯示資料            | **DXVA \_ COPPQueryDisplayData**           |
| HDCP 金鑰資料           | **DXVA \_ COPPQueryHDCPKeyData**           |
| 全域保護等級 | **DXVA \_ COPPQueryGlobalProtectionLevel** |
| 本機保護層級  | **DXVA \_ COPPQueryLocalProtectionLevel**  |
| 保護類型         | **DXVA \_ COPPQueryProtectionType**        |
| Signaling               | **DXVA \_ COPPQuerySignaling**             |



 

匯流排資料查詢

傳回圖形介面卡所使用的 i/o 匯流排型別。

-   **GUID**： DXVA \_ COPPQueryBusData
-   **輸入資料**：無。
-   傳回 **資料**：傳回 [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata)結構。 匯流排類型會以 **dwData** 成員的旗標形式傳回，作為 [**COPP \_ BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) 列舉的旗標。

連接器類型查詢

傳回實體接點型別。

-   **GUID**： DXVA \_ COPPQueryConnectorType
-   **輸入資料**：無。
-   傳回 **資料**：傳回 [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata)結構。 連接器類型會以 **dwData** 成員中的旗標形式傳回，以做為 [**COPP \_ ConnectorType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) 列舉的旗標。

顯示資料查詢

傳回透過連接器傳輸之視訊訊號的描述。

透過連接器傳送的視訊訊號不一定會與桌面顯示模式具有相同的格式。 例如，桌面顯示器模式可能是 85 Hz 的1024x768 圖元，而連接器可能是以720x480 圖元為單位傳輸視訊訊號的 S-video 連接器，60/1.01 Hz 交錯。 在此情況下，驅動程式會傳回 S-video 信號的解析度，而不是電腦解析度。

-   **GUID**： DXVA \_ COPPQueryDisplayData
-   **輸入資料**：無。
-   傳回 **資料**：傳回 [**DXVA \_ COPPStatusDisplayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata)結構。

HDCP 索引鍵資料查詢

傳回裝置的 HDCP 金鑰選取向量 (B-KSV) 。

KSV 是提供給裝置製造商的識別碼，用於 HDCP 驗證和設定程式。 應用程式應該針對已撤銷的 KSVs 清單來檢查此值。 取得 KSV 撤銷清單的機制超出 COPP 通訊協定的範圍。 如需詳細資訊，請參閱 HDCP 規格。

此查詢也會判斷連線的 HDCP 裝置是監視器還是 HDCP 中繼器。 如果 HDCP 裝置為 HDCP 中繼器，應用程式不應該播放受保護的內容，因為 COPP 不支援這些功能。

-   **GUID**： DXVA \_ COPPQueryHDCPKeyData
-   **輸入資料**：無。
-   傳回 **資料**：傳回 [**DXVA \_ COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata)結構。

全域保護等級查詢

傳回所指定保護機制的全域保護層級。

全域保護層級是目前正在連接器上套用的保護層級，而不管圖形驅動程式如何指示套用保護。 例如，應用程式可以藉由呼叫 **ChangeDisplaySettingsEx** 函數來設定 ACP 保護層級。 在這種情況下，全域保護層級會反映這項設定，即使不是透過 COPP 來要求也是一樣。

-   **GUID**： DXVA \_ COPPQueryGlobalProtectionLevel
-   **輸入資料**：要查詢的保護機制，指定為32位整數。 請參閱 [COPP 保護類型旗標](copp-protection-type-flags.md)。
-   傳回 **資料**：傳回 [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata)結構。 目前的保護層級會在 **dwData** 成員中傳回。 此值的意義取決於所查詢的保護機制。 針對每個保護機制， **dwData** 成員的值是來自不同列舉的旗標，如下表所示。

    | 保護機制 | 列舉型別                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**COPP \_ ACP \_ 保護 \_ 等級**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**COPP \_ CGMSA \_ 保護 \_ 等級**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | 觀看                 | [**COPP \_ HDCP \_ 保護 \_ 等級**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

本機保護等級查詢

傳回所指定保護機制的本機保護層級。

本機保護層級是透過目前的 COPP 會話所要求的保護層級。 驅動程式可能會設定較高的保護層級。

-   **GUID**： DXVA \_ COPPQueryLocalProtectionLevel
-   **輸入資料**：要查詢的保護機制，以32位整數來進行查詢。 請參閱 [COPP 保護類型旗標](copp-protection-type-flags.md)。
-   傳回 **資料**：傳回 [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata)結構。 目前的保護層級會在 **dwData** 成員中傳回。 此值的意義取決於所查詢的保護機制。 針對每個保護機制， **dwData** 成員的值是來自不同列舉的旗標，如下表所示。

    | 保護機制 | 列舉型別                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**COPP \_ ACP \_ 保護 \_ 等級**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**COPP \_ CGMSA \_ 保護 \_ 等級**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | 觀看                 | [**COPP \_ HDCP \_ 保護 \_ 等級**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

保護類型查詢

傳回連接器可用的保護機制。

-   **GUID**： DXVA \_ COPPQueryProtectionType
-   **輸入資料**：無。
-   傳回 **資料**：傳回 [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata)結構。 保護機制會以零或多個旗標的組合傳回 **dwData** 成員。 請參閱 [COPP 保護類型旗標](copp-protection-type-flags.md)。 如果有一個以上的保護機制可用，旗標就會與位 **or** 合併。

發出信號查詢

傳回驅動程式支援的所有保護標準的清單、目前作用中的標準，以及目前的外觀比例或其他信號資料。

-   **GUID**： DXVA \_ COPPQuerySignaling
-   **輸入資料**：無。
-   傳回 **資料**：傳回 [**DXVA \_ COPPStatusSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata)結構。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用認證輸出保護通訊協定 (COPP) ](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



