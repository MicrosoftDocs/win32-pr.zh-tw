---
description: 網路來源的 Proxy 支援
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: 網路來源的 Proxy 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971690"
---
# <a name="proxy-support-for-network-sources"></a>網路來源的 Proxy 支援

Proxy 伺服器是您內部網路與網際網路之間的轉送伺服器，可將要求從用戶端應用程式路由傳送至媒體伺服器，並從媒體伺服器抓取檔案。

當用戶端應用程式嘗試存取來源 URL 時，媒體基礎隱含地建立 *proxy 定位器* 物件。 Proxy 定位器物件會公開 [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) 介面。 在來源解析期間，媒體基礎會檢查傳遞給來源解析程式方法的屬性存放區。

如果屬性存放區包含的 [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) 屬性設定為應用程式所執行的 proxy 定位器 factory 物件，則會叫用 [**IMFNetProxyLocatorFactory：： CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) 方法，以使用自訂設定來建立 proxy 定位器。

如果未設定屬性存放區，媒體基礎會使用預設設定來建立 proxy 定位器。 這些設定如下所示：

-   如果設定了 [使用者原則]，則 proxy 定位器會使用登錄中指定的設定。

-   若為 HTTP，proxy 定位器會使用瀏覽器 proxy 設定。

-   針對 RTSP，proxy 定位器設定為在連線至媒體伺服器時略過 proxy 伺服器。

應用程式可以變更此預設設定。 下列主題包含 proxy 定位器設定的相關資訊：

-   [Proxy 定位器設定](proxy-locator-configuration-settings.md)

-   [如何設定 Proxy 定位器](how-to-configure-the-proxy-locator.md)

媒體基礎初始化指定給 [來源解析程式](source-resolver.md)之來源 URL 的 proxy 定位器。 Proxy 定位器會根據設定來偵測要使用的 proxy 伺服器。 當 proxy 定位器嘗試設定 proxy 伺服器時，它會在登錄中記錄成功或失敗的結果。 在下一個 proxy 偵測程式期間，會檢查此值。 如果已知特定的 proxy 伺服器在過去造成失敗，proxy 定位器就會略過它。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[屬性和屬性](attributes-and-properties.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 



