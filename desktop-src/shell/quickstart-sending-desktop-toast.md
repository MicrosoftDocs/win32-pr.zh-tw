---
description: 本快速入門說明如何從桌面應用程式引發快顯通知。
title: 從桌面傳送快顯通知
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 36f9da25c20d99da74be30046fc5f9f4789dfd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850032"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a>快速入門：從桌面傳送快顯通知

本快速入門說明如何從桌面應用程式引發快顯通知。

## <a name="prerequisites"></a>必要條件

-   程式庫
    -   C + +：執行時間 .lib
    -   C \# ： Windows. Winmd
-   您必須將應用程式的快捷方式（具有 [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md)）安裝至開始畫面。 不過請注意，它不需要釘選到開始畫面。 如需詳細資訊，請參閱 [如何透過 AppUserModelID 啟用桌面](enable-desktop-toast-with-appusermodelid.md)快顯通知。
-   至少支援 Windows 8 的 Microsoft Visual Studio 版本

## <a name="instructions"></a>指示

### <a name="1-create-your-toast-content"></a>1. 建立您的快顯內容

> [!Note]  
> 當您指定包含影像的快顯範本時，請注意桌面應用程式只能使用本機映射;不支援 web 映射。 此外，您必須將本機影像檔案的路徑提供為絕對 (而非相對) 路徑。

 


```csharp
// Get a toast XML template
XmlDocument toastXml = ToastNotificationManager.GetTemplateContent(ToastTemplateType.ToastImageAndText04);

// Fill in the text elements
XmlNodeList stringElements = toastXml.GetElementsByTagName("text");
for (int i = 0; i < stringElements.Length; i++)
{
    stringElements[i].AppendChild(toastXml.CreateTextNode("Line " + i));
}

// Specify the absolute path to an image
String imagePath = "file:///" + Path.GetFullPath("toastImageAndText.png");
XmlNodeList imageElements = toastXml.GetElementsByTagName("image");

ToastNotification toast = new ToastNotification(toastXml);
```



### <a name="2-create-and-attach-the-event-handlers"></a>2. 建立並附加事件處理常式

註冊快顯事件的處理常式：啟用、關閉和失敗。 傳統型應用程式至少必須訂閱已啟動的事件，讓它可以在使用者選取時，處理來自快顯通知的應用程式預期啟用。


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a>3. 傳送快顯通知

> [!IMPORTANT]
> 您必須在每次呼叫 [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041)時，將應用程式快捷方式的 [AppUserModelID](../properties/props-system-appusermodel-id.md)包含在開始畫面上。 如果您無法這樣做，將不會顯示您的快顯通知。

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a>4. 處理回呼

如果您的應用程式從快顯通知收到「已啟動」回呼，請將它帶入前景。 當使用者選取快顯通知時，預期會將應用程式啟動至與該快顯內容相關的視圖。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[從桌面應用程式範例傳送快顯通知](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[如何透過 AppUserModelID 啟用桌面快顯通知](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[快顯通知 XML 架構](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[快顯通知總覽](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[快速入門：傳送快顯通知](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[快速入門：傳送快顯推播通知](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[快顯通知的指導方針和檢查清單](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[如何選擇和使用快顯通知範本](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[如何從快顯通知處理啟用](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[如何加入宣告快顯通知](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[選擇快顯通知範本](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[快顯音訊選項](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
