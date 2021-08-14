---
description: 您可以設定 (CA) 的 Microsoft 憑證授權單位單位，以封存和復原與憑證要求中所提交之公開金鑰相關聯的私密金鑰。
ms.assetid: c6535dbf-c3fe-4f70-9a70-02805253a651
title: 金鑰修復伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a313ac46bf540d6d0f356f7e2c4910e31bee1f2a4268931ac6a942085505b423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903771"
---
# <a name="key-recovery-server"></a>金鑰修復伺服器

您可以設定 (CA) 的 Microsoft 憑證授權單位單位，以封存和復原與憑證要求中所提交之公開金鑰相關聯的私密金鑰。 如果遺失金鑰，復原會很有用。 依預設，只可封存加密金鑰。 不需要封存僅供簽署的金鑰，因為如果遺失私用簽署金鑰，則只需要公開金鑰來驗證簽章。

若要封存金鑰，必須將 CA 設定為向 (KRA) 憑證發出金鑰復原代理，並至少已發出一個憑證。 金鑰復原代理是組織授權的系統管理員，可將私密金鑰解密。 為了增強安全性，建議您將金鑰復原代理和憑證管理員角色指派給不同的個人、允許憑證管理員抓取但不解密封存金鑰，以及允許金鑰復原代理程式解密金鑰，但無法取出金鑰。

## <a name="key-archival"></a>金鑰保存

用戶端通常會使用範本來要求憑證。 如果範本需要封存私密金鑰，則下列步驟是由用戶端和 CA 執行：

1.  用戶端會抓取並驗證 CA exchange 憑證，以判斷它是否已由用來簽署 CA 簽署憑證的相同金鑰簽署。 這可確保唯一可解密私密金鑰的 CA 是要求憑證的 CA。
2.  CA exchange 憑證中的公開金鑰是用來加密與憑證要求相關聯的私密金鑰，並將要求傳送至 CA。
3.  CA 會使用與其 exchange 憑證相關聯的私密金鑰來解密用戶端所傳送的私密金鑰，並確認要求中的公開金鑰和私密金鑰相關聯。
4.  CA 會使用 KRA 憑證中的公開金鑰來加密私密金鑰。 如果 CA 已發出多個 KRA 憑證，它會使用每個可用的公開金鑰來加密私密金鑰一次，讓任何授權的金鑰復原代理程式都可以復原金鑰。 加密的私密金鑰會儲存在憑證資料庫中。
5.  CA 會釋放私密金鑰的所有參考，並安全地釋出所有包含金鑰的記憶體和零。 這可確保 CA 無法再以純文字格式存取金鑰。

> [!Note]  
> 只有 CMC 要求才能用於金鑰保存。 CMC 要求會以 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 介面表示。

 

## <a name="key-recovery"></a>金鑰復原

Active Directory 憑證服務或憑證註冊 API 不直接支援金鑰復原。 不過，Microsoft 會提供下列應用程式來協助處理：

-   Certutil.exe 是命令列程式，可用來取出 CA 設定資訊、驗證憑證、金鑰組和憑證鏈，以及備份和還原金鑰。 它包含在從 Windows server 2003 開始的伺服器作業系統中。
-   Krecover.exe 是以對話方塊為基礎的程式，可進行金鑰修復。 它隨附于從 Windows Server 2003 開始的資源套件。

您可以執行下列步驟來復原私密金鑰：

1.  憑證管理員會使用憑證、要求者或使用者的名稱，找出憑證資料庫中金鑰復原的潛在候選項目。 **Certutil** **-getkey** 命令可用於此用途。
2.  一旦憑證管理員有憑證清單之後，就會再次呼叫 **-getkey** 命令，並使用特定的憑證序號或 thumb 列印來取出 PKCS \# 7 檔案，其中包含在使用 kra 公開金鑰進行封存期間加密的 KRA 憑證、使用者憑證鏈，以及私密金鑰。
3.  憑證管理員會將進程的控制權傳遞給金鑰復原代理程式，其私密金鑰符合 KRA 憑證中包含的公開金鑰。
4.  Key recovery agent 會 \# 使用 KRA 私密金鑰來解密 PKCS 7 檔案中所傳回的封存私密金鑰。 這可以藉由使用 **Certutil** **-recoverkey** 命令來完成，此命令會將金鑰放在受密碼保護的 PKCS 12 檔案中 \# 。 用戶端必須透過安全的頻外機制提供密碼。
5.  用戶端會匯入 PKCS \# 12 檔案並使用密碼來取得金鑰。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PKI 元素](about-pki-components.md)
</dt> </dl>

 

 



