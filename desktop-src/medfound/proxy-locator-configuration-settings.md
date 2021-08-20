---
description: Proxy 定位器設定設定
ms.assetid: d74a85cf-293e-4322-9aff-55b06d6fda5e
title: Proxy 定位器設定設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5b2f7bc8e8567fcb1d84ab48bdd2a9652045ecb0332de63b82db2652dfe86a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058631"
---
# <a name="proxy-locator-configuration-settings"></a>Proxy 定位器設定設定

本主題說明預設 proxy 定位器的設定。 如需有關使用自訂設定來建立 proxy 定位器的詳細資訊，請參閱 [如何設定 Proxy 定位器](how-to-configure-the-proxy-locator.md)。

Proxy 定位器可以設定為以三種模式運作： *手動模式*、 *自動偵測模式* 和 *瀏覽器模式*。 這些值定義于 [**MFNET \_ PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) 列舉中。 應用程式可以藉由設定 [**MFNETSOURCE \_ PROXYSETTINGS**](mfnetsource-proxysettings-property.md) 屬性來設定模式。 您也可以將此屬性設定為 **MFNET \_ PROXYSETTING \_ NONE**，以將 proxy 定位器設定為不使用 proxy 伺服器。 如果媒體伺服器是本機主機，或應用程式要求類別 (127. x. x. x. x. x. x. x. x. x. x) —保留給回送測試，則不會使用 proxy 伺服器。

> [!Caution]  
> Proxy 伺服器是內部網路與網際網路之間的安全性屏障。 若未使用 proxy 伺服器，則會暴露網路的安全性威脅。

 

-   手動模式。 應用程式會藉由將 [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) 屬性設定為 **MFNET \_ PROXYSETTING \_ MANUAL** 來設定此模式。 應用程式必須指定下列連接資訊：

    -   Proxy 伺服器的主機名稱： [**MFNETSOURCE \_ PROXYHOSTNAME**](mfnetsource-proxyhostname-property.md) 屬性。
    -   埠號碼： [**MFNETSOURCE \_ PROXYPORT**](mfnetsource-proxyport-property.md) 屬性。
    -   是否針對本機位址使用 proxy 伺服器： [**MFNETSOURCE \_ PROXYBYPASSFORLOCAL**](mfnetsource-proxybypassforlocal-property.md) 屬性。 這個設定是選擇性的。 如果未指定此值，則 proxy 定位器會使用預設值 **FALSE**。

        > [!Note]  
        > 藉由略過 proxy 伺服器，應用程式可能可以更快地連接到內部網路上的媒體伺服器。

         

    -   不需要 proxy 伺服器來建立連線的媒體伺服器地址清單： [**MFNETSOURCE \_ PROXYEXCEPTIONLIST**](mfnetsource-proxyexceptionlist-property.md) 屬性。 這個設定是選擇性的。

-   自動偵測模式。 應用程式會藉由將 [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) 屬性設定為 **MFNET \_ PROXYSETTING \_ AUTO** 來設定此模式。 在此模式中，proxy 定位器會使用 WinHTTP 自動代理程式機制來取得 proxy 伺服器的主機名稱和埠號碼。 您可以使用 WPAD auto proxy 腳本（由網域系統管理員設定）來抓取此連接資訊。 如需此機制的詳細資訊，請參閱 [Microsoft 網站](../winhttp/winhttp-autoproxy-support.md)。

    Proxy 定位器會在登錄中快取連接資訊。 在後續的 proxy 偵測呼叫中，proxy 定位器會從登錄快取讀取 proxy 資訊，以降低自動偵測所需的額外負荷。 不過，應用程式可以藉由設定 [**MFNETSOURCE \_ PROXYRERUNAUTODETECTION**](mfnetsource-proxyrerunautodetection-property.md) 屬性來強制執行自動 proxy redetection。

-   瀏覽器模式。 應用程式會藉由將 [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) 屬性設定為 **MFNET \_ PROXYSETTING \_ BROWSER** 來設定此模式。 在此模式中，proxy 定位器會使用瀏覽器應用程式的 proxy 設定。 如果通訊協定是 HTTP 或 HTTPD，預設會設定此模式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網路來源的 Proxy 支援](proxy-support-for-network-sources.md)
</dt> </dl>

 

 
