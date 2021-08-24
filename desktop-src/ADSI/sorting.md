---
title: '排序 (ADSI) '
description: 用戶端可以要求伺服器來排序結果集。
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555b4b6f1868b2e4fddc1891cdf349ef6f44bc47dca6eb80e021ec49cb91b5d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082222"
---
# <a name="sorting-adsi"></a>排序 (ADSI) 

用戶端可以要求伺服器來排序結果集。 您可以指定：

-   排序次序：可以指定遞增或遞減排序次序。
-   排序屬性：您可以在排序字串中指定多個屬性。 例如，依姓氏、名字和名字排序。

當您指定排序次序時，您應該嘗試使用其中一個索引屬性。 否則，伺服器必須先計算完整的結果集，才能將它傳送至用戶端。 即使您已要求分頁搜尋並指定頁面大小，也是如此。

> [!Note]  
> 並非所有目錄伺服器都支援多個屬性排序或排序次序。

 

 

 




