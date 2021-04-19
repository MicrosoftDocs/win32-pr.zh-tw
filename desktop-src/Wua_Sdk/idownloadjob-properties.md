---
description: IDownloadJob 介面會定義下列屬性。
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: IDownloadJob 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981142"
---
# <a name="idownloadjob-properties"></a>IDownloadJob 屬性

[**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob)介面會定義下列屬性。



| 屬性                                        | 描述                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | 取得傳遞至 [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) 方法的呼叫端特定狀態物件。           |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | 取得設定，指出是否已完全處理對 [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) 的呼叫。 |
| [**更新**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | 取得介面，其中包含在下載中指定之更新的唯讀集合。                                                  |



 

 

 



