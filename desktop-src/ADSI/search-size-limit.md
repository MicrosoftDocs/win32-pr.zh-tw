---
title: 搜尋大小限制
description: 若要減少記憶體需求，用戶端可以專注于從伺服器傳回的少數物件，並忽略結果集的其餘部分。
ms.assetid: 675a4931-dfa4-4948-936b-dee27add530c
ms.tgt_platform: multiple
keywords:
- 搜尋大小限制 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a48961532891f6573ccf8cb230117fad76daef95c57559e672eae93f022caf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763448"
---
# <a name="search-size-limit"></a>搜尋大小限制

若要減少記憶體需求，用戶端可以專注于從伺服器傳回的少數物件，並忽略結果集的其餘部分。 為了達成此目的，用戶端會指定搜尋大小限制和其他適當的搜尋準則。 例如，如果目錄儲存學校學區的測試分數，您可以藉由指定10和遞減排序次序的大小限制，查詢具有最高測試分數的前十名學生。

如需有關搭配特定搜尋介面使用 [搜尋大小限制] 選項的詳細資訊，請參閱：

-   [使用 >idirectorysearch 的大小限制](size-limit-with-idirectorysearch.md)
-   [使用 ActiveX Data Objects 搜尋](searching-with-activex-data-objects-ado.md)
-   [使用 OLE DB 搜尋](searching-with-ole-db.md)

 

 




