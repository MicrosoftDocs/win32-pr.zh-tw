---
description: 傳送 COPP 狀態要求
ms.assetid: 9f9950ff-469f-4cea-924e-3f9471eb4838
title: 傳送 COPP 狀態要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5494b0e856df573bdbfc9b1554ab82be206a95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687384"
---
# <a name="sending-copp-status-requests"></a>傳送 COPP 狀態要求

若要傳送經認證的輸出保護通訊協定 (COPP) 狀態要求，請在 [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) 結構中填入要求資料。 結構成員如下：

-   **rApp**。 128位的亂數字，以 GUID 類型。 驅動程式回應中會傳回相同的數位。 您應該在堆積上配置亂數字，然後將它複製到結構中。 這可防止攻擊者修改 [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) 結構的內容。
-   **guidStatusRequestID**。 識別要求的 GUID。 請參閱 [COPP 查詢參考](copp-query-reference.md)。
-   **dwSequence**。 狀態序號。 在每個狀態要求之後遞增此值。  (在 [起始 COPP 會話](initiating-a-copp-session.md)的區段中，此值在程式碼範例中會顯示為 *uStatusSeq* ) 。
-   **cbSizeData**。 要求所需的任何其他資料大小（以位元組為單位）。
-   **>statusdata**。 狀態要求的資料。

將 [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) 結構傳遞至 [**IAMCertifiedOutputProtection：:P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) 方法。 例如，下列程式碼會傳送狀態要求，以查詢可用的保護機制：


```C++
AMCOPPStatusInput input;
AMCOPPStatusOutput output;

// Create a 128-bit random number.
GUID *pGuid = new GUID();
if (pGuid == NULL)
{
    // Handle out-of-memory condition.
}
CryptGenRandom(hCSP, sizeof(GUID), (BYTE*)pGuid);  

// Copy the random number into the command structure.
memcpy(&input.rApp, pGuid, sizeof(GUID));

// Fill in the other data.
input.guidStatusRequestID = DXVA_COPPQueryProtectionType; // Request type.
input.dwSequence = uStatusSeq;  // Status sequence number.
input.cbSizeData = 0            // No other data for this query.

// Send the request.
hr = pCOPP->ProtectionStatus(&input, &output);

// Increment the sequence number each time.
++uStatusSeq;
```



回應會寫入 [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput)結構的 **COPPStatus** 成員中。 **CbSizeData** 成員會提供回應中有效資料的大小。 為確保訊息的完整性，驅動程式會使用 OMAC 1 演算法來計算 (MAC) 的訊息驗證碼，並在結構的 **macKDI** 成員中傳回此值。 應用程式應驗證此值，如下所示：

1.  針對在 [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) (結構的 **macKDI** 成員後面出現的資料區塊，計算 OMAC 標記，也就是 **cbSizeData** plus **COPPStatus**) 。
2.  使用直接 **memcmp**，將此標記與 **macKDI** 中的值進行比較。

OMAC 1 演算法的詳細說明，請參閱 [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) 。 COPP 會使用下列 OMAC-1 參數：

-   E = AES
-   t = 128 位

從狀態要求傳回的資料一律會從兩個專案開始：

-   應用程式所傳遞的相同 **rApp** 值。 您應確認這個值符合堆積上儲存的原始值。
-   [**COPP \_ StatusFlags**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags)值，指出輸出保護狀態是否已變更。

由於連接可能會遺失或重新設定，因此應用程式應該定期輪詢驅動程式是否有目前的狀態。 如果 \_ 已設定 COPP RenegotiationRequired 旗標，則應用程式應該嘗試重設保護層級。 如果 \_ 已設定 COPP LinkLost 旗標，應用程式應該停止播放內容。 例如， \_ 可能會傳回 COPP LinkLost 旗標，因為使用者已中斷輸出連接器的連線。 應用程式應該釋放目前的 VMR 實例、建立新的 VMR 實例，然後建立新的 COPP 會話， (包括金鑰交換和憑證驗證) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用認證輸出保護通訊協定 (COPP) ](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



