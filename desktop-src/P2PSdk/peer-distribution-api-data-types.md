---
description: 對等散發 API 會定義下列資料類型。
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: '對等散發 API 資料類型 (Peerdist. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001713"
---
# <a name="peer-distribution-api-data-types"></a>對等散發 API 資料類型

對等散發 API 會定義下列資料類型。


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| 資料類型                                                                                                                     | 描述                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**PEERDIST \_ 實例 \_ 控制碼**          | 與對等散發實例相關聯的控制碼。 這個控制碼是由 [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)所建立，並用於大部分的對等散發作業。<br/>                                          |
| <span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**PEERDIST \_ 內容 \_ 控制碼**             | 與內容相關聯的控制碼。 這個控制碼是由 [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) 所建立，並且會在開啟、關閉、新增或發佈內容時參考。<br/>                     |
| <span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**PEERDIST \_ CONTENTINFO \_ 控制碼** | 與內容資訊相關聯的控制碼。 這個控制碼是由 [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)所建立，並且會在抓取編碼的內容資訊時使用。<br/> |
| <span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**PEERDIST \_ 串流 \_ 控制碼**                | 與資料流程相關聯的控制碼。 這個控制碼是由 [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) 所建立，並且會在發行、關閉或新增至串流內容時參考。<br/>        |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows 7 Professional \[ desktop 應用程式\]<br/>                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Peerdist. h</dt> </dl> |



 

 




