---
description: 從 x.509 憑證格式第3版開始，憑證可能會包含憑證延伸。
ms.assetid: fb106cab-8a61-4a83-8fb4-7c045d905575
title: 延伸模組處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba61c5896887471038325eba0dbed75f43061cff81452727933a3013c37f8aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006926"
---
# <a name="extension-handlers"></a>延伸模組處理常式

從 [*X.509*](../secgloss/x-gly.md) 憑證格式第3版開始，憑證可能會包含憑證延伸。  (x.509 憑證的內容，請參閱 [憑證屬性](certificate-properties.md)。 ) 這些延伸模組表示其他資訊。 例如，延伸模組可以表示其他的主體識別資訊，也可以表示金鑰使用方式資訊，以指定可使用金鑰的 (例如簽章或加密) 。 針對應用程式使用定義了一組標準延伸模組，而且也可以自訂擴充功能。

每個擴充功能都有相關聯的物件識別碼字串，可識別其他資訊的類型，以及包含這項資訊的資料結構。 例如，金鑰使用方式物件識別碼為 "2.5.29.15"，表示金鑰使用方式資訊。 其相關聯的資料結構是 [**CRYPT \_ 位 \_ BLOB (位**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_bit_blob)) 指定如何使用金鑰。

擴充功能可以在發行之前新增至憑證。 發出憑證時，任何啟用的延伸模組都是憑證的一部分。 如果擴充功能標示為「重大」，則使用應用程式必須知道其使用方式，而且應用程式必須遵守延伸模組的意圖或值。 憑證服務允許透過 [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) 和 [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy)所提供的方法，在非發行的憑證上設定延伸模組。 如需憑證延伸的詳細資訊，請參閱 CryptoAPI 檔中的憑證 [**\_ 延伸**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) 。 如需一般憑證延伸模組資料結構的詳細資訊，請參閱 [X.509 憑證延伸結構](cryptography-structures.md)。

延伸模組處理常式是一個 COM 物件，它提供了更複雜但常用的延伸模組和資料類型（例如 IA5String 或 PrintableString）編碼的常式。

具有 **DATE**、 **LONG** 和 **BSTR** 資料類型的延伸模組不需要擴充處理常式。 原則模組只會呼叫 [**ICertServerPolicy：： SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) ，並將 *類型* 參數設定為代表延伸資料類型的值： PROPTYPE \_ DATE、PROPTYPE \_ LONG 或 PROPTYPE \_ STRING。 然後，它會將擴充傳遞給伺服器引擎。 伺服器引擎接著會執行 [*抽象語法標記法 (一)*](../secgloss/a-gly.md) (asn.1) 編碼，然後再將擴充功能儲存在憑證中。

不過，具有非這些預設類型之資料類型的延伸模組必須是由擴充處理常式編碼的，然後原則模組才會將它們傳遞給伺服器引擎。 當原則模組呼叫 [**ICertServerPolicy：： SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) 傳遞 asn.1 編碼的延伸至伺服器引擎時，它必須將 *型* 別參數設定為 PROPTYPE \_ BINARY。 然後，伺服器引擎只會將此編碼的延伸模組儲存在憑證中。

預設的擴充處理常式 Certenc.dll 會匯出許多 **ICertEncodeXXX** 介面，並且可由原則模組呼叫。 必要的類型資訊也包含在平臺軟體發展工具組 (SDK) 提供的 Certencl.dll 中。 每個介面都會提供 **編碼** 方法，以二進位格式傳回原則模組的 asn.1 編碼憑證延伸。 然後，您可以藉由呼叫 [**ICertServerPolicy：： SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) 方法，在憑證中設定延伸模組。

如需詳細資訊，請參閱 [撰寫自訂延伸模組處理常式](writing-custom-extension-handlers.md)。

 

 
