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
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a><span data-ttu-id="7896e-103">快速入門：從桌面傳送快顯通知</span><span class="sxs-lookup"><span data-stu-id="7896e-103">Quickstart: Sending a toast notification from the desktop</span></span>

<span data-ttu-id="7896e-104">本快速入門說明如何從桌面應用程式引發快顯通知。</span><span class="sxs-lookup"><span data-stu-id="7896e-104">This quickstart shows how to raise a toast notification from a desktop app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7896e-105">必要條件</span><span class="sxs-lookup"><span data-stu-id="7896e-105">Prerequisites</span></span>

-   <span data-ttu-id="7896e-106">程式庫</span><span class="sxs-lookup"><span data-stu-id="7896e-106">Libraries</span></span>
    -   <span data-ttu-id="7896e-107">C + +：執行時間 .lib</span><span class="sxs-lookup"><span data-stu-id="7896e-107">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="7896e-108">C \# ： Windows. Winmd</span><span class="sxs-lookup"><span data-stu-id="7896e-108">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="7896e-109">您必須將應用程式的快捷方式（具有 [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md)）安裝至開始畫面。</span><span class="sxs-lookup"><span data-stu-id="7896e-109">A shortcut to your app, with a [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), must be installed to the Start screen.</span></span> <span data-ttu-id="7896e-110">不過請注意，它不需要釘選到開始畫面。</span><span class="sxs-lookup"><span data-stu-id="7896e-110">Note, however, that it does not need to be pinned to the Start screen.</span></span> <span data-ttu-id="7896e-111">如需詳細資訊，請參閱 [如何透過 AppUserModelID 啟用桌面](enable-desktop-toast-with-appusermodelid.md)快顯通知。</span><span class="sxs-lookup"><span data-stu-id="7896e-111">For more information, see [How to enable desktop toast notifications through an AppUserModelID](enable-desktop-toast-with-appusermodelid.md).</span></span>
-   <span data-ttu-id="7896e-112">至少支援 Windows 8 的 Microsoft Visual Studio 版本</span><span class="sxs-lookup"><span data-stu-id="7896e-112">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="7896e-113">指示</span><span class="sxs-lookup"><span data-stu-id="7896e-113">Instructions</span></span>

### <a name="1-create-your-toast-content"></a><span data-ttu-id="7896e-114">1. 建立您的快顯內容</span><span class="sxs-lookup"><span data-stu-id="7896e-114">1. Create your toast content</span></span>

> [!Note]  
> <span data-ttu-id="7896e-115">當您指定包含影像的快顯範本時，請注意桌面應用程式只能使用本機映射;不支援 web 映射。</span><span class="sxs-lookup"><span data-stu-id="7896e-115">When you specify a toast template that includes an image, be aware that desktop apps can use only local images; web images are not supported.</span></span> <span data-ttu-id="7896e-116">此外，您必須將本機影像檔案的路徑提供為絕對 (而非相對) 路徑。</span><span class="sxs-lookup"><span data-stu-id="7896e-116">Also, the path to the local image file must be provided as an absolute (not relative) path.</span></span>

 


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



### <a name="2-create-and-attach-the-event-handlers"></a><span data-ttu-id="7896e-117">2. 建立並附加事件處理常式</span><span class="sxs-lookup"><span data-stu-id="7896e-117">2. Create and attach the event handlers</span></span>

<span data-ttu-id="7896e-118">註冊快顯事件的處理常式：啟用、關閉和失敗。</span><span class="sxs-lookup"><span data-stu-id="7896e-118">Register handlers for the toast events: Activated, Dismissed, and Failed.</span></span> <span data-ttu-id="7896e-119">傳統型應用程式至少必須訂閱已啟動的事件，讓它可以在使用者選取時，處理來自快顯通知的應用程式預期啟用。</span><span class="sxs-lookup"><span data-stu-id="7896e-119">A desktop app must at least subscribe to the Activated event so that it can handle the expected activation of the app from the toast when the user selects it.</span></span>


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a><span data-ttu-id="7896e-120">3. 傳送快顯通知</span><span class="sxs-lookup"><span data-stu-id="7896e-120">3. Send the toast</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7896e-121">您必須在每次呼叫 [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041)時，將應用程式快捷方式的 [AppUserModelID](../properties/props-system-appusermodel-id.md)包含在開始畫面上。</span><span class="sxs-lookup"><span data-stu-id="7896e-121">You must include the [AppUserModelID](../properties/props-system-appusermodel-id.md) of your app's shortcut on the Start screen each time that you call [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041).</span></span> <span data-ttu-id="7896e-122">如果您無法這樣做，將不會顯示您的快顯通知。</span><span class="sxs-lookup"><span data-stu-id="7896e-122">If you fail to do this, your toast will not be displayed.</span></span>

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a><span data-ttu-id="7896e-123">4. 處理回呼</span><span class="sxs-lookup"><span data-stu-id="7896e-123">4. Handle the callbacks</span></span>

<span data-ttu-id="7896e-124">如果您的應用程式從快顯通知收到「已啟動」回呼，請將它帶入前景。</span><span class="sxs-lookup"><span data-stu-id="7896e-124">Bring your app's window to the foreground if it receives an "activated" callback from the toast notification.</span></span> <span data-ttu-id="7896e-125">當使用者選取快顯通知時，預期會將應用程式啟動至與該快顯內容相關的視圖。</span><span class="sxs-lookup"><span data-stu-id="7896e-125">When a user selects a toast, the expectation is that the app will be launched to a view related to the content of that toast..</span></span>

## <a name="related-topics"></a><span data-ttu-id="7896e-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="7896e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7896e-127">從桌面應用程式範例傳送快顯通知</span><span class="sxs-lookup"><span data-stu-id="7896e-127">Sending toast notifications from desktop apps sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[<span data-ttu-id="7896e-128">如何透過 AppUserModelID 啟用桌面快顯通知</span><span class="sxs-lookup"><span data-stu-id="7896e-128">How to enable desktop toast notifications through an AppUserModelID</span></span>](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[<span data-ttu-id="7896e-129">快顯通知 XML 架構</span><span class="sxs-lookup"><span data-stu-id="7896e-129">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="7896e-130">[快顯通知總覽](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7896e-130">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7896e-131">[快速入門：傳送快顯通知](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7896e-131">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7896e-132">[快速入門：傳送快顯推播通知](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7896e-132">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="7896e-133">快顯通知的指導方針和檢查清單</span><span class="sxs-lookup"><span data-stu-id="7896e-133">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

<span data-ttu-id="7896e-134">[如何選擇和使用快顯通知範本](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7896e-134">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7896e-135">[如何從快顯通知處理啟用](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7896e-135">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7896e-136">[如何加入宣告快顯通知](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7896e-136">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7896e-137">[選擇快顯通知範本](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7896e-137">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7896e-138">[快顯音訊選項](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7896e-138">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 
