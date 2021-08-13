---
description: 公開為 XML web service 的 COM + 應用程式的存取權，是由處理傳入要求的 IIS web 伺服器所控制。
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: 保護 XML Web Service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccc49a096def7fdca3f508ca590cd23df0fbf2e92fd816ba55300931122361e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546961"
---
# <a name="securing-xml-web-services"></a>保護 XML Web Service

公開為 XML web service 的 COM + 應用程式的存取權，是由處理傳入要求的 IIS web 伺服器所控制。 您也可以將 IIS 設定為要求與呼叫端進行通訊，以透過使用安全通訊端層 (SSL) 通訊協定建立的安全通道進行通訊。

> [!Note]  
> 受保護的 XML web service 不支援透過 WSDL 的 WKO 存取。 相反地，安裝 .NET Framework 1.1 版的用戶端可以使用 CAO 模式來呼叫它。 如果協力廠商用戶端需要透過 WSDL 存取您的 XML web service，您必須允許匿名存取。

 

> [!Note]  
> 若要使用 SSL 通訊協定來建立安全的通道，您必須取得並安裝 SSL 憑證。

 

## <a name="component-services-administrative-tool"></a>元件服務系統管理工具

若要選取 XML web service 的驗證機制，請使用下列步驟：

1.  以滑鼠右鍵按一下桌面上的 **我的電腦** 圖示，然後按一下 [ **管理**]。

2.  在 [ **服務和應用程式** ] 和 [ **網際網路資訊服務**] 下，找出對應至 XML web Service 之虛擬根目錄的圖示。 以滑鼠右鍵按一下目錄圖示，然後選擇 [ **屬性**]。

3.  在 [內容] 對話方塊的 [ **目錄安全性** ] 索引標籤上，尋找 [ **驗證和存取控制** ]，然後按一下對應的 [ **編輯** ] 按鈕。

4.  在 [ **驗證方法** ] 對話方塊中，于 [ **已驗證的存取**] 下，使用核取方塊來選取您想要允許的驗證機制。 按一下 [確定]。

    > [!Note]  
    > 您可以使用 [iis **驗證方法**] 對話方塊上的下列任何選項，將 iis 設定為驗證呼叫者：**整合式 Windows 驗證**、 **Windows 網域伺服器的摘要式驗證**、**基本驗證 (密碼以純文字傳送)** 或 **.net Passport 驗證**。 您也可以允許匿名存取。

     

5.  在 [屬性] 對話方塊中，按一下 **[確定]**。

若要允許非安全、匿名存取 XML web service，請使用下列步驟：

1.  以滑鼠右鍵按一下桌面上的 **我的電腦** 圖示，然後按一下 [ **管理**]。

2.  在 [ **服務和應用程式** ] 和 [ **網際網路資訊服務**] 下，找出對應至 XML web Service 之虛擬根目錄的圖示。 以滑鼠右鍵按一下目錄圖示，然後選擇 [ **屬性**]。

3.  在 [內容] 對話方塊的 [ **目錄安全性** ] 索引標籤上，尋找 [ **驗證和存取控制**]，然後按一下對應的 [ **編輯** ] 按鈕。 選取 [ **啟用匿名存取** ] 核取方塊。 按一下 [確定]。

4.  在 [內容] 對話方塊的 [ **目錄安全性** ] 索引標籤上，找出 **安全通訊** ，然後按一下對應的 [ **編輯** ] 按鈕。 取消核取 [ **需要安全通道 (SSL)** ] 核取方塊。 按一下 [確定]。

5.  在 [屬性] 對話方塊中，按一下 **[確定]**。

## <a name="visual-basic"></a>Visual Basic

不適用。

## <a name="cc"></a>C/C++

不適用。

## <a name="additional-security-considerations"></a>其他安全性考慮

藉由要求安全通道，您可以藉由加密用戶端和 XML web 服務之間的通訊，來協助保護交換的資料機密性。 如果您允許使用純文字密碼進行驗證，則應該要求安全通道以避免在網路上公開密碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[以 CAO 模式存取 XML Web Service](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[在 WKO 模式中存取 XML Web Service](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[COM + SOAP 服務安全性考慮](com--soap-service-security-considerations.md)
</dt> <dt>

[建立 XML Web Service](creating-xml-web-services.md)
</dt> </dl>

 

 



