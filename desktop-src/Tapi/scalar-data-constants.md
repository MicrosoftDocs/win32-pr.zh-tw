---
description: 針對可延伸的純量資料常數，服務提供者廠商可以在指定的範圍內定義新值。
ms.assetid: 62280b71-9bec-4a9d-abd2-d3e1c2cee43f
title: 純量資料常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 815288ca4a22da741e5b98257ae50732f818b466404a95712ee74756785fd699
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773308"
---
# <a name="scalar-data-constants"></a>純量資料常數

針對可延伸的純量資料常數，服務提供者廠商可以在指定的範圍內定義新值。 因為大部分的資料常數都是 **DWORD**，所以範圍0X00000000 到0x7fffffff 通常會保留給一般未來的延伸模組，而透過0xffffffff 的0x80000000 則適用于供應商專屬的延伸模組。 假設廠商會定義值，這些值是 API 所定義之資料類型的自然延伸。

 

 



