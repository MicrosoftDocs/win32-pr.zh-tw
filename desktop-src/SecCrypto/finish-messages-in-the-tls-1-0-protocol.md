---
description: 完成的訊息會在變更加密規格訊息之後立即傳送，以確認金鑰交換和驗證程式是否成功。
ms.assetid: 1ae92223-3729-48be-af42-146c9cbae6a5
title: 在 TLS 1.0 通訊協定中完成訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e9af7502f0865661e2ed0f6a80059cb822395002ccaf035373dc3db322adac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006976"
---
# <a name="finish-messages-in-the-tls-10-protocol"></a>在 TLS 1.0 通訊協定中完成訊息

完成的訊息會在變更加密規格訊息之後立即傳送，以確認金鑰交換和驗證程式是否成功。 TLS 1.0 通訊協定中的完成訊息會使用 [*虛擬隨機函式*](../secgloss/p-gly.md) 來計算， (PRF) ，其中包含 [*主要金鑰*](../secgloss/m-gly.md)、標籤和種子做為輸入。 PRF 會產生任意長度的輸出。 下列方法可用來產生 TLS 1.0 完成訊息中使用的 PRF 輸出。

使用 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)來產生 PRF [*雜湊*](../secgloss/h-gly.md)控制碼，並將 **ALG \_ 識別碼** 值設定為 CALG \_ TLS1PRF，並將控制碼傳遞至 *hKey* 參數中傳遞的主要金鑰。 在使用 CryptSetHashParam 函式的 DwParam 參數中，每個在雜湊控制碼上分別使用值 HP \_ TLS1PRF \_ LABEL 和 HP \_ TLS1PRF \_ seed  [](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam)來設定標籤和種子值。 最後，通訊協定引擎會使用 DwParam 參數中的值 HP HASHVAL 來呼叫函數 [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) \_ ，以抓取要包含在完成訊息中的 PRF 資料。 對 **CryptGetHashParam** 進行呼叫時，通訊協定引擎必須指定要產生的資料位元組數目。 這是在 *pdwDataLen* 參數中完成，而產生的資料會放在 *>pbdata* 參數所指向的緩衝區中。

以下是此通訊協定引擎的一般原始程式碼：


```C++
CRYPT_DATA_BLOB Data;
HCRYPTHASH hFinishHash;
BYTE rgbFinishPRF[12];
BYTE rgbCliHashOfHandshakes[36];

//------------------------------------------------------------
// get client finish message

CryptCreateHash(
         hProv, 
         CALG_TLS1PRF, 
         hMasterKey, 
         0, 
         &hFinishHash);

Data.pbData = (BYTE*)"client finished";
Data.cbData = 15;
CryptSetHashParam(
         hFinishHash, 
         HP_TLS1PRF_LABEL, 
         (BYTE*)&Data, 
         0);

Data.pbData = rgbCliHashOfHandshakes;
Data.cbData = sizeof(rgbCliHashOfHandshakes);
CryptSetHashParam(
          hFinishHash, 
          HP_TLS1PRF_SEED, 
          (BYTE*)&Data, 
          0);

cbFinishPRF = sizeof(rgbFinishPRF);
CryptGetHashParam(
          hFinishHash, 
          HP_HASHVAL, 
          rgbFinishPRF, 
          &cbFinishPRF, 
          0);

CryptDestroyHash(hFinishHash);
```



 

 
