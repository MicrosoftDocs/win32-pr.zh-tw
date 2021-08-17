---
title: 簡報
description: 簡報是 UPnP 流程中的最後一個步驟。
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92f8457a881dc0414713e996d230261330c10911f2aea285a2e365ad0d59320
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137191"
---
# <a name="presentation"></a>簡報

簡報是 UPnP 流程中的最後一個步驟。 如果裝置有用於表示的 URL，則控制點可以從此 URL 取出頁面，並將頁面載入瀏覽器。 視簡報頁面和裝置的功能而定，控制點可以控制裝置並查看裝置的狀態。

在註冊期間傳遞給 [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) 的資源路徑，是所有與裝置呈現相關的檔案所在的位置。 裝置開發人員可以為每個內嵌裝置提供個別頁面。 裝置描述範本中的表示 URL 可以是絕對 URL 或相對 URL。 針對相對於資源路徑的相對 Url，裝置描述範本應該包含檔案名。 **IUPnPRegistrar** 會將此值轉換為實際位置的 URL。 若為絕對 Url，則不會修改位置。

為了在簡報頁面內支援用戶端腳本，額外的資訊通常會以「查詢字串」的形式附加至 URL。 附加的額外資訊是裝置描述檔的 URL，以及裝置或內嵌裝置的 UDN。 裝置描述 URL 可以用來在腳本中載入描述檔，然後透過其服務控制裝置。 UDN 用來從根裝置選取內嵌裝置。

修改過之呈現 URL 的格式為：實際的簡報 URL，問號 ( "？") ，裝置描述 URL、加號 ( "+" ) 、裝置 UDN。 問號代表查詢字串的開頭。

如果裝置描述範本中的簡報 URL 是絕對 URL，而且它已包含問號 ( "？") ，則不會將額外的資訊新增至展示 URL。



| 描述                        | URL                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| 在裝置描述範本中 | **presentationURL** MyDevice.html **/presentationURL**                                                                                              |
| 由裝置主機產生       | **presentationURL** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394... + UDN **/presentationURL** |



 

用戶端腳本可能必須從展示 URL 中解壓縮裝置描述 URL 以載入 [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) 物件。 這是藉由取得查詢字串，並以加號 ( "+" ) 來終止。


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



如果是內嵌裝置的簡報頁面，則需要一些額外的工作。 載入 [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)之後，腳本必須取得內嵌裝置的集合，然後選取符合查詢字串中 UDN 的裝置。 下列腳本示範如何針對目前的簡報頁面選取內嵌裝置。 它會假設已載入 LightDesc。


```VB
Dim LightDevice
Set LightDevice = LightDesc.RootDevice

Dim EmbeddedDevices 
set EmbeddedDevices = LightDevice.Children

Dim DeviceUdnString
DeviceUdnString = Trim(Mid(QueryString,Instr(QueryString,"+")+1,Len(QueryString)))

Dim Item
set Item = EmbeddedDevices.Item(DeviceUdnString)
```



 

 




