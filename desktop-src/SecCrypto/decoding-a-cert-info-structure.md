---
description: 指定憑證之後，解碼憑證 BLOB 的第一個步驟就是呼叫 CertCreateCertificateCoNtext，將編碼憑證的指標傳遞 (BLOB) 。
ms.assetid: b50530e2-15a0-4215-bf18-300cf67d1611
title: 解碼 CERT_INFO 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7178c9a5bcfc95a8e2945a6e381f0c2c29cf3b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558535"
---
# <a name="decoding-a-cert_info-structure"></a>解碼 CERT \_ 資訊結構

指定憑證之後，解碼憑證 [*BLOB*](../secgloss/b-gly.md) 的第一個步驟就是呼叫 [**CertCreateCertificateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)，將編碼憑證的指標傳遞 (*BLOB*) 。 呼叫此函式時，它會建立重複的編碼憑證、建立類型 [**cert \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)的結構，並建立 [**cert \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)類型的結構。 如下圖所示， [*憑證內容*](../secgloss/c-gly.md) 包含原始憑證 *BLOB*、類型為 **cert \_ CoNtext** 的 c 結構，以及 **cert \_ 資訊** 類型的 c 結構。 憑證 **\_ 內容** 結構的其中一個成員會指向 **cert \_ 資訊** 結構，而另一個成員會指向編碼的憑證 BLOB。

![憑證內容](images/certcntx.png)

編碼的物件 (資料成員) 一律會提供做為 [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) 函數的輸入，而輸出則是 C 結構，可能或可能沒有編碼的成員，這取決於您的進程有多遠。

另外還有另一個需要解碼的成員，也就是 **延伸** 成員。 雖然它未編碼于 [**CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) 層級，但它確實包含一些編碼資訊。 若要解碼這項資訊，請繼續進行，如下圖所示。

![解碼資訊](images/xtension.png)

在 [**cert \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) 結構中，成員 **rgExtension** 是憑證 [**\_ 延伸**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) 結構陣列的指標。 每個憑證 **\_ 延伸** 結構都有以編碼形式提供的 **值** 成員，需要進行解碼。 **值** 成員會傳遞至 [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)函式，然後函式的輸出取決於 **pszObjId** 成員的值。 請注意，在此圖中，會產生兩個不同的結構，其中一個類型 [**cert \_ 基本 \_ 條件約束 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) 和類型 [**cert \_ 授權單位 \_ 金鑰 \_ 識別碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info)，視 **pszObjId** 的值而定。

 

 
