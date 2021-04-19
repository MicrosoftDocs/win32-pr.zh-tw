---
description: 說明如何使用 CryptMsgCountersign 來對訊息進行副署。
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Countersigning 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02091d25e7ee22f986a26b8f07abff68ebb8c11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980520"
---
# <a name="countersigning-a-message"></a>Countersigning 訊息

**若要使用 CryptMsgCountersign 來副署已簽署的訊息**

1.  呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) 以取得已簽署訊息的控制碼。
2.  初始化 countersigner 的 [**CMSG \_ 簽署者 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) 結構。
3.  將 [**CMSG \_ 簽署者 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) 結構新增至 countersigners 的陣列 () 目前只支援一個 countersigner。
4.  呼叫 [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) 以新增副署或副署。

如果所有的函式呼叫都成功，則原始訊息現在會以未驗證的屬性包含 [*副署*](../secgloss/c-gly.md) 。

**若要使用 CryptMsgCountersignEncoded 來副署已簽署的訊息**

1.  呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) 以取得已簽署訊息的控制碼。
2.  呼叫 [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) 以取得已簽署訊息的編碼簽署者資訊。
3.  初始化 countersigner 的 [**CMSG \_ 簽署者 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) 結構。
4.  將 [**CMSG \_ 簽署者 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) 結構新增至 countersigners 的陣列 () 目前只支援一個 countersigner。
5.  呼叫 [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) 來建立編碼的副署屬性。
6.  呼叫 [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) 將副署屬性新增至原始訊息作為未驗證的屬性。

如果所有函式呼叫都成功，則會將 [*副署*](../secgloss/c-gly.md) 屬性新增至原始訊息。

 

 
