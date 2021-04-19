---
description: 您可以指定預設佇列回呼常式來處理 SetupCommitFileQueue 所傳送的通知，也可以由根據預設佇列回呼常式功能建立的自訂回呼常式來呼叫它。
ms.assetid: df8ae7b5-f3a2-4343-a603-440ab5c02b88
title: 使用預設佇列回呼常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51bceadf309257b9faf2b3ce3b8a12771572664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975086"
---
# <a name="using-the-default-queue-callback-routine"></a>使用預設佇列回呼常式

您可以指定預設佇列回呼常式來處理 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)所傳送的通知，也可以由根據預設佇列回呼常式功能建立的自訂回呼常式來呼叫它。

下列各節說明如何初始化和終止預設佇列回呼常式所使用的內容。 這些章節也會說明如何搭配使用預設佇列回呼常式與 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 或自訂回呼常式。

-   [初始化和終止回呼內容](initializing-and-terminating-the-callback-context.md)
-   [呼叫預設佇列回呼常式](calling-the-default-queue-callback-routine.md)

 

 



