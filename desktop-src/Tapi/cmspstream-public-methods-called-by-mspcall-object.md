---
description: 下列清單包含 MSPCall 物件所呼叫的 CMSPStream 方法。
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: MSPCall 物件呼叫的 CMSPStream 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987616"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a>CMSPStream 由 MSPCall 物件呼叫的公用方法



| CMSPStream 公用方法                                 | Description                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Init**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | 建立資料流程時由 **MSPCall** 呼叫。                                   |
| [**關閉**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | 由 **MSPCall** 呼叫以取消選取所有的終端物件，並釋放呼叫物件。 |
| [**GetState**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | 由 MSPCall 物件呼叫，以取得資料流程的目前狀態。                   |
| [**HandleTSPData**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | 衍生的呼叫物件可以呼叫這個方法，讓資料流程處理 TSP 命令。     |
| [**ProcessGraphEvent**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | 由 MSPCall 物件呼叫，讓資料流程處理圖形事件。                     |



 

 

 



