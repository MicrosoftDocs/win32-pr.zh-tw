---
description: Microsoft Digest 的挑戰是由伺服器對 AcceptSecurityCoNtext (Digest) 函數的初始呼叫所產生。
ms.assetid: d33383c2-5c0d-401f-ab28-2a985f6508e0
title: 產生摘要挑戰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511ec4f01c90acf08669835f9728cc711dfd1023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194524"
---
# <a name="generating-the-digest-challenge"></a>產生摘要挑戰

Microsoft Digest 的挑戰是由伺服器對 [**AcceptSecurityCoNtext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函數的初始呼叫所產生。 此函式呼叫會產生 nonce，這是唯一的值，其中包含可用來偵測安全性違規的資訊。 此呼叫也會產生用來維護狀態資訊的部分 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 。 呼叫 **AcceptSecurityCoNtext (Digest 時)** 您指定內容需求旗標來控制 Microsoft Digest 的行為，以及設定保護的品質。 如需詳細資訊，請參閱 [摘要挑戰內容需求](#digest-challenge-context-requirements)。

[**AcceptSecurityCoNtext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)函式初始呼叫的輸出是包含權杖的安全性緩衝區，[*它會使用*](/windows/desktop/SecGloss/c-gly)HTTP 401 回應傳送給用戶端， (拒絕存取) 。

> [!Note]  
> 在輸入緩衝區中不含資訊的 [**AcceptSecurityCoNtext (摘要)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 的呼叫會傳回摘要挑戰。

 

## <a name="digest-challenge-context-requirements"></a>摘要挑戰內容需求

內容需求是決定下列事項的旗標：

-   Microsoft Digest 是否做為 SASL 機制或 HTTP 驗證通訊協定。
-   用戶端和伺服器所共用的安全性內容所支援的保護品質。

根據預設，Microsoft Digest 會作為 SASL 機制。 若要將它用於 HTTP 驗證，則 \_ \_ 必須由伺服器設定 ASC 需求 HTTP ( 0x10000000) 旗標。

內容需求會指定為傳遞給 [**AcceptSecurityCoNtext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)函數之 *fCoNtextReq* 參數的旗標。 旗標會藉由控制挑戰中的 qop 指示詞，來影響安全性內容的保護品質。

根據預設，qop 指示詞會設定為 "auth"。 若要產生將 qop 指示詞設定為 "auth-int" 的挑戰，伺服器必須指定下列一或多個旗標：

-   ASC \_ 需求 \_ 完整性
-   ASC 要求重新執行偵測 \_ \_ \_
-   ASC \_ 需求 \_ 序列 \_ 偵測

僅限 SASL：藉由指定 ASC \_ \_ 要求機密性內容需求旗標，以將 qop 指示詞設定為 "auth" 來產生挑戰。 因為此旗標對 HTTP 驗證無效，所以無法搭配 ASC 要求 \_ HTTP 旗標使用 \_ 。

如需 qop 指示詞的詳細資訊，請參閱 [保護品質和密碼](quality-of-protection-and-ciphers.md)。

如需挑戰的詳細資訊，請參閱 [摘要挑戰的內容](contents-of-a-digest-challenge.md)。

 

 
