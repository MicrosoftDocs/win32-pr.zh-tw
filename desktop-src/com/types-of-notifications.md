---
title: 通知類型
description: 通知類型
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372463"
---
# <a name="types-of-notifications"></a>通知類型

通知分為三個群組：複合檔案、資料和查看。 物件會傳送複合檔案通知，以回應重新命名、儲存、關閉，或在連結的情況下，將其連結來源重新命名。 如您所預期，物件會傳送資料通知以回應其資料的變更，並傳送視圖通知以回應其簡報中的變更。 容器應用程式必須個別註冊這些通知類型，但全部都可由單一諮詢接收來處理。

複合檔案通知的所有容器、物件處理常式和連結化物件註冊。 一般容器也會註冊查看通知。 資料通知通常會同時傳送至連結化物件和物件處理常式。 特定用途的容器（例如呈現資料本身的容器），可能會因為接收資料通知而不是 view 通知而受益。 例如，具有資料表連結的內嵌圖表容器可以註冊資料通知。 因為資料表的變更會影響圖表，所以資料通知的接收會指示容器取得新的表格式資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[通知](notifications.md)
</dt> </dl>

 

 




