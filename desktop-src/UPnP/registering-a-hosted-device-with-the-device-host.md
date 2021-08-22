---
title: 向裝置主機註冊託管裝置
description: 註冊託管裝置表示提供裝置描述及其裝置控制物件給裝置主機。
ms.assetid: 1d85b412-9b1b-415d-8664-8d96a6644793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486d01364b684e2aa6792b8a6c0b91ccc87a26670057c67192fe587ac049c388
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999558"
---
# <a name="registering-a-hosted-device-with-the-device-host"></a>向裝置主機註冊託管裝置

註冊託管裝置表示提供裝置描述及其裝置控制物件給裝置主機。 然後，裝置主機會使用 UPnP 探索通訊協定來建立完整的 UPnP 裝置描述、發佈它，並在網路上公佈裝置。 一旦發佈裝置之後，就可以使用它來控制點。

裝置的註冊方式有兩種：

-   應用程式會建立裝置控制物件的實例，並將其指標傳遞至裝置主機。
-   應用程式會將已註冊裝置控制物件的 ProgID 傳遞給裝置主機。 裝置主機在接收裝置的第一個要求時，會將它具現化。

無論使用哪種方法，裝置主機都會在註冊後立即發佈並公告裝置。 這兩種方法之間的差異與載入裝置程式碼的方式不同。 當應用程式傳入裝置控制物件的指標時，裝置程式碼會在註冊時載入並執行。 當應用程式傳遞 ProgID 時，只會在叫用動作、查詢屬性或事件訂閱要求時載入裝置程式碼。 第二種方法會稍微提高效率。 不過，它不適用於必須在任何控制項或事件訂用帳戶要求抵達之前執行的裝置，因為使用此方法時，只會在需要時才建立裝置控制物件。 第二種方法也可能會在收到裝置類型的第一個要求時產生效能問題。

如果您想要確保在電腦啟動時，網路上的裝置主機會自動宣告裝置，請叫用 [**IUPnPRegistrar：： >registerdevice.js**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice)。 **>Registerdevice.js** 可確保只有在收到控制項或事件訂閱要求時，才會載入您的裝置程式碼。

如果您的裝置是暫時性或橋接，請叫用 [**IUPnPRegistrar：： RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)，當電腦重新開機時，不會自動重新通告裝置。

## <a name="discovery-announcement-lifetime"></a>探索公告存留期

裝置主機所註冊的每個裝置都會與存留期相關聯，該存留期是由裝置在註冊時所指定。 裝置的存留期是裝置的探索宣告有效的時間。 存留期會以首次探索宣告中的標頭形式傳遞至控制點。 裝置主機會在到期時間之前自動更新公告。 探索公告存留期的值應該是15分鐘或更多 (預設值為30分鐘) 。

## <a name="device-identifiers-created-at-registration"></a>註冊時建立的裝置識別碼

建立裝置描述範本時，裝置開發人員必須提供服務描述的資源路徑和相關聯的圖示。 資源路徑是由裝置應用程式所決定。

由於相同的裝置可以在同一部電腦上多次註冊，因此裝置描述範本中指定的 UDN 不足以唯一識別裝置。 因此，裝置在註冊後，裝置主機會建立裝置識別碼。 此裝置識別碼與裝置描述範本中的 UDN 相關，可以用來唯一識別裝置。

當裝置暫時取消註冊，然後重新註冊時，也會使用此識別碼。 當裝置暫時取消註冊時，裝置主機不會刪除 UDN。 未刪除 UDN 的原因包括：

-   正在升級裝置。
-   您正在變更裝置的屬性。
-   服務暫時無法使用。
-   您正在將新的服務新增至裝置。
-   您正在更新 DLL。
-   裝置處於待命模式。

如需註冊的詳細資訊，請參閱下列各節：

-   [如何向裝置主機註冊裝置](how-to-register-a-device-with-the-device-host.md)
-   [取消註冊裝置](unregistering-a-device.md)
-   [**IUPnPRegistrar::UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice)
-   [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)

 

 




