---
title: 搜尋超時
description: 用戶端也可能會強制等候伺服器傳回結果集的時間限制。
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- 搜尋即時 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfdc63dd4490a840a16eb61598b2461c3e1a40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300059"
---
# <a name="search-time-out"></a>搜尋超時

用戶端也可能會強制等候伺服器傳回結果集的時間限制。 [搜尋超時] 選項的值會指定此限制。 當伺服器無法在指定的期間內回應查詢時，用戶端可以停止搜尋，稍後再試一次。

當用戶端要求非同步搜尋時，超時屬性很有用。 在非同步搜尋中，用戶端會提出要求，然後在等候伺服器傳回結果時，繼續執行其他工作。 伺服器可能會離線，而不會通知用戶端。 在此情況下，用戶端無法辨識伺服器是否仍在處理查詢，或是否已停止運作。 超時屬性可讓用戶端在這類實例中有一些控制權。

如需有關使用搜尋超時選項搭配特定搜尋介面的詳細資訊，請參閱：

-   [使用 >idirectorysearch 的用戶端時間限制](client-time-limit-with-idirectorysearch.md)
-   [使用 ActiveX Data Objects 搜尋](searching-with-activex-data-objects-ado.md)
-   [使用 OLE DB 搜尋](searching-with-ole-db.md)

 

 




