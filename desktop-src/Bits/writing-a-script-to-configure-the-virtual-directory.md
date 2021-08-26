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
ms.openlocfilehash: b9ea1de5a0b9f7be9598a4011cbb6cd76f49e6d4bcc3d468093be1479ee2b59e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004598"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a>撰寫腳本來設定虛擬目錄

您可以使用預設的 BITS IIS 屬性值，將檔案上傳至伺服器。 上傳檔案會寫入至作業的遠端檔案名中指定的 URL。 若要將檔案上傳至伺服器應用程式並接收回複，請將 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性變更為以傳址方式傳送資料 (將包含資料) 或依值傳送的檔案名， (在要求) 的主體中傳送資料。

如需您可以修改之屬性的清單和說明，請參閱 [BITS IIS 擴充功能屬性](bits-iis-extension-properties.md)。 使用 [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) 介面的方法來啟用和停用用於上傳的虛擬目錄。

下列範例顯示如何使用 Windows 腳本主機來建立、設定和啟用用於 BITS 上傳的 IIS 虛擬目錄。


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



若要變更先前的範例以將資料上傳至伺服器應用程式，請在 **SetInfo** 之前加入下列程式碼。


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



上傳檔案的位置會以位---------------Name 標頭傳遞至伺服器應用程式 myasp。 若要接收要求主體中的上傳檔案，請將 [BITSServerNotificationType](bits-iis-extension-properties.md) 屬性設定為2。

如需在伺服器應用程式中接收上傳資料的詳細資訊，請參閱 [使用 BITS 通知要求/回應標頭](using-bits-notification-request-response-headers.md)。

 

 




