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
# <a name="notification-protocol-for-server-applications"></a><span data-ttu-id="cf184-103">伺服器應用程式的通知通訊協定</span><span class="sxs-lookup"><span data-stu-id="cf184-103">Notification Protocol for Server Applications</span></span>

<span data-ttu-id="cf184-104">BITS 會使用 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性來判斷 bits 如何將上傳檔案的內容傳送至伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="cf184-104">BITS uses the [BITSServerNotificationType](bits-iis-extension-properties.md) property to determine how BITS sends the contents of the upload file to the server application.</span></span> <span data-ttu-id="cf184-105">如果 BITSServerNotificationType 屬性設定為1，BITS 會 [在標頭中傳遞上傳](#sending-the-location-of-the-upload-file-in-a-header)檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="cf184-105">If the BITSServerNotificationType property is set to 1, [BITS passes the location of the upload file in a header](#sending-the-location-of-the-upload-file-in-a-header).</span></span> <span data-ttu-id="cf184-106">如果 BITSServerNotificationType 屬性設定為2，BITS 會 [在要求本文中傳遞上傳](#sending-the-upload-file-in-the-body-of-the-request)檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="cf184-106">If the BITSServerNotificationType property is set to 2, [BITS passes the contents of the upload file in the body of the request](#sending-the-upload-file-in-the-body-of-the-request).</span></span>

<span data-ttu-id="cf184-107">如需有關 BITS 如何處理伺服器應用程式錯誤的詳細資訊，請參閱 [處理伺服器應用程式錯誤](#handling-server-application-errors)。</span><span class="sxs-lookup"><span data-stu-id="cf184-107">For details on how BITS handles errors from the server application, see [Handling server application errors](#handling-server-application-errors).</span></span>

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a><span data-ttu-id="cf184-108">傳送標頭中的上傳檔案位置</span><span class="sxs-lookup"><span data-stu-id="cf184-108">Sending the location of the upload file in a header</span></span>

<span data-ttu-id="cf184-109">如果 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性設定為1，則 BITS 會將上傳和回復檔案的位置傳遞至標頭中的伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="cf184-109">BITS passes the location of the upload and reply files to the server application in the headers if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1.</span></span> <span data-ttu-id="cf184-110">伺服器應用程式會開啟上傳檔案、處理資料，然後產生回復檔。</span><span class="sxs-lookup"><span data-stu-id="cf184-110">The server application opens the upload file, processes the data, and then generates the reply file.</span></span> <span data-ttu-id="cf184-111">根據預設，BITS 會在接收到伺服器應用程式的回應之後，從伺服器移除上傳和回復檔案。</span><span class="sxs-lookup"><span data-stu-id="cf184-111">By default, BITS removes the upload and reply files from the server after it receives the response from the server application.</span></span> <span data-ttu-id="cf184-112">若要讓 BITS 將上傳檔案複製到工作中的遠端檔案名所指定的位置，請在您的回應中包含位複製檔案到目的地的標頭。</span><span class="sxs-lookup"><span data-stu-id="cf184-112">To have BITS copy the upload file to the location specified by the remote file name in the job, include the BITS-Copy-File-To-Destination header in your response.</span></span> <span data-ttu-id="cf184-113">如果您未包含標頭，而且想要儲存上傳和回復檔案，則必須先將上傳和回復檔案複製到新的位置，然後再回應。</span><span class="sxs-lookup"><span data-stu-id="cf184-113">If you do not include the header and you want to save the upload and reply files, you must copy the upload and reply files to a new location before responding.</span></span> <span data-ttu-id="cf184-114">下表顯示要求標頭。</span><span class="sxs-lookup"><span data-stu-id="cf184-114">The following table shows the request headers.</span></span>



| <span data-ttu-id="cf184-115">要求標頭</span><span class="sxs-lookup"><span data-stu-id="cf184-115">Request header</span></span>              | <span data-ttu-id="cf184-116">描述</span><span class="sxs-lookup"><span data-stu-id="cf184-116">Description</span></span>                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf184-117">位-原始-要求-URL</span><span class="sxs-lookup"><span data-stu-id="cf184-117">BITS-Original-Request-URL</span></span>   | <span data-ttu-id="cf184-118">包含在作業中指定的遠端名稱。</span><span class="sxs-lookup"><span data-stu-id="cf184-118">Contains the remote name specified in the job.</span></span>                                             |
| <span data-ttu-id="cf184-119">位-要求-資料檔案名稱</span><span class="sxs-lookup"><span data-stu-id="cf184-119">BITS-Request-DataFile-Name</span></span>  | <span data-ttu-id="cf184-120">包含所上傳資料的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="cf184-120">Contains the full path to the uploaded data.</span></span>                                               |
| <span data-ttu-id="cf184-121">位-回應-資料檔案名稱</span><span class="sxs-lookup"><span data-stu-id="cf184-121">BITS-Response-DataFile-Name</span></span> | <span data-ttu-id="cf184-122">包含 BITS 預期伺服器應用程式寫入回應的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="cf184-122">Contains the full path to where BITS expects the server application to write the response.</span></span> |



 

<span data-ttu-id="cf184-123">下表顯示回應標頭。</span><span class="sxs-lookup"><span data-stu-id="cf184-123">The following table shows the response headers.</span></span>



| <span data-ttu-id="cf184-124">回應標頭</span><span class="sxs-lookup"><span data-stu-id="cf184-124">Response header</span></span>               | <span data-ttu-id="cf184-125">描述</span><span class="sxs-lookup"><span data-stu-id="cf184-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf184-126">BITS-靜態-回應-URL</span><span class="sxs-lookup"><span data-stu-id="cf184-126">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="cf184-127">選擇性。</span><span class="sxs-lookup"><span data-stu-id="cf184-127">Optional.</span></span> <span data-ttu-id="cf184-128">包含絕對 URL (請勿指定靜態資料檔案) 的相對 URL，以做為回應使用。</span><span class="sxs-lookup"><span data-stu-id="cf184-128">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="cf184-129">BITS 用戶端必須能夠存取靜態資料檔案。</span><span class="sxs-lookup"><span data-stu-id="cf184-129">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="cf184-130">如果您使用此標頭，請勿建立在 BITS-Response-----Name 要求標頭中指定的回應檔。</span><span class="sxs-lookup"><span data-stu-id="cf184-130">If you use this header, do not create the response file specified in the BITS-Response-DataFile-Name request header.</span></span> <span data-ttu-id="cf184-131">請注意，BITS 不會為您刪除此檔案。</span><span class="sxs-lookup"><span data-stu-id="cf184-131">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                           |
| <span data-ttu-id="cf184-132">位-複製-檔案到目的地</span><span class="sxs-lookup"><span data-stu-id="cf184-132">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="cf184-133">選擇性。</span><span class="sxs-lookup"><span data-stu-id="cf184-133">Optional.</span></span> <span data-ttu-id="cf184-134">根據預設，如果 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性設定為1或2，則 BITS 伺服器不會將上傳檔案複製到工作中遠端檔案名所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="cf184-134">By default, if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="cf184-135">若要讓 BITS 將檔案複製到工作中的遠端檔案名所指定的位置，請傳送此回應標頭。</span><span class="sxs-lookup"><span data-stu-id="cf184-135">To have BITS copy the file to the location specified by the remote file name in the job, send this response header.</span></span> <span data-ttu-id="cf184-136">您可以指定任何值;BITS 不會使用此值。</span><span class="sxs-lookup"><span data-stu-id="cf184-136">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="cf184-137">請注意，遠端檔案路徑中的資料夾必須存在。</span><span class="sxs-lookup"><span data-stu-id="cf184-137">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="cf184-138">下列要求會顯示將上傳檔案的位置傳送至伺服器應用程式的位。</span><span class="sxs-lookup"><span data-stu-id="cf184-138">The following request shows BITS sending the location of the upload file to the server application.</span></span>

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

<span data-ttu-id="cf184-139">以下顯示伺服器應用程式對 BITS 的回復;回復會放在 BITS-回應-資料檔案-名稱要求標頭所指定的檔案中。</span><span class="sxs-lookup"><span data-stu-id="cf184-139">The following shows the server application's reply to BITS; the reply is placed in the file specified by the BITS-Response-DataFile-Name request header.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a><span data-ttu-id="cf184-140">傳送要求主體中的上傳檔案</span><span class="sxs-lookup"><span data-stu-id="cf184-140">Sending the upload file in the body of the request</span></span>

<span data-ttu-id="cf184-141">如果 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性設定為2，則 BITS 會將上傳檔案傳送到要求的主體中。</span><span class="sxs-lookup"><span data-stu-id="cf184-141">BITS sends the upload file in the body of the request if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 2.</span></span> <span data-ttu-id="cf184-142">在要求本文中傳送上傳檔案可讓現有的腳本和應用程式以最少量的修改方式運作。</span><span class="sxs-lookup"><span data-stu-id="cf184-142">Sending the upload file in the body of the request lets existing scripts and applications work with minimal modifications.</span></span> <span data-ttu-id="cf184-143">上傳檔案和回復檔案會分別在要求和回應中傳遞。</span><span class="sxs-lookup"><span data-stu-id="cf184-143">The upload file and reply file are passed in the request and response, respectively.</span></span> <span data-ttu-id="cf184-144">下表顯示要求標頭。</span><span class="sxs-lookup"><span data-stu-id="cf184-144">The following table shows the request header.</span></span>



| <span data-ttu-id="cf184-145">要求標頭</span><span class="sxs-lookup"><span data-stu-id="cf184-145">Request header</span></span>            | <span data-ttu-id="cf184-146">描述</span><span class="sxs-lookup"><span data-stu-id="cf184-146">Description</span></span>                                    |
|---------------------------|------------------------------------------------|
| <span data-ttu-id="cf184-147">位-原始-要求-URL</span><span class="sxs-lookup"><span data-stu-id="cf184-147">BITS-Original-Request-URL</span></span> | <span data-ttu-id="cf184-148">包含在作業中指定的遠端名稱。</span><span class="sxs-lookup"><span data-stu-id="cf184-148">Contains the remote name specified in the job.</span></span> |



 

<span data-ttu-id="cf184-149">下表顯示回應標頭。</span><span class="sxs-lookup"><span data-stu-id="cf184-149">The following table shows the response headers.</span></span>



| <span data-ttu-id="cf184-150">回應標頭</span><span class="sxs-lookup"><span data-stu-id="cf184-150">Response header</span></span>               | <span data-ttu-id="cf184-151">描述</span><span class="sxs-lookup"><span data-stu-id="cf184-151">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf184-152">BITS-靜態-回應-URL</span><span class="sxs-lookup"><span data-stu-id="cf184-152">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="cf184-153">選擇性。</span><span class="sxs-lookup"><span data-stu-id="cf184-153">Optional.</span></span> <span data-ttu-id="cf184-154">包含絕對 URL (請勿指定靜態資料檔案) 的相對 URL，以做為回應使用。</span><span class="sxs-lookup"><span data-stu-id="cf184-154">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="cf184-155">BITS 用戶端必須能夠存取靜態資料檔案。</span><span class="sxs-lookup"><span data-stu-id="cf184-155">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="cf184-156">如果您使用此標頭，請勿在資料流程中包含回應。</span><span class="sxs-lookup"><span data-stu-id="cf184-156">If you use this header, do not include the response in the stream.</span></span> <span data-ttu-id="cf184-157">請注意，BITS 不會為您刪除此檔案。</span><span class="sxs-lookup"><span data-stu-id="cf184-157">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="cf184-158">位-複製-檔案到目的地</span><span class="sxs-lookup"><span data-stu-id="cf184-158">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="cf184-159">選擇性。</span><span class="sxs-lookup"><span data-stu-id="cf184-159">Optional.</span></span> <span data-ttu-id="cf184-160">如果 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性設定為1或2，則 BITS 伺服器不會將上傳檔案複製到工作中遠端檔案名所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="cf184-160">If the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="cf184-161">若要讓 BITS 將檔案複製到遠端檔案名所指定的位置，請傳送此回應標頭。</span><span class="sxs-lookup"><span data-stu-id="cf184-161">To have BITS copy the file to the location specified by the remote file name, send this response header.</span></span> <span data-ttu-id="cf184-162">您可以指定任何值;BITS 不會使用此值。</span><span class="sxs-lookup"><span data-stu-id="cf184-162">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="cf184-163">請注意，遠端檔案路徑中的資料夾必須存在。</span><span class="sxs-lookup"><span data-stu-id="cf184-163">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="cf184-164">下列要求會顯示在要求的主體中，將已上傳的檔案傳遞至伺服器應用程式的位。</span><span class="sxs-lookup"><span data-stu-id="cf184-164">The following request shows BITS passing the uploaded file to the server application in the body of the request.</span></span>

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

<span data-ttu-id="cf184-165">下列回復顯示將回復資料傳遞給回應主體中之位的伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="cf184-165">The following reply shows the server application passing the reply data to BITS in the body of the response.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a><span data-ttu-id="cf184-166">處理伺服器應用程式錯誤</span><span class="sxs-lookup"><span data-stu-id="cf184-166">Handling server application errors</span></span>

<span data-ttu-id="cf184-167">請參閱 [處理伺服器應用程式錯誤](handling-server-application-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="cf184-167">See [Handling Server Application Errors](handling-server-application-errors.md).</span></span>

 

 





