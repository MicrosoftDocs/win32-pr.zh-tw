---
description: 下列通知是由 SetupIterateCabinet 傳送。 如需有關通知格式和使用的詳細資訊，請參閱通知。
ms.assetid: 5a362a93-ebe8-4995-aacc-13ee10d3407a
title: 封包檔通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47018d9fda41e74dac9b8e4896674cbf21ed5ecd4a915d0c86da14d9787030a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117966356"
---
# <a name="cabinet-file-notifications"></a>封包檔通知

下列通知是由 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)傳送。 如需有關通知格式和使用的詳細資訊，請參閱 [通知](notifications.md)。



| 通知                                                        | 描述                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ FILEEXTRACTED**](spfilenotify-fileextracted.md)   | 已從封包解壓縮檔案。                                  |
| [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)   | 在封包中遇到檔案，應用程式是否要將它解壓縮？ |
| [**SPFILENOTIFY \_ NEEDNEWCABINET**](spfilenotify-neednewcabinet.md) | 目前的檔案會在下一個封包中繼續。                             |



 

 

 



