---
description: COM + SOAP 服務安全性考慮
ms.assetid: c4f7744c-ff57-4d9d-8632-7e5bbb73449a
title: COM + SOAP 服務安全性考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67e034dfeaa4ec7f8688420aafcaec434653c942665ec3e3cbaa1535b51980d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548547"
---
# <a name="com-soap-service-security-considerations"></a>COM + SOAP 服務安全性考慮

COM + SOAP 服務取決於 IIS web 伺服器的安全性。 即使在 [用戶端啟動的物件模式](accessing-xml-web-services-in-cao-mode.md)中，COM + RPC 也不會傳輸用戶端身分識別，因此無法使用以角色為基礎的安全性或 DCOM 所提供的任何其他安全性功能。 如果您想要協助保護您的 XML web 服務所傳送之資料的隱私權，或協助保護您的 XML web service 免于未經授權的存取，您可以將 IIS 設定為根據用戶端 IP 位址限制 XML web service 的存取，或要求用戶端出示數位憑證來驗證其身分識別。 如果您未限制存取，任何可以與 web 伺服器通訊的用戶端都可以存取您的 XML web service。

您可以設定 IIS 使用公開金鑰加密 SSL 或 TLS 通訊協定，將 XML web service 與用戶端的通訊加密。 如果您不加密 SOAP 通訊，在用戶端與伺服器之間交換的資料可能會由協力廠商觀察到任何透過其傳送 SOAP 通訊之網路的存取;視網路拓撲而定，這可能是小型 LAN 或可能是網際網路。

根據預設，會在 HTTP 埠 (80) 接收未加密的 SOAP 通訊，並在 HTTPS 埠 (443) 接收加密的 SOAP 通訊。 若要讓用戶端成功存取 XML web service，用戶端與伺服器之間的所有防火牆都必須設定為允許 TCP SYN 封包到達適當的伺服器埠。 相反地，若要限制存取 XML web service，防火牆系統管理員可以選擇關閉這些埠。

公開為 XML web service 之 COM 元件的預設安全性設定，會根據安裝的 Microsoft .NET Framework 版本而有所不同。 如果已安裝1.0 版，則根據預設，XML web service 不是安全的;接受所有呼叫，且不使用加密。 如果已安裝1.1 版或更新版本，則根據預設，XML web service 是安全的;呼叫端必須經過驗證，而且需要加密。

受保護的 XML web service 不支援透過 WSDL 的 WKO 存取。 相反地，安裝 .NET Framework 1.1 版的用戶端可以使用 CAO 模式來呼叫它。 如果協力廠商用戶端需要透過 WSDL 存取您的 XML web service，您必須允許匿名存取。

公開為 XML web service 的 COM 元件預設會以匿名使用者的許可權來執行， (不會使用其呼叫端) 的許可權。 您可以將 IIS 設定為以不同的使用者的形式執行 XML web service;有時可能是必要的，因為您的元件使用的是匿名使用者沒有存取權的檔案或其他資源。 不過，您應該一律嘗試以最少的許可權來執行您的元件，以限制惡意呼叫端可能造成的損害。

> [!Note]  
> 因為您透過 XML web service 公開的方法可能會向惡意呼叫端公開，所以您應該一律務必驗證它所相依的任何輸入參數。

 

如需有關如何設定特定 XML web service 安全性設定的詳細指示，請參閱 [保護 XML Web 服務](securing-xml-web-services.md)。

**將安全的 SOAP 應用程式轉換成不安全的 SOAP 應用程式**

1.  開啟 Internet Information Services (IIS) 系統管理工具。
2.  找出應用程式的虛擬目錄，然後開啟 [ **屬性** ] 對話方塊。
3.  勾選 [**檔**] 索引標籤上的 [**啟用預設內容] 頁面**。
4.  在 [**目錄安全性**] 索引標籤中，按一下 [**匿名存取及驗證控制**] 底下的 [**編輯**
5.  核取 [ **匿名存取** ] 以啟用匿名存取，然後按一下 **[確定]**。
6.  按一下 [**安全通訊**] 下的 [**編輯**]。
7.  取消核取 [ **需要安全通道 (SSL)** ] 核取方塊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + SOAP 服務總覽](com--soap-service-overview.md)
</dt> </dl>

 

 



