---
description: 在使用預設佇列回呼常式之前，您可以在認可檔案佇列時將它指定為回呼常式，或是從自訂回呼常式呼叫它，就必須將它初始化。
ms.assetid: e25a9787-a4a3-4d06-bf55-f6f7cfb23481
title: 初始化和終止回呼內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03cb4c144cb9069d395ccd688e2a172680df8a12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994414"
---
# <a name="initializing-and-terminating-the-callback-context"></a>初始化和終止回呼內容

在使用預設佇列回呼常式之前，您可以在認可檔案佇列時將它指定為回呼常式，或是從自訂回呼常式呼叫它，就必須將它初始化。

[**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)函式會建立預設佇列回呼常式所使用的內容結構。 它會傳回該結構的 void 指標。 此結構對於預設回呼常式的作業而言是不可或缺的，必須傳遞至回呼常式。 您可以藉由指定 void 指標做為 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)呼叫中的內容，或在從自訂回呼常式呼叫 [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) 時，指定 void 指標做為內容參數。 安裝應用程式不得變更或參考此內容結構。

[**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)函式也會初始化預設佇列回呼常式的內容，但它會指定第二個視窗，以便每次佇列傳送通知時，接收呼叫端指定的進度訊息。 這可讓您使用預設的 [提示] 和 [錯誤] 對話方塊，也可以在第二個視窗中內嵌進度列（例如，在安裝精靈的頁面中）。

無論您是否使用 [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) 或 [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)初始化預設佇列回呼常式所使用的內容，在佇列作業完成處理之後，請呼叫 [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) 來釋放在初始化內容結構時所配置的資源。

 

 



