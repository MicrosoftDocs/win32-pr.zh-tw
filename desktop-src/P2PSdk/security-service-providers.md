---
description: 安全性服務提供者介面 (SSPI) 為安全的分散式應用程式提供通用的產業標準介面。
ms.assetid: c3cebb9d-9094-493f-96d3-763a0c282dfb
title: 安全性服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2121940337d0f4e06c53981cf30f0125180c466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985473"
---
# <a name="security-service-providers"></a>安全性服務提供者

安全性服務提供者介面 (SSPI) 為安全的分散式應用程式提供通用的產業標準介面。 對等圖形 API 提供了一種方法，可讓應用程式藉由指定安全性服務提供者 (SSP) 來保護圖形中的連結，這是一個可實作為 SSPI 介面的 DLL。 應用程式會在使用 [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)建立圖形時指定 SSP。

如需建立您自己的 SSP 的詳細資訊，請參閱 [圖表參考連結](graphing-reference-links.md)清單中的 SSPI 檔連結。

## <a name="programming-considerations-for-implementing-an-ssp"></a>執行 SSP 的程式設計考慮

從 SSP 內呼叫應用程式時，請特別小心。 下列考慮適用于 SSP 回呼：

-   回呼不應該花很長的時間來傳回，因為它們是在連接協商期間呼叫。 如果建立連接需要太長的時間，可以卸載連接。
-   對等圖形 API 會根據系統的實際負載，動態調整連接逾時值。 最低的超時值為20秒。
-   為了避免潛在的鎖死情況，應用程式不能從回呼存取對等圖形資料庫。 如果應用程式需要來自圖形資料庫的資訊，應用程式可以快取所需的資訊，然後從回呼內參考快取。 快取也可協助縮短連線時間。

呼叫 SSPI 進入點時，對等圖形基礎結構需要五個 (5) 函式的特定參數的特定值。 您無法變更提供給 SSP 的參數值，而且 SSP 可以忽略五個參數的值或正常處理這些參數的值。 下列清單會識別這些特定參數和必要值：

-   [**AcquireCredentialsHandle**](graphing-reference-links.md)

    為 *pvGetKeyArgument* 參數指定一個 (1) 。 針對 *pszPrincipal*、 *pvLogonID* 和 *pGetKeyFn* 參數指定 **Null** 。

-   [**InitializeSecurityCoNtext**](graphing-reference-links.md)

    指定下列 *fCoNtextReq* 參數旗標： isc 要求 **\_ \_ 相互驗證的 \_ \| isc 要求 \_ \_ 機密性 isc \| 要求 \_ \_ 完整性 \| isc 要求 \_ 順序 \_ 偵測 \_ 到 \| isc \_ 需求 \_ 資料流程的 \| isc 要求 \_ \_ 配置 \_ 記憶體**。

-   [**AcceptSecurityCoNtext**](graphing-reference-links.md)

    為 *fCoNtextReq* 參數指定下列旗標： **asc 要求 \_ \_ 相互 \_ 驗證 asc \| 要求 \_ \_ 機密性 \| asc 要求 \_ \_ 完整性 asc 要求順序偵測 asc 要求 \| \_ \_ \_ \| \_ \_ 資料流程 \| asc \_ 需求 \_ 配置 \_ 記憶體**。

-   [**EncryptMessage**](graphing-reference-links.md)

    針對 *fQOP* 和 *MessageSeqNo* 參數，指定零 (0) 。

-   [**DecryptMessage**](graphing-reference-links.md)

    針對 *MessageSeqNo* 參數指定零 (0) ，針對 *PfQOP* 參數指定 **Null** 。

呼叫 [**EncryptMessage**](graphing-reference-links.md)時，會在 **SecBufferDesc** 結構中傳遞四個緩衝區。 下表指出傳遞緩衝區的順序。

| SSP 特定結構         | Description                                                                                                                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **之 SECBUFFER \_ 資料流程 \_ 標頭**  | 包含安全性標頭資料。 標頭緩衝區的大小是藉由呼叫 [**QueryCoNtextAttributes**](graphing-reference-links.md) 並指定 **SECPKG \_ ATTR \_ 資料流程 \_ 大小** 屬性取得。  |
| **之 SECBUFFER \_ 資料**            | 包含要加密的純文字訊息。                                                                                                                                                                  |
| **之 SECBUFFER \_ 資料流程 \_ 結尾** | 包含安全性尾端資料。 標頭緩衝區的大小是藉由呼叫 [**QueryCoNtextAttributes**](graphing-reference-links.md) 並指定 **SECPKG \_ ATTR \_ 資料流程 \_ 大小** 屬性取得。 |
| **之 SECBUFFER \_ 空白**           | 未初始化。 此緩衝區的大小為零 (0) 。                                                                                                                                                             |



 

呼叫 [**DecryptMessage**](graphing-reference-links.md)時，對等圖形 API 只會傳遞四個 **之 secbuffer** 結構。 第一個緩衝區是 **之 secbuffer \_ 資料**，並且包含加密的訊息。 其餘的緩衝區用於輸出，其類型為 **之 secbuffer \_ 空白**。

SSP 需要在一次呼叫中支援加密和解密大小為16K 以上的使用者資料緩衝區。

 

 



