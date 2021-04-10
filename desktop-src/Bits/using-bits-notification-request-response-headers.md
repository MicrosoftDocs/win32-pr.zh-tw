---
title: 使用 BITS 通知要求/回應標頭
description: BITS 可以透過參考) 將上傳檔案 (的位置傳送至您的伺服器應用程式，也可以在 (要求的主體中傳送上傳檔案) 的值。
ms.assetid: b80f9077-54e7-4d10-909a-dee7d8822627
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dcbee8b82d96a4f13db0ae4de6441e9df40ce83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183043"
---
# <a name="using-bits-notification-requestresponse-headers"></a>使用 BITS 通知要求/回應標頭

BITS 可以透過參考) 將上傳檔案 (的位置傳送至您的伺服器應用程式，也可以在 (要求的主體中傳送上傳檔案) 的值。 若要指定 BITS 如何將上傳檔案傳送至您的伺服器應用程式，請設定 IIS 元檔案屬性 [**BITSServerNotificationType**](bits-iis-extension-properties.md)。 如果您以傳址方式指定，BITS 會以位---------Name 標頭傳遞檔案的位置。 若要傳送回復，請建立您的回應，並將其寫入至位-回應-資料檔案-名稱標頭中指定的檔案。

傳送相同回復給許多用戶端的伺服器應用程式應該以傳址方式使用，因此伺服器上只會有一個回復複本。 例如，在軟體更新應用程式中，用戶端會將其軟體設定上傳至伺服器應用程式。 伺服器應用程式會決定用戶端所需的封裝，並將封裝的 URL 傳送給位。 然後，BITS 會將套件下載為回復。

針對每個用戶端產生唯一回復的伺服器應用程式應該使用 value。 例如，支援購買音樂檔案的伺服器應用程式，必須將簽署的音樂檔案傳送給用戶端。 因為簽署的音樂檔案對用戶端而言是唯一的，所以伺服器應用程式不會將它儲存在伺服器上。 依值也適用于已撰寫成直接接受 web 用戶端資料的應用程式。

如需在 BITS 和您的伺服器應用程式之間使用的要求和回應標頭的詳細資訊，請參閱 [伺服器應用程式的通知通訊協定](notification-protocol-for-server-applications.md)。

下列 JavaScript 範例示範如何在參考通知所使用的伺服器應用程式中存取要求和回應檔 (BITS 會將標頭中的檔案位置傳遞) 。


```JavaScript
  var fso = new ActiveXObject ("Scripting.FileSystemObject")
  var requestFileName = Request.ServerVariables ("HTTP_BITS-Request-DataFile-Name")
  var responseFileName = Request.ServerVariables ("HTTP_BITS-Response-DataFile-Name")
  var requestStream
  var responseStream
  var ForReading = 1
  var ForWriting = 2
  var TristateUseDefault = -2

  //Open the upload data file as text stream for reading.
  requestStream = fso.OpenTextFile(requestFileName, ForReading, false, TristateUseDefault);

  //Do something with the uploaded data.

  //Close the upload stream.
  requestStream.Close()

  //Open response data file as text stream for writing.
  responseStream = fso.OpenTextFile(responseFileName, ForWriting, true, TristateUseDefault);

  //Write a response to the response file.

  //Close the response text stream
  responseStream.Close()
```



如果您想要使用不同于位-回應-資料檔案名稱中所指定的回應檔，請呼叫 **AddHeader** 方法來加入 Bits-靜態-回應 URL，如下列範例所示。 如果您指定不同的回應檔，請勿建立以位-回應-資料檔案名稱指定的回應檔。


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




