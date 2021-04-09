---
title: 透過網站佈建 Wi-Fi 設定檔
description: 允許您的使用者從網站下載設定檔，並布建。
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933586"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a>透過網站佈建 Wi-Fi 設定檔

本主題所述的工作流程是在 Windows 10 2004 版中引進。 本主題說明如何設定網站，讓使用者可以布建 Passpoint 網路的設定檔 (或一般網路) ，再移至對應的 Wi-Fi 存取點的範圍。 其中一個範例案例是，可能打算首次造訪機場或會議的使用者，並且想要在家裡下載和布建設定檔以事先準備。

作為開發人員，您可以藉由提供 XML 設定檔和設定網站來啟用工作流程。 然後，您的使用者就可以透過網頁瀏覽器從您的網站下載 Wi-Fi 設定檔。 在使用者的裝置上，接著會使用 [URI 啟用] 和 [Windows **設定** ] 應用程式來布建 Wi-Fi 設定檔。

此工作流程會取代 Internet Explorer 中用於布建 Wi-Fi 設定檔的機制，而這些設定檔依賴 Microsoft 特定的 JavaScript Api。 這項新的工作流程預期會與所有主要瀏覽器搭配運作。

## <a name="the-workflow-in-more-detail"></a>更詳細的工作流程

您可以從包含做為引數的超連結啟動此工作流程，以提供 XML 檔的下載 URI。

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

例如，下列 HTML 標籤會提供一個連結，以安裝在假設檔中找到的設定檔 (s) `http://contoso.com/ProvisioningDoc.xml` 。

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

您的 XML 必須遵守布建架構 (查看 [帳戶](/windows-hardware/drivers/mobilebroadband/account-provisioning) 布建) 。 您的 XML 也必須包含一或多個 [WLANProfile](./wlan-profileschema-wlanprofile-element.md)   元素。每個設定檔會顯示在 [ **新增** ] 對話方塊中，如下所述。

當使用者按一下您的 HTML 連結時，會在 [ **設定** ] 應用程式中叫用安裝工作流程。 [ **設定** ] 應用程式會下載您的布建 XML 檔。 下載後，會顯示有關設定檔、簽章和簽署者的資訊， (前提是檔遵守架構) 。

![設定應用程式](images/install-dialog.png)

只有當布建檔案已簽署且受信任時，才會啟用 [**設定**] 應用程式對話方塊中的 [**新增**] 按鈕。

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a>在您的網頁中，判斷是否支援此工作流程

在 JavaScript 中，沒有任何方法可判斷 Windows 的確切組建版本。 但是，如果您的使用者使用 Microsoft Edge 的網頁瀏覽器，您就可以檢查 HTTP 標頭的值來判斷 Edge 的版本 `User-agent` 。 如果版本大於或等於 `18.nnnnn` ，則支援工作流程。

## <a name="related-topics"></a>相關主題

* [帳戶布建](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [WLANProfile 元素](./wlan-profileschema-wlanprofile-element.md)