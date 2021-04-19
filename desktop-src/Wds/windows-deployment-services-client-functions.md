---
title: Windows 部署服務用戶端函數
description: 下列函式會與 Windows 部署服務用戶端 API 搭配使用。
ms.assetid: 4cedd8a8-7f46-4229-9d96-58965b751e43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe124c6f02d12943d40fbc98af4a687d5b892f86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966821"
---
# <a name="windows-deployment-services-client-functions"></a>Windows 部署服務用戶端函數

下列函式會與 Windows 部署服務用戶端 API 搭配使用。



| 函式                                                                                 | 描述                                                                                                                            |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [*PFN \_ WdsCliCallback*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclicallback)                                          | 檔案或映射傳送期間的進度通知和錯誤訊息。                                                              |
| [*PFN \_ WdsCliTraceFunction*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclitracefunction)                                | 接收來自 WDS 用戶端的調試訊息。                                                                                       |
| [**WdsCliAuthorizeSession**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession)                                 | 將匿名會話轉換成經過驗證的會話。                                                                           |
| [**WdsCliCancelTransfer**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicanceltransfer)                                     | 取消 WDS 傳送作業。                                                                                                      |
| [**WdsCliClose**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliclose)                                                       | 關閉 WDS 會話或映射的控制碼，並釋放資源。                                                                      |
| [**WdsCliCreateSession**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession)                                       | 使用 WDS 伺服器啟動新的會話。                                                                                                |
| [**WdsCliFindFirstImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage)                                     | 開始列舉 WDS 伺服器上儲存的映射，並傳回參考第一個映射的 find 控制碼。                     |
| [**WdsCliFindNextImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage)                                       | 將尋找控制碼的參考前移至儲存在 WDS 伺服器上的下一個映射。                                                      |
| [**WdsCliFreeStringArray**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifreestringarray)                                   | 釋放 [**WdsCliObtainDriverPackages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages) 函式所配置的字串值陣列。 |
| [**WdsCliGetEnumerationFlags**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags)                           | 傳回目前影像控制碼的影像列舉旗標。                                                                       |
| [**WdsCliGetImageArchitecture**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture)                         | 傳回目前映射的處理器架構。                                                                              |
| [**WdsCliGetImageDescription**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription)                           | 傳回目前影像的描述。                                                                                          |
| [**WdsCliGetImageGroup**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup)                                       | 傳回目前映射的映射組名。                                                                                    |
| [**WdsCliGetImageHalName**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname)                                   | 傳回目前映射 (HAL) 名稱的硬體抽象層。                                                               |
| [**WdsCliGetImageHandleFromFindHandle**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromfindhandle)         | 傳回目前影像的影像控制碼。                                                                                         |
| [**WdsCliGetImageHandleFromTransferHandle**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromtransferhandle) | 從已完成的傳送控制碼傳回影像控制碼。                                                                              |
| [**WdsCliGetImageIndex**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex)                                       | 傳回目前影像的影像索引。                                                                                         |
| [**WdsCliGetImageLanguage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage)                                 | 傳回目前影像的預設語言。                                                                                     |
| [**WdsCliGetImageLanguages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages)                               | 傳回目前影像所支援的語言陣列。                                                                          |
| [**WdsCliGetImageLastModifiedTime**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime)                 | 傳回目前影像的上次修改時間。                                                                                  |
| [**WdsCliGetImageName**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename)                                         | 傳回目前影像的名稱。                                                                                                 |
| [**WdsCliGetImageNamespace**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagenamespace)                               | 傳回目前影像的名稱。                                                                                                 |
| [**WdsCliGetImagePath**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath)                                         | 傳回包含目前影像之影像檔案的路徑。                                                                    |
| [**WdsCliGetImageSize**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize)                                         | 傳回目前影像的大小。                                                                                                 |
| [**WdsCliGetImageVersion**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion)                                   | 傳回目前映射的版本。                                                                                              |
| [**WdsCliGetTransferSize**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligettransfersize)                                   | 傳回目前傳送的大小。                                                                                              |
| [**WdsCliInitializeLog**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog)                                       | 初始化用戶端的記錄檔。                                                                                                    |
| [**WdsCliLog**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclilog)                                                           | 將記錄檔事件傳送至 WDS 伺服器。                                                                                                   |
| [**WdsCliObtainDriverPackages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages)                         | 從 WDS 映射取得，驅動程式套件 (可在這部電腦上使用的 INF 檔案) 。                                           |
| [**WdsCliRegisterTrace**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliregistertrace)                                       | 註冊將接收偵錯工具訊息的回呼函數。                                                                    |
| [**WdsCliTransferFile**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferfile)                                         | 使用多播傳輸通訊協定，將檔案從 WDS 伺服器傳送至 WDS 用戶端。                                              |
| [**WdsCliTransferImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferimage)                                       | 從 WDS 伺服器傳輸映射。                                                                                                  |
| [**WdsCliWaitForTransfer**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliwaitfortransfer)                                   | 等候傳送完成。                                                                                                      |



 



| 函式                                                             | 描述                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WdsCliGetDriverQueryXml**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetdriverqueryxml)           | 產生 XML 字串，可用來查詢驅動程式套件的 WDS 伺服器。 從 Windows 8 和 Windows Server 2012 開始提供。               |
| [**WdsCliObtainDriverPackagesEx**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackagesex) | 取得適用于指定的 WDS 驅動程式查詢 XML (INF 檔案) 的驅動程式套件。 從 Windows 8 和 Windows Server 2012 開始提供。 |



 

 

 




