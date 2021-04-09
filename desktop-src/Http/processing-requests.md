---
title: 處理要求
description: 處理要求包含四個步驟。
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e820d425e44daab9d687d1d43b756b833582a092
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "103853231"
---
# <a name="processing-requests"></a>處理要求

處理要求包含四個步驟：

-   接收要求
-   處理要求
-   傳送回應
-   正在取消無法處理的要求

![顯示進程要求迴圈的圖表。](images/processloop.png)

## <a name="receiving-a-request"></a>接收要求

HTTP 伺服器 API 會提供一個要求結構來儲存剖析的連入要求。 此結構是由應用程式所配置，並在收到傳入要求時初始化。 應用程式會呼叫 [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) 函數來接收要求。 如果要求緩衝區太小而無法接收要求，應用程式可以增加緩衝區大小，然後再次呼叫 **HttpReceiveHttpRequest** ，以接收整個要求。

如果要求包含要接收的實體主體資料，則應用程式會在呼叫 [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)期間以 *pRequestBuffer* 參數傳回的要求識別碼來呼叫 [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) 。

## <a name="handling-the-request"></a>處理要求

應用程式會執行要求的應用程式特定處理，並會構成回應。 HTTP 伺服器 API 不會在此程式上強加任何時間。

## <a name="sending-the-response"></a>傳送回應

當應用程式完成處理要求並編寫回應時，它會呼叫 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) 函式來傳送回應。 如果回應包含要傳送的實體主體資料，則應用程式也會呼叫 [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)。

## <a name="canceling-requests"></a>取消要求

應用程式從呼叫 [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)收到要求識別碼之後，就可以在任何時候呼叫 [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest)來取消要求。

 

 




