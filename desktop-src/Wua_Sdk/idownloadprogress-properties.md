---
description: IDownloadProgress 介面會定義下列屬性。
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: IDownloadProgress 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943484"
---
# <a name="idownloadprogress-properties"></a>IDownloadProgress 屬性

[**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress)介面會定義下列屬性。



| 屬性                                                                               | 描述                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CurrentUpdateBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | 取得字串，這個字串會指定要下載的內容檔案或正在下載之更新檔案的資料量（以位元組為單位）。  |
| [**CurrentUpdateBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | 取得字串，這個字串會評估應為所下載之更新內容檔案或檔案所傳送的資料量（以位元組為單位）。 |
| [**CurrentUpdateDownloadPhase**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | 取得 [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) 列舉值，這個值會指定目前進行中之下載的階段。          |
| [**CurrentUpdateIndex**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | 取得以零為基底的索引值，這個值會指定在選取多個更新時，目前正在下載的更新。             |
| [**CurrentUpdatePercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | 取得已下載之目前更新百分比的估計值。                                                               |
| [**PercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | 取得已下載的所有更新百分比的估計值。                                                                 |
| [**TotalBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | 取得字串，這個字串會指定已下載的總數據量（以位元組為單位）。                                                        |
| [**TotalBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | 取得字串，表示將下載的總數據量（以位元組為單位）。                                        |



 

 

 



