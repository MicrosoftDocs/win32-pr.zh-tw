---
title: 伺服器應用程式的通知通訊協定
description: BITS 會使用 BITSServerNotificationType 屬性來判斷 BITS 如何將上傳檔案的內容傳送至伺服器應用程式。
ms.assetid: d5193d0c-3ab4-47ab-a570-fea2904a4371
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d35f6f5fec1a1de9ebd5c2c244a55bc1806b06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931957"
---
# <a name="notification-protocol-for-server-applications"></a>伺服器應用程式的通知通訊協定

BITS 會使用 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性來判斷 bits 如何將上傳檔案的內容傳送至伺服器應用程式。 如果 BITSServerNotificationType 屬性設定為1，BITS 會 [在標頭中傳遞上傳](#sending-the-location-of-the-upload-file-in-a-header)檔案的位置。 如果 BITSServerNotificationType 屬性設定為2，BITS 會 [在要求本文中傳遞上傳](#sending-the-upload-file-in-the-body-of-the-request)檔案的內容。

如需有關 BITS 如何處理伺服器應用程式錯誤的詳細資訊，請參閱 [處理伺服器應用程式錯誤](#handling-server-application-errors)。

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a>傳送標頭中的上傳檔案位置

如果 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性設定為1，則 BITS 會將上傳和回復檔案的位置傳遞至標頭中的伺服器應用程式。 伺服器應用程式會開啟上傳檔案、處理資料，然後產生回復檔。 根據預設，BITS 會在接收到伺服器應用程式的回應之後，從伺服器移除上傳和回復檔案。 若要讓 BITS 將上傳檔案複製到工作中的遠端檔案名所指定的位置，請在您的回應中包含位複製檔案到目的地的標頭。 如果您未包含標頭，而且想要儲存上傳和回復檔案，則必須先將上傳和回復檔案複製到新的位置，然後再回應。 下表顯示要求標頭。



| 要求標頭              | 描述                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| 位-原始-要求-URL   | 包含在作業中指定的遠端名稱。                                             |
| 位-要求-資料檔案名稱  | 包含所上傳資料的完整路徑。                                               |
| 位-回應-資料檔案名稱 | 包含 BITS 預期伺服器應用程式寫入回應的完整路徑。 |



 

下表顯示回應標頭。



| 回應標頭               | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BITS-靜態-回應-URL      | 選擇性。 包含絕對 URL (請勿指定靜態資料檔案) 的相對 URL，以做為回應使用。 BITS 用戶端必須能夠存取靜態資料檔案。 如果您使用此標頭，請勿建立在 BITS-Response-----Name 要求標頭中指定的回應檔。 請注意，BITS 不會為您刪除此檔案。<br/>                                                                                                           |
| 位-複製-檔案到目的地 | 選擇性。 根據預設，如果 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性設定為1或2，則 BITS 伺服器不會將上傳檔案複製到工作中遠端檔案名所指定的位置。 若要讓 BITS 將檔案複製到工作中的遠端檔案名所指定的位置，請傳送此回應標頭。 您可以指定任何值;BITS 不會使用此值。 請注意，遠端檔案路徑中的資料夾必須存在。 |



 

下列要求會顯示將上傳檔案的位置傳送至伺服器應用程式的位。

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
BITS-Request-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\request
BITS-Response-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\response
Content-Length: 0
```

以下顯示伺服器應用程式對 BITS 的回復;回復會放在 BITS-回應-資料檔案-名稱要求標頭所指定的檔案中。

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a>傳送要求主體中的上傳檔案

如果 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性設定為2，則 BITS 會將上傳檔案傳送到要求的主體中。 在要求本文中傳送上傳檔案可讓現有的腳本和應用程式以最少量的修改方式運作。 上傳檔案和回復檔案會分別在要求和回應中傳遞。 下表顯示要求標頭。



| 要求標頭            | 描述                                    |
|---------------------------|------------------------------------------------|
| 位-原始-要求-URL | 包含在作業中指定的遠端名稱。 |



 

下表顯示回應標頭。



| 回應標頭               | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BITS-靜態-回應-URL      | 選擇性。 包含絕對 URL (請勿指定靜態資料檔案) 的相對 URL，以做為回應使用。 BITS 用戶端必須能夠存取靜態資料檔案。 如果您使用此標頭，請勿在資料流程中包含回應。 請注意，BITS 不會為您刪除此檔案。<br/>                                                                                                                                      |
| 位-複製-檔案到目的地 | 選擇性。 如果 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性設定為1或2，則 BITS 伺服器不會將上傳檔案複製到工作中遠端檔案名所指定的位置。 若要讓 BITS 將檔案複製到遠端檔案名所指定的位置，請傳送此回應標頭。 您可以指定任何值;BITS 不會使用此值。 請注意，遠端檔案路徑中的資料夾必須存在。 |



 

下列要求會顯示在要求的主體中，將已上傳的檔案傳遞至伺服器應用程式的位。

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

下列回復顯示將回復資料傳遞給回應主體中之位的伺服器應用程式。

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a>處理伺服器應用程式錯誤

請參閱 [處理伺服器應用程式錯誤](handling-server-application-errors.md)。

 

 





