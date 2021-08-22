---
description: 本主題列出使用 XPS 數位簽章 API 將數位簽章新增至 XPS 檔的考慮。
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: 使用 XPS 數位簽章 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ea6e38704efa2a348a90fec247f37b9722857a3838b10233937e63dc37fdbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469350"
---
# <a name="using-xps-digital-signature-api"></a>使用 XPS 數位簽章 API

本主題列出使用 XPS 數位簽章 API 將數位簽章新增至 XPS 檔的考慮。

XPS 數位簽章 API 可讓應用程式要求使用者簽署 XPS 檔，並驗證 XPS 檔中找到的簽章。 XPS 數位簽章 API 可以套用至 XPS 檔，而不需要將它載入 XPS OM，並且可用於從 XPS OM 序列化的 XPS 檔串流。

[Xps 數位簽章 API 程式設計](#xps-digital-signature-api-programming-tasks)工作章節包含的主題說明如何使用 XPS 數位簽章 api 進行程式設計。 本主題列出在將數位簽章支援新增至應用程式時，使用 XPS 數位簽章 API 的下列考慮。

-   [XPS 數位簽章 API 程式設計工作](#xps-digital-signature-api-programming-tasks)
-   [XPS 數位簽章 API 程式設計的特殊注意事項](#special-notes-about-xps-digital-signature-api-programming)
    -   [驗證 XPS 檔中的數位簽章](#verifying-digital-signatures-in-an-xps-document)
    -   [數位簽章簽署原則](#digital-signature-signing-policy)
    -   [內嵌憑證鏈](#embedding-a-certificate-chain)
    -   [使用 CERT \_ 內容結構](#using-the-cert\_context-structure)
-   [相關主題](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a>XPS 數位簽章 API 程式設計工作

本章節包含的主題說明如何使用 XPS 數位簽章 API 來執行程式設計工作。

-   [一般數位簽章程式設計工作](basic-digital-signature-programming-tasks.md)<dl>

[初始化簽章管理員](initialize-the-signature-manager.md)  
    [簽署檔](sign-a-document.md)  
    [將簽名要求新增至 XPS 檔](add-a-signature-request-to-a-document.md)  
    [驗證檔簽章](verify-document-signatures.md)  
    </dl>
-   [其他數位簽章程式設計工作](advanced-digital-signature-programming-tasks.md)<dl>

[從檔案載入憑證](load-a-certificate-from-a-file.md)  
    [確認憑證支援簽章方法](verify-a-certificate-supports-a-signature-method.md)  
    [確認系統支援摘要式方法](verify-a-certificate-supports-a-digest-method.md)  
    [在檔中內嵌憑證鏈](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a>XPS 數位簽章 API 程式設計的特殊注意事項

當您使用 XPS 數位簽章 API 時，下列主題需要一些特殊的考慮。

-   [驗證 XPS 檔中的數位簽章](#verifying-digital-signatures-in-an-xps-document)
-   [數位簽章簽署原則](#digital-signature-signing-policy)
-   [內嵌憑證鏈](#embedding-a-certificate-chain)
-   [使用 CERT \_ 內容結構](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a>驗證 XPS 檔中的數位簽章

[**IXpsSignature：： Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) 只會檢查已簽署的內容，以判斷它在簽署後尚未變更。 **IXpsSignature：： verify** 不會驗證用來簽署檔內容的任何憑證。

如需有關憑證和密碼編譯的詳細資訊，請參閱 [關於密碼](/windows/desktop/SecCrypto/about-cryptography)編譯。

如需如何在程式中驗證檔簽章的範例，請參閱 [驗證檔](verify-document-signatures.md)簽章和憑證。

### <a name="digital-signature-signing-policy"></a>數位簽章簽署原則

數位簽章簽署原則會決定要簽署 XPS 檔的哪些部分。 其中一個簽署原則選項是簽署從簽章來源部分開始的簽章關聯性。 因為簽章關聯性會隨著每個新增的簽章而變更，所以在加入新簽章時，在此原則下建立的簽章將會中斷。 請確定您清楚瞭解設定此原則的含意和效果;否則，可能會產生非預期或不想要的行為。

如需簽署原則的詳細資訊，請參閱 [**XPS \_ 簽署 \_ 原則**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)。

### <a name="embedding-a-certificate-chain"></a>內嵌憑證鏈

組成特定憑證信任鏈的憑證可以新增至 XPS 檔。 內嵌這些憑證可讓應用程式更輕鬆地在離線案例中，以驗證數位簽章所使用的憑證。

如需有關如何將憑證內嵌至 XPS 檔的詳細資訊，請參閱 [在檔中內嵌憑證鏈](embedding-certificate-trust-chains-in-a-document.md)。

### <a name="using-the-cert_context-structure"></a>使用 CERT \_ 內容結構

[**Cert \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)和 [**cert \_ 資訊**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)結構是保存憑證資訊的主要資料結構。 如需有關使用這些結構的詳細資訊，請參閱 [使用 CERT \_ 資訊資料結構](/windows/desktop/SecCrypto/using-a-cert-info-data-structure)。

[**CERT \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)當您不再需要密碼編譯 API 函式時，必須釋放它所傳回的內容結構。 若要釋放 **憑證 \_ 內容** 結構，請呼叫 [**CertFreeCertificateCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) 函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[一般數位簽章程式設計工作](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[其他數位簽章程式設計工作](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[**憑證 \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CERT \_ 資訊**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[**CertFreeCertificateCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**XPS \_ 簽署 \_ 原則**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
