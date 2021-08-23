---
description: 命名 mailslots，並將訊息放入 mailslots。
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: 郵筒名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f96cc5300b3472abe7d6e824266bd0abd0e7b668e38f9f3462eee3cbf3dfb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716898"
---
# <a name="mailslot-names"></a>郵筒名稱

當進程建立信箱時，mailslot 名稱必須具有下列格式。

\\\\.\\郵筒 \\ \[ *路徑* \\ \] *名稱*

郵筒名稱需要下列元素：兩個反斜線來開始名稱、句號、句點之後的反斜線、"郵筒" 和 "尾端反斜線" 一字。 名稱不區分大小寫。 郵筒名稱前面可以有一個路徑，其中包含一個或多個目錄的名稱（以反斜線分隔）。 例如，如果使用者預期來自 Bob、Pete 和 Sue 之稅金的訊息，使用者的郵筒應用程式可能會允許使用者為每個寄件者建立個別的 mailslots，如下所示：<dl> \\\\.\\郵筒 \\ \\ bobs-machine \_ 批註  
\\\\.\\郵筒 \\ \\ petes \_ 批註  
\\\\.\\郵筒 \\ \\ 使用 \_ 批註  
</dl>

為了將訊息放入郵筒，進程會依名稱開啟信箱。 若要寫入本機電腦上的信箱，處理常式可以使用具有相同表單的郵筒名稱來建立郵筒。 不過，這種情況相當罕見。 更頻繁地，您可以使用下列格式來寫入特定遠端電腦上的信箱：

\\\\*ComputerName* \\郵筒 \\ \[ *路徑* \\ \] *名稱*

若要使用指定的名稱將訊息放入指定網域中的每個信箱，請使用下列格式：

\\\\*DomainName* \\郵筒 \\ \[ *路徑* \\ \] *名稱*

若要將訊息放入系統的主要網域中具有指定名稱的每個信箱，請使用下列格式：

\\\\\*\\郵筒 \\ \[ *路徑* \\ \] *名稱*

 

 



