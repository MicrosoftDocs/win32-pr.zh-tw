---
title: CPROPS.Cpp
description: 在範例提供者元件中，可以在 cprops 中找到屬性快取執行的範例。 下表列出支援的方法。
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66394b7375779f50a97505128178ec35106187c076ca5d6741375a7f71b8ec46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428997"
---
# <a name="cpropscpp"></a>CPROPS.Cpp

在範例提供者元件中，可以在 cprops 中找到屬性快取執行的範例。 下表列出支援的方法。



| 方法                                           | 描述                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **CPropertyCache：： addproperty**                  | 藉由加入新的屬性快取來擴充它。                                                                      |
| **CPropertyCache::updateproperty**               | 查閱屬性，釋出其內容，並改用新的值;然後，將此屬性的快取標記為已變更。 |
| **CPropertyCache::findproperty**                 | 依名稱查閱此屬性;儲存其索引。                                                                      |
| **CPropertyCache：： getproperty**                  | 在快取中尋找屬性（如果有的話），否則呼叫 **GetInfo**。 設定索引，並複製新值。  |
| **CPropertyCache：:p utproperty**                  | 尋找屬性。 釋出，並放入新值。                                                       |
| **CPropertyCache::CPropertyCache**               | 標準的函式。                                                                                               |
| **CPropertyCache：： ~ CPropertyCache**              | 標準的函式。                                                                                                |
| **CPropertyCache::createpropertycache**          | 建立快取。                                                                                                   |
| **CPropertyCache::unboundgetproperty**           | 在快取中尋找屬性，並將它設定為這些值。                                                          |
| **CPropertyCache::SampleDSMarshallProperties**   | 封送處理屬性資料和值。                                                                                   |
| **CPropertyCache::marshallproperty**             | 封送處理屬性。                                                                                                 |
| **CPropertyCache::SampleDSUnMarshallProperties** | Unmarshal 屬性資料和值。                                                                                 |
| **CPropertyCache::unmarshallproperty**           | Unmarshal 屬性。                                                                                               |



 

 

 




