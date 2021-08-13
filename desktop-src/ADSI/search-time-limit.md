---
title: 搜尋時間限制
description: 當您在繁重工作負載的伺服器上要求搜尋時，您可能會想要指示伺服器將搜尋限制在指定的時間限制。
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- 搜尋時間限制 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b666b41db67872cd418cca2d4ef2e3d766fbc1a1d1c1a2d9945eec7dfceb2429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690513"
---
# <a name="search-time-limit"></a>搜尋時間限制

當您在繁重工作負載的伺服器上要求搜尋時，您可能會想要指示伺服器將搜尋限制在指定的時間限制。 例如，若要執行應用程式以在執行接近容量的伺服器上產生每週報表，並避免將 CPU 時間最大化並防止其他作業執行，您可以將搜尋時間設定為較小的值，並在稍後無法產生報表時重新執行應用程式。

有些伺服器可能會強加自己的系統管理時間限制。 在這些情況下，如果您指定的搜尋時間限制值大於管理時間限制，伺服器會忽略您的規格，並改為使用其內部管理時間限制。

如需有關使用 [搜尋時間限制] 選項搭配特定搜尋介面的詳細資訊，請參閱：

-   [使用 >idirectorysearch 的伺服器時間限制](server-time-limit-with-idirectorysearch.md)
-   [使用 ActiveX Data Objects 搜尋](searching-with-activex-data-objects-ado.md)
-   [使用 OLE DB 搜尋](searching-with-ole-db.md)

 

 




