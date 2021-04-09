---
title: 使用者帳戶控制和位
description: 當系統管理員使用者登入電腦時，會建立兩個存取權杖。 其中一個是篩選的標準使用者存取權杖，另一個則是完整的系統管理員存取權杖。
ms.assetid: 02439ab3-b885-4a2f-b507-0c48d2b30b76
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 3017b3a0d816ba393d1427c5c1d2315a68b2dcc0
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2020
ms.locfileid: "103933011"
---
# <a name="bits-security-tokens-and-administrator-accounts"></a>BITS 安全性、權杖和系統管理員帳戶

## <a name="http-server-certificate-callbacks"></a>HTTP 伺服器證書回呼
正確驗證伺服器憑證是維護 HTTPS 安全性的重要部分。 BITS 有助於根據 [**SetSecurityFlags**](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags)所指定的需求清單，一律驗證伺服器憑證。 依預設，BITS 會使用「瀏覽器」樣式憑證驗證。

您也可以指定要呼叫的自訂函數，以便進一步驗證憑證。 使用 [**SetServerCertificateValidationInterface**](/windows/desktop/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-setservercertificatevalidationinterface) 方法來設定伺服器憑證回呼。 只有在作業系統已根據 [ **SetSecurityFlag**](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags)的呼叫驗證憑證之後，才會呼叫您的方法。 

## <a name="http-client-certificates"></a>HTTP 用戶端憑證
您可以使用兩種不同的憑證設定方法，在 HTTP 作業上設定用戶端憑證。 您可以依 [識別碼](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) 或憑證 [主體名稱](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname)來設定憑證。 如果伺服器需要用戶端驗證，則會在 TLS 協商期間使用用戶端憑證 (或重新協商) 。

## <a name="write-only-http-headers"></a>僅限寫入的 HTTP 標頭
BITS 可協助您保護 HTTP 驗證權杖免于不必要的存取。 HTTP 伺服器通常會在下載檔案或將檔案上傳至 HTTP 伺服器時，需要某種類型的安全性權杖或字串。

BITS 會以數種方式保護這些驗證權杖。
* BITS 可讓您藉由指定 HTTPS URL 來使用 TLS 和受 SSL 保護的 HTTP 連接。
* 自訂標頭一律會以加密格式保存在磁片上。
* 您可以使用 [**IBackgroundCopyJobHttpOptions3：： MakeCustomHeadersWriteOnly**](/windows/win32/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-makecustomheaderswriteonly) 方法，防止客戶標頭傳回其他程式。


## <a name="standard-and-administrator-users"></a>標準和系統管理員使用者
系統管理員群組中的使用者可以使用系統管理員許可權) ，以標準使用者存取權或提高許可權的狀態 (處理常式。 只要使用者登入電腦，BITS 就會以任一狀態執行工作。 不過，如果使用者建立工作或取得工作的擁有權（以提高許可權狀態），則使用者必須處於提升的狀態才能抓取或修改作業 (否則，呼叫會失敗，並會拒絕存取 (0x80070005) ) 。 若要判斷作業的提升狀態，請呼叫 [**IBackgroundCopyJob4：： GetOwnerElevationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerelevationstate) 方法。

標準使用者無法列舉或修改其他使用者所擁有的作業。

## <a name="integrity-level"></a>完整性層級
除了提升的狀態之外，權杖的完整性層級還可以判斷使用者是否可以修改作業。 用戶端無法修改具有較高完整性層級的權杖所建立的工作。 尤其是許多本機系統權杖的完整性層級高於提高許可權之視窗的完整性層級，因此系統管理員無法從一般提高許可權的命令視窗修改它們。 例如，Windows Update 和 SMS 作業以 LocalSystem 的身分執行，其完整性層級高於提高許可權的權杖，因此系統管理員無法修改或刪除這些作業。 若要修改這些作業，請建立以本機系統的形式執行工作排程器工作。 工作可以執行使用 BITS API 的主控台應用程式，或者工作可以執行呼叫 BitsAdmin.exe 的腳本。 若要判斷使用的完整性層級，請呼叫 [**IBackgroundCopyJob4：： GetOwnerIntegrityLevel**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerintegritylevel) 方法。

## <a name="service-identity"></a>服務身分識別
從 Windows 10 2019 年5月更新 (10.0;組建 18362) ，從服務啟動的 BITS 作業將會維護服務身分識別。 這可讓想要使用 BITS 的服務，將檔案從其許可權系結至服務 SID 的目錄中下載檔案或上傳檔案。 此外，網路流量將會正確地設定為要求 BITS 工作的服務，而不是以位為的屬性。

 




