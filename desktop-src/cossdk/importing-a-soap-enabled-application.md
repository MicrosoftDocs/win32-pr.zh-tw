---
description: 當啟用 SOAP 的應用程式從 proxy 模式中的伺服器匯出時，匯入該應用程式的用戶端就可以自動存取它所包含之元件的方法（從遠端），如同用戶端啟始物件中伺服器提供的 web 服務一樣 (CAO) 模式。 這可讓您輕鬆地在網路上將 COM + 應用程式的功能部署為 XML web service。
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: 匯入 SOAP-Enabled 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9faca91a726caea765d4b2ca227ddba0ff3a2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510711"
---
# <a name="importing-a-soap-enabled-application"></a>匯入 SOAP-Enabled 應用程式

當啟用 SOAP 的應用程式從 proxy 模式中的伺服器 [匯出](exporting-a-soap-enabled-application.md) 時，匯入該應用程式的用戶端就可以自動存取它所包含之元件的方法（從遠端），如同用戶端啟始物件中伺服器提供的 web 服務一樣 (CAO) 模式。 這可讓您輕鬆地在網路上將 COM + 應用程式的功能部署為 XML web service。

在用戶端上使用以這種方式匯入之應用程式的元件時，不會在用戶端上執行，而是會使用匯出應用程式的來源伺服器所提供的 XML web service，從遠端存取。 如需使用以這種方式匯入之應用程式元件的詳細資訊，請參閱 [以 CAO 模式存取 XML Web Service](accessing-xml-web-services-in-cao-mode.md)。

## <a name="component-services-administrative-tool"></a>元件服務系統管理工具

若要將啟用 SOAP 的應用程式匯入至用戶端，請使用下列步驟：

1.  在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要安裝應用程式之用戶端電腦相關聯的資料夾。

2.  在用戶端的 [ **Com + 應用程式** ] 資料夾上按一下滑鼠右鍵，然後選擇 [ **新增**]。 **Com + 應用程式安裝精靈** 隨即出現。

3.  在 [ **Com + 應用程式安裝] 嚮導** 中，按一下 [ **安裝預先建立的應用程式 (s])**。

4.  流覽網路以找出或指定您要安裝應用程式之伺服器上的 MSI 檔案的網路路徑。

## <a name="visual-basic"></a>Visual Basic

不適用。

## <a name="cc"></a>C/C++

不適用。

## <a name="remarks"></a>備註

COM 元件是由 GUID 所識別，如果重新編譯元件，則會變更。 如果已重新編譯公開為 XML web service 的已設定 COM 元件，使用它的用戶端應用程式將會中斷。 因此，當重新編譯公開為 XML web service 的元件時，用戶端應該重新匯入使用該元件的應用程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + SOAP 服務總覽](com--soap-service-overview.md)
</dt> <dt>

[建立 XML Web Service](creating-xml-web-services.md)
</dt> <dt>

[匯出 SOAP-Enabled 應用程式](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



