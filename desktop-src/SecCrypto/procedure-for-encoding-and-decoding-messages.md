---
description: 詳細說明編碼一般訊息的程式。
ms.assetid: 554cab0d-cfa2-46a7-80d9-f41430eb4b47
title: 編碼和解碼訊息的程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49da09c2318fffd3d1c92d6012055172709609a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985639"
---
# <a name="procedure-for-encoding-and-decoding-messages"></a>編碼和解碼訊息的程式

編碼一般訊息的程式如下所示。

**編碼訊息**

1.  針對所需的資料類型，初始化適當的資料結構。
2.  呼叫 [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)，傳遞必要的引數。 呼叫 **CryptMsgOpenToEncode** 時，如果要提供給 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 的資料已經經過訊息編碼，請在 *pszInnerContentObjID* 中傳遞適當的物件識別碼 (例如，"1.2.840.113549.1.7.2" 代表 szOID \_ RSA \_ signedData) 。 如果 *pszInnerContentObjID* 為 **Null**，則會假設 [*內部內容*](../secgloss/i-gly.md) 類型之前未經過編碼，並且會適當地處理。
3.  視需要呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 多次以完成訊息。 在最後一次呼叫時，將 *fFinal* 參數設定為 **TRUE**。  (需詳細資訊，請參閱 **CryptMsgUpdate**) 。
4.  呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) 以取得所需參數的指標，例如內容。 針對簡單的一般資料編碼，請使用 \_ \_ *dwParamtype* 的 CMSG 內容參數。
5.  藉由呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)來關閉訊息。

此程式會產生函式呼叫中所指定類型的編碼訊息。

解碼一般訊息的程式如下所示。

**解碼訊息**

1.  使用 [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength)來決定緩衝區保存編碼資料所需的長度。
2.  呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)，傳遞必要的引數。 為了維持與 Internet Explorer 版本3.0 的相容性，會提供 *dwMsgType* 參數。 在 Internet Explorer 3.0 中建立的已簽署資料不包含標頭資訊。 因此，如果這類訊息是從檔案簽章中解壓縮，則訊息類型必須傳遞至函式。 如果將零傳遞至 *dwMsgType* 參數，則函式會從訊息的標頭讀取訊息類型。 如果標頭遺失，函式呼叫將會失敗。 如果成功，則會傳回已開啟之訊息的控制碼。
3.  呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 一次。 這會根據訊息類型，對訊息採取適當的動作。
4.  如需訊息的其他處理，例如額外的解密或簽章驗證，請呼叫 [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)，並在 *dwCtrlType* 中傳遞所需的動作。
5.  呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) 以取得所需參數的指標，例如內容。 若要解碼簡單的一般資料，請使用 CMSG \_ CONTENT \_ PARAM 作為 *dwParamtype* 參數。
6.  呼叫 [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) 以關閉訊息。

如需執行這些步驟的範例，請參閱 [範例 C 程式：編碼和解碼資料](example-c-program-encoding-and-decoding-data.md)。 如需示範編碼、解碼以及驗證已簽署訊息簽章之程式的程式和範例，請參閱 [範例 C 程式：簽署、編碼、解碼和驗證訊息](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)。

 

 
