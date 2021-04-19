---
description: 媒介會與用戶端應用程式通訊，以允許它們提交憑證要求，並 (假設要求產生已發行的憑證) 將發行的憑證下載至用戶端。
ms.assetid: c696f09e-98d3-4cea-8ea1-cd8f40b74f12
title: 媒介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 040e79abb03bd0363d37fdad79f7311412b0ffe2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106976625"
---
# <a name="intermediaries"></a>媒介

媒介會與用戶端應用程式通訊，以允許它們提交 [*憑證要求*](../secgloss/c-gly.md)，並 (假設要求產生已發行的憑證) 將發行的憑證下載至用戶端。 每個傳輸層通訊協定都需要自己的媒介。

Microsoft 憑證服務隨附的中繼 () for HTTP 的網頁註冊頁面。 媒介的另一個範例是 Microsoft Windows 憑證 MMC 嵌入式管理單元， (可讓您) 叫用憑證要求 Wizard。 如果有其他傳輸層通訊協定與憑證服務搭配使用，開發人員可以為每個所需的傳輸層通訊協定建立媒介。

媒介會使用伺服器引擎所提供的 [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) 和 [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) 介面，與憑證服務進行通訊。 [**ICertRequest：： submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit)方法可用來提交 [*憑證要求*](../secgloss/c-gly.md)，而 [**ICertRequest：： GetCertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcertificate)用來取得所產生的已發行憑證。 同樣地， [**ICertConfig：： GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig) 可用來判斷可用來發行憑證的憑證授權單位單位。

媒介與語言無關。 它可能是以 c + +、Visual Basic、JAVA、腳本或其他語言撰寫的程式。

除了從用戶端收集資料以建立憑證要求之外，媒介還可以指定要求屬性。 提交給執行企業原則模組之 [*憑證授權單位*](../secgloss/c-gly.md) 單位的要求，必須透過在要求本身中指定 "CertificateTemplate" 屬性或憑證範本延伸來指出所要求的憑證類型。

請注意，在建立憑證要求期間，開發人員 (和媒介) 負責維護私密金鑰的密碼。 私密金鑰遭入侵之後 (遺失其秘密) ，就沒有用處。

憑證服務網頁註冊頁面會使用 [憑證註冊介面](cryptography-interfaces.md)，藉由在工作站上產生金鑰來保護私密金鑰。 除了維護私密金鑰的密碼，憑證註冊控制項還允許媒介指定密碼編譯服務提供者、金鑰規格、金鑰強度和雜湊演算法。

憑證 MMC 嵌入式管理單元也會使用憑證註冊控制項 (Xenroll.dll) 。 但是，憑證服務網頁註冊頁面會在需要時將憑證註冊控制資源 (Xenroll.dll) 下載至用戶端，而憑證 MMC 嵌入式管理單元則是在 Xenroll.dll 已是可用資源的環境中執行。

除了 [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) 和 [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)，仲介的開發人員也可能會發現 [憑證註冊介面](cryptography-interfaces.md) 和 [智慧卡註冊控制項](certificate-enrollment-control.md) 都很有用。

 

 
