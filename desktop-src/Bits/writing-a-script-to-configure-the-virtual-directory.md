---
title: 撰寫腳本來設定虛擬目錄
description: 撰寫腳本來設定虛擬目錄
ms.assetid: 0324fbc8-1d64-454c-b021-4e010edcac8d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae23a33c2c91dc0a141c6f377daf89708499aae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931911"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a><span data-ttu-id="9a407-103">撰寫腳本來設定虛擬目錄</span><span class="sxs-lookup"><span data-stu-id="9a407-103">Writing a Script to Configure the Virtual Directory</span></span>

<span data-ttu-id="9a407-104">您可以使用預設的 BITS IIS 屬性值，將檔案上傳至伺服器。</span><span class="sxs-lookup"><span data-stu-id="9a407-104">You can use the default BITS IIS property values to upload a file to the server.</span></span> <span data-ttu-id="9a407-105">上傳檔案會寫入至作業的遠端檔案名中指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="9a407-105">The upload file is written to the URL as specified in the remote file name of the job.</span></span> <span data-ttu-id="9a407-106">若要將檔案上傳至伺服器應用程式並接收回複，請將 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性變更為以傳址方式傳送資料 (將包含資料) 或依值傳送的檔案名， (在要求) 的主體中傳送資料。</span><span class="sxs-lookup"><span data-stu-id="9a407-106">To upload the file to a server application and receive a reply, change the [BITSServerNotificationType](bits-iis-extension-properties.md) property to send the data by reference (sends the name of the file that contains the data) or by value (sends the data in the body of the request).</span></span>

<span data-ttu-id="9a407-107">如需您可以修改之屬性的清單和說明，請參閱 [BITS IIS 擴充功能屬性](bits-iis-extension-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="9a407-107">For a list and description of the properties that you can modify, see [BITS IIS Extension Properties](bits-iis-extension-properties.md).</span></span> <span data-ttu-id="9a407-108">使用 [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) 介面的方法來啟用和停用用於上傳的虛擬目錄。</span><span class="sxs-lookup"><span data-stu-id="9a407-108">Use the methods of the [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) interface to enable and disable the virtual directory for uploads.</span></span>

<span data-ttu-id="9a407-109">下列範例示範如何使用 Windows Script Host 來建立、設定和啟用用於 BITS 上傳的 IIS 虛擬目錄。</span><span class="sxs-lookup"><span data-stu-id="9a407-109">The following example shows how to use Windows Script Host to create, configure, and enable an IIS virtual directory for BITS uploads.</span></span>


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

//Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



<span data-ttu-id="9a407-110">若要變更先前的範例以將資料上傳至伺服器應用程式，請在 **SetInfo** 之前加入下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="9a407-110">To change the previous example to upload the data to a server application, add the following code before **SetInfo**.</span></span>


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



<span data-ttu-id="9a407-111">上傳檔案的位置會以位---------------Name 標頭傳遞至伺服器應用程式 myasp。</span><span class="sxs-lookup"><span data-stu-id="9a407-111">The location of the upload file is passed to the server application, myasp.asp, in the BITS-Request-DataFile-Name header.</span></span> <span data-ttu-id="9a407-112">若要接收要求主體中的上傳檔案，請將 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性設定為2。</span><span class="sxs-lookup"><span data-stu-id="9a407-112">To receive the upload file in the body of the request, set the [BITSServerNotificationType](bits-iis-extension-properties.md) property to 2.</span></span>

<span data-ttu-id="9a407-113">如需在伺服器應用程式中接收上傳資料的詳細資訊，請參閱 [使用 BITS 通知要求/回應標頭](using-bits-notification-request-response-headers.md)。</span><span class="sxs-lookup"><span data-stu-id="9a407-113">For information on receiving the upload data in your server application, see [Using BITS Notification Request/Response Headers](using-bits-notification-request-response-headers.md).</span></span>

 

 




