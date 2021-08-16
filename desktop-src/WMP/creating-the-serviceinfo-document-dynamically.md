---
title: 動態建立 ServiceInfo 檔
description: 動態建立 ServiceInfo 檔
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Windows Media Player 線上商店，建立 ServiceInfo 檔
- 線上商店，建立 ServiceInfo 檔
- 輸入1個線上商店，建立 ServiceInfo 檔
- 輸入2個線上商店，建立 ServiceInfo 檔
- Windows Media Player 線上商店，以動態方式建立 ServiceInfo 檔
- 線上商店，以動態方式建立 ServiceInfo 檔
- 輸入1個線上商店，以動態方式建立 ServiceInfo 檔
- 輸入2個線上商店，以動態方式建立 ServiceInfo 檔
- Windows Media Player 線上商店，ServiceInfo 檔
- 線上商店，ServiceInfo 檔
- 輸入1個線上商店、ServiceInfo 檔
- 輸入2個線上商店、ServiceInfo 檔
- 以動態方式建立 ServiceInfo 檔
- 建立 ServiceInfo 檔
- ServiceInfo 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3883487d072af57174a1f40f2fcef05d3290917b473a95bf723c34d793c5ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340988"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a>動態建立 ServiceInfo 檔

您可以使用 ASP 來建立 ServiceInfo 檔。 這可讓您使用下列技術，在線上商店中提供更大的彈性：

-   以動態方式產生 Url 的主機名稱。
-   根據地區設定和 geoid 參數變更當地語系化的 Url。
-   以動態方式將查詢字串參數從 ServiceInfo URL 附加至其他 Url，例如流覽網頁 URL。

下列範例程式碼顯示可動態建立 ServiceInfo 檔的簡易 ASP 頁面：


```C++
<%
    Dim sHost
    Dim sLocale

    sHost = Request.ServerVariables("HTTP_HOST")
    sLocale = Request.QueryString("locale")
%>

<?xml version="1.0" encoding="utf-8"?>
<ServiceInfo Version="1.00" Key="MyCommerceService">
    <FriendlyName>My Online Store</FriendlyName>
    <ServiceTask1
        URL = "https://<%= sHost %>/service/html/Music.asp">
    </ServiceTask1>
    <ServiceTask2
        URL = "https://<%= sHost %>/service/html/Video.asp">
    </ServiceTask2>
    <ServiceTask3
        URL = "https://<%= sHost %>/service/html/Radio.asp">
    </ServiceTask3>
    <Navigate
        BaseURL = "https://<%= sHost %>/service/html/navigate.asp?myloc<%= sLocale %>">
    </Navigate>
</ServiceInfo>
```



上述範例程式碼會使用 ASP 從 web 伺服器抓取主機名稱，並在檔中動態建立 Url。 程式碼也會從 ServiceInfo 要求抓取 *地區* 設定查詢字串參數，並將其附加至導覽頁面的 URL。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**類型2線上商店的流覽**](navigation-for-type-2-online-stores.md)
</dt> <dt>

[**類型1線上商店的 ServiceInfo 檔**](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**適用于 Type 2 線上商店的 ServiceInfo 檔**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 




