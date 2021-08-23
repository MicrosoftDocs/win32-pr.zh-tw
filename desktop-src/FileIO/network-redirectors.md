---
description: 描述網路重新導向程式的功能。
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: 網路重定向器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed44bb8479c4aea5056b667688cb27ae0f1fe1ebf4f43d066a49143d5bfeadc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951077"
---
# <a name="network-redirectors"></a>網路重定向器

網路重新導向器是一種檔案系統驅動程式 (或 FSD) ，其功能如下：

-   做為網路 i/o 作業的用戶端，方法是將 i/o 要求傳送到伺服器，並處理來自伺服器的回應。
-   做為網路 i/o 作業的伺服器，方法是接收來自伺服器的 i/o 要求並處理要求。

它會執行所有與伺服器的低層級互動，以解析應用程式提供的檔案名與遠端伺服器上的資源位置。 如此一來，重新導向器可讓應用程式存取和管理遠端伺服器上的資源，就好像它們位於本機電腦上一樣。

重定向器完全在核心模式下運作。 這可提供下列優於使用者模式替代專案的效能優勢：

-   它可以與伺服器上執行的核心模式 FSDs （例如伺服器 FSD）互動，而不需要使用者對核心模式和核心對使用者模式內容切換。
-   它可以在核心模式中與伺服器上的快取管理員互動，以快取伺服器快取管理員在用戶端上傳送的 i/o 資料。
-   API 函式自訂-針對遠端 i/o 要求進行自訂，並不需要變更標準檔案 i/o 函數來提供此功能。

 

 



