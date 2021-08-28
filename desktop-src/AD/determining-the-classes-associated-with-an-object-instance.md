---
title: 判斷與物件實例相關聯的類別
description: Active Directory Domain Services 中的每個物件都有兩個屬性，其值可識別物件為其實例的物件類別階層架構。
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af65b5e1abf7f0bc68ae115cb409d2cdb556e08
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471494"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a>判斷與物件實例相關聯的類別

Active Directory Domain Services 中的每個物件都有兩個屬性，其值可識別物件為其實例的物件類別階層架構。




| 屬性 | 描述 | 
|-----------|-------------|
| <strong>structuralObjectClass</strong> | 識別物件為其實例的結構化和抽象類別。 例如，使用者物件的值可以是：<ul><li><strong>top</strong></li><li><strong>人</strong></li><li><strong>organizationalPerson</strong></li><li><strong>user</strong></li></ul> | 
| <strong>objectClass</strong> | 識別包含在 <strong>structuralObjectClass</strong>中的類別，再加上任何動態附加的輔助類別。 例如，如果將「車輛」輔助類別附加至使用者物件，這些值可以是：<ul><li><strong>top</strong></li><li><strong>車輛</strong></li><li><strong>人</strong></li><li><strong>organizationalPerson</strong></li><li><strong>user</strong></li></ul> | 




 

請注意，這兩個屬性都不包括以靜態方式連結化物件為實例之物件類別的輔助類別。 例如， **securityPrincipal** 輔助類別會以靜態方式連結至 **使用者** 類別，因為它包含在使用者 **classSchema** 物件的 **systemAuxiliaryClass** 值中。它不會包含在 user 類別實例的 **objectClass** 或 **structuralObjectClass** 屬性中。

 

 




