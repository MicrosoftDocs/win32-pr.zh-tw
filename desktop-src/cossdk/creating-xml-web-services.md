---
description: 任何 COM + 應用程式都可以公開為 XML web service。
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: 建立 XML Web Service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12dbc5ee08d9300d52b538648ba520b16a60a9e3769242c252eaa40d518a3ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307335"
---
# <a name="creating-xml-web-services"></a>建立 XML Web Service

任何 COM + 應用程式都可以公開為 XML web service。 然後，您可以從遠端呼叫應用程式在伺服器 COM +) 目錄中所設定元件 (元件的預設介面中的方法。 您可以使用 [元件服務] 系統管理工具來建立 IIS 虛擬根目錄，以使用 SOAP 來呼叫元件方法。

> [!Note]  
> 您必須在電腦上安裝 .NET Framework，才能將 com + 應用程式公開為 XML web service。

 

**將 COM + 應用程式公開為 XML web service**

1.  在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要管理之電腦相關聯的 [ **Com + 應用程式** ] 資料夾。

2.  以滑鼠右鍵按一下您想要公開為 XML web service 的應用程式，然後選擇 [ **屬性**]。

3.  按一下 [屬性] 對話方塊中的 [ **啟用** ] 索引標籤。

4.  選取 [ **使用 SOAP** ] 核取方塊。

5.  在 [ **SOAP VRoot** ] 文字方塊中，輸入可從遠端存取元件方法的 IIS 虛擬根目錄的名稱。 請注意，SOAP VRoot 不能是另一個 SOAP VRoot 目錄的子目錄。

6.  按一下 [確定]。

    如果您將 IIS 虛擬根目錄指定為 *vroot* ，且您的伺服器完整功能變數名稱為 *servername*，則您的元件會公開為 XML web service 的 URL 為 HTTPs://*servername* / *vroot*/。

    您檔案系統中的對應目錄是 \\ windows \\ system32 \\ com \\ SoapVRoots \\ *vroot* \\ ;com + 會將數個設定檔和 ASP.NET 程式放在那裡。 若是負載過重的 XML web service，您可能會想要調整儲存在檔案 web.config 中的參數。如需此檔案的詳細資訊，請參閱 IIS 檔。

    公開為 XML web service 之 com + 應用程式的預設安全性設定，會根據安裝的 .NET Framework 版本而有所不同。 如果已安裝1.0 版，則根據預設，XML web service 不是安全的;接受所有呼叫，且不使用加密。 如果已安裝1.1 版或更新版本，則根據預設，XML web service 是安全的;呼叫端必須經過驗證，而且需要加密。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[以 CAO 模式存取 XML Web Service](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[在 WKO 模式中存取 XML Web Service](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[COM + SOAP 服務總覽](com--soap-service-overview.md)
</dt> <dt>

[保護 XML Web Service](securing-xml-web-services.md)
</dt> </dl>

 

 



