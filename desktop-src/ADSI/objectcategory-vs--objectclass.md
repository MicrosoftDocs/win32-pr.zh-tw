---
title: objectCategory 與 objectClass
description: ObjectCategory 和 objectClass 屬性都可以參考目錄物件的指定架構類別。
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- objectCategory 與 objectClass ADSI
- 屬性 ASI、搜尋 objectCategory 和 objectClass 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3833f8cf26cb2272fbe1e7c1063322f39a8c0147e4b22382d26067f90e72e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839218"
---
# <a name="objectcategory-vs-objectclass"></a>objectCategory 與 objectClass

**ObjectCategory** 和 **objectClass** 屬性都可以參考目錄物件的指定架構類別。 不過，兩者之間的語義有很大的差異。 「objectClass = 樂趣」指的是這類目錄物件，其中「樂趣」代表物件類別階層中的任何類別。 相反地，"objectCategory = 樂趣" 指的是這些目錄物件，其中「樂趣」會識別物件類別階層中的特定類別。

**objectClass** 可以接受多個值，而 **objectCategory** 會採用單一值。 因此， **objectCategory** 更適合用來比對目錄搜尋中的物件類型。 ADSI 使用這個作為預設比對準則。 使用一個 **objectClass** 的搜尋無法擴充至大型資料庫。 ADSI 支援 " (objectCategory = SomeDN) " 和 " (objectCategory = \_ \_ \_) 類別的 Ldap 顯示名稱 \_ " 語法。

唯一的例外是 LDAP 搜尋篩選「 (objectClass =) 」不 \* 會在物件類別上指定搜尋，而只會測試物件是否存在。

 

 




