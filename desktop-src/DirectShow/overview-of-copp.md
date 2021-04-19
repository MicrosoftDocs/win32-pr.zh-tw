---
description: COPP 總覽
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: COPP 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970500"
---
# <a name="overview-of-copp"></a>COPP 總覽

以下是應用程式必須執行的基本步驟，才能使用認證輸出保護通訊協定 (COPP) 。

**取得驅動程式的憑證鏈**

1.  使用影片混合轉譯器 (VMR-7 或 VMR-9) 或 [**增強型影片**](enhanced-video-renderer-filter.md) 轉譯器篩選器 (EVR) ，建立可轉譯影片的 DirectShow 播放圖形。
2.  查詢 [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) 介面的 VMR。
3.  呼叫 [**IAMCertifiedOutputProtection：： KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange)。 這個方法會從驅動程式傳回128位的亂數字，以及包含驅動程式2048位 RSA 公開金鑰的憑證鏈。

**驗證憑證鏈**

1.  驗證憑證鏈。 如果憑證鏈無效，請停止。
2.  檢查憑證撤銷清單 (CRL) 。 如果憑證鏈中有任何憑證出現在撤銷清單中，請停止。
3.  從憑證鏈取得 RSA 公開金鑰。

**將 COPP 會話初始化**

1.  產生128位 AES 工作階段金鑰。 此金鑰是用來簽署資料，並確認已簽署的資料尚未遭到篡改。
2.  產生兩個密碼編譯安全32位亂數字。 第一個是狀態序號，而第二個是命令序號。 每次應用程式傳送命令或狀態要求時，它會遞增對應的序號，並在 COPP 命令中包含此號碼或要求資料。
3.  從圖形驅動程式、AES 工作階段金鑰、狀態序號和命令序號串連128位的亂數字。 使用驅動程式的公開金鑰來加密此位元組陣列，並將結果傳遞給 [**IAMCertifiedOutputProtection：： SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart)。

**傳送 COPP 命令和狀態要求**

1.  藉由呼叫 [**IAMCertifiedOutputProtection：:P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus)，查詢可用的保護類型和其他資訊。
2.  藉由呼叫 [**IAMCertifiedOutputProtection：:P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand)來設定所需的保護層級。
3.  定期查詢目前的本機保護層級。 如果本機保護等級未預期地變更，或如果偵測到問題，則停止播放。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用認證輸出保護通訊協定 (COPP) ](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



