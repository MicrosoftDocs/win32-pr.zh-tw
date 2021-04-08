---
title: 依範圍或輸入網域來搜尋群組
description: 在 Windows 2000 網域中，有一個名為 [群組] 的類別，用於所有群組範圍 (網域本機、全域、通用) 和類型 (安全性、散發) 。
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- 依網域 AD 中的範圍或類型搜尋群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9aae5e2c7be7b9cba590f9bc80f0517bca918
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681639"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a>依範圍或輸入網域來搜尋群組

在 Windows 2000 網域中，有一個名為 [ [**群組**](/windows/desktop/ADSchema/c-group) ] 的類別，用於所有群組範圍 (網域本機、全域、通用) 和類型 (安全性、散發) 。 Group 物件的 [**groupType**](/windows/desktop/ADSchema/a-grouptype) 屬性會指定群組類型和範圍。

若要使用類型或範圍來搜尋 Windows 2000 網域上的群組，請使用包含 [**groupType**](/windows/desktop/ADSchema/a-grouptype) 屬性之相符規則的篩選準則。 如需相符規則的詳細資訊，請參閱 [搜尋篩選語法](/windows/desktop/ADSI/search-filter-syntax)。

如需詳細資訊和示範如何在定義域中搜尋群組的程式碼範例，請參閱 [在網域中搜尋群組的範例程式碼](example-code-for-performing-a-query-in-a-domain.md)。

## <a name="example-ldap-query-strings"></a>範例 LDAP 查詢字串

下列查詢字串範例顯示如何建立用來搜尋或篩選特定群組類型的 LDAP 查詢字串。

下列查詢字串會搜尋安全性群組。 此範例使用 "-2147483648" 做為 **ADS \_ 群組 \_ 類型 \_ 安全性 \_ 啟用** 旗標的十進位對等專案。


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



下列查詢字串會搜尋通用通訊群組;亦即，包含 **ads \_ 群組 \_ 類型 \_ 通用 \_ 組** 旗標的群組，且不包含 **ads \_ 群組 \_ 類型 \_ 安全性 \_ 啟用** 旗標。 此範例會使用 "8" 作為 **ads \_ 群組 \_ 類型 \_ 通用 \_ 組類型** 的十進位對等專案，並使用 "-2147483648" 做為 **ads \_ 群組 \_ 類型 \_ 安全性 \_ 啟用** 旗標的十進位對等專案。


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 