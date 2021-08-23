---
description: 取得驅動程式憑證鏈
ms.assetid: bc7b346c-3382-4f2b-90b6-03f6a1a5a9ce
title: 取得驅動程式憑證鏈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2641c27c3d24ab45a87b16e8c805228c316d9f89428cd29abbaff347b5aae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684558"
---
# <a name="obtaining-the-drivers-certificate-chain"></a>取得驅動程式憑證鏈

若要 (COPP) 使用經認證的輸出保護通訊協定，應用程式必須先建立 DirectShow 圖形，其中包含影片混合轉譯篩選 (VMR-7 或 VMR-9) 。 較舊的影片轉譯器篩選器不支援 COPP。 在呼叫任何 COPP 方法之前，應用程式必須建立影片播放圖形，並將該解碼器連接至 VMR 濾波器的輸入圖釘。 不需要播放影片檔案。

建立圖形之後，請查詢 [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) 介面的 VMR，然後呼叫 [**IAMCertifiedOutputProtection：： KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange)。 這個方法會傳回類型為 GUID 的128位亂數字，以及位元組陣列的指標，其中包含以 UTF-8 格式表示的驅動程式 XML 憑證鏈。 下列程式碼說明如何取得憑證鏈。


```C++
GUID guidRandom;
BYTE *pbCertificateChain = NULL;
DWORD cbCertificateChainLen;   // Size of the certificate chain, in bytes.
hr = pCOPP->KeyExchange(&guidRandom, &pbCertificateChain,
         &cbCertificateChainLen);
if (SUCCEEDED(hr))
{
    // TODO: Validate the certificate chain and get the driver's
    // public key. 

    // When you are done, free the buffer that contains the 
    // certificate chain.
    CoTaskMemFree(pbCertificateChain);
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用認證輸出保護通訊協定 (COPP) ](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



