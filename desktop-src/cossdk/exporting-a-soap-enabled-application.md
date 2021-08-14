---
description: 當您使用 COM + 來建立 XML web service 時，該服務可供任何授權用戶端使用，包括未使用 COM + 或甚至是 Microsoft Windows 的用戶端。
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: 匯出 SOAP-Enabled 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce79bbc5dca59feb23ba9e976575b3b33570ecd27cf1e6a68560b02e073f48bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307285"
---
# <a name="exporting-a-soap-enabled-application"></a>匯出 SOAP-Enabled 應用程式

當您使用 COM + 來建立 XML web service 時，該服務可供任何授權用戶端使用，包括未使用 COM + 或甚至是 Microsoft Windows 的用戶端。 不過，在用戶端啟動的物件中使用 COM + web 服務，從 COM + 用戶端應用程式 (CAO) 模式是特別簡單的。 只要以 proxy 模式匯出啟用 SOAP 的應用程式，然後將它匯 [入](importing-a-soap-enabled-application.md) 您要存取對應之 XML web service 的用戶端。

## <a name="component-services-administrative-tool"></a>元件服務系統管理工具

若要從伺服器匯出啟用 SOAP 的應用程式，請使用下列步驟：

1.  在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要管理之電腦相關聯的 [ **Com + 應用程式** ] 資料夾。

2.  以滑鼠右鍵按一下您想要公開為 XML web service 的元件，然後選擇 [ **匯出**]。 **Com + 應用程式匯出 Wizard** 隨即出現。

3.  在標示為 **要建立之應用程式檔的完整路徑和檔案名** 的文字方塊中，輸入將包含所匯出應用程式之 MSI 檔案的完整路徑和檔案名，或按一下 **[流覽]** 以使用對話方塊來選取完整路徑和檔案名。

4.  在 [ **匯出為**] 下，選取 [ **應用程式 Proxy –安裝在其他電腦上，以啟用此電腦的存取** ] 選項按鈕。

## <a name="visual-basic"></a>Visual Basic

不適用。

## <a name="cc"></a>C/C++

不適用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + SOAP 服務總覽](com--soap-service-overview.md)
</dt> <dt>

[建立 XML Web Service](creating-xml-web-services.md)
</dt> <dt>

[匯入 SOAP-Enabled 應用程式](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



