---
description: 下列通知是由 SetupIterateCabinet 傳送。 如需有關通知格式和使用的詳細資訊，請參閱通知。
ms.assetid: 5a362a93-ebe8-4995-aacc-13ee10d3407a
title: 封包檔通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3e4eb7645fc3603f026db6bde3ce92f2ed2ce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970591"
---
# <a name="cabinet-file-notifications"></a>封包檔通知

下列通知是由 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)傳送。 如需有關通知格式和使用的詳細資訊，請參閱 [通知](notifications.md)。



| 通知                                                        | Description                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ FILEEXTRACTED**](spfilenotify-fileextracted.md)   | 已從封包解壓縮檔案。                                  |
| [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)   | 在封包中遇到檔案，應用程式是否要將它解壓縮？ |
| [**SPFILENOTIFY \_ NEEDNEWCABINET**](spfilenotify-neednewcabinet.md) | 目前的檔案會在下一個封包中繼續。                             |



 

 

 



