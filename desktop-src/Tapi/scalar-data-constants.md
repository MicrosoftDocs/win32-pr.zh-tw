---
description: 針對可延伸的純量資料常數，服務提供者廠商可以在指定的範圍內定義新值。
ms.assetid: 62280b71-9bec-4a9d-abd2-d3e1c2cee43f
title: 純量資料常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3187d2064501727614dfcbf0b8e11c136fea13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695840"
---
# <a name="scalar-data-constants"></a>純量資料常數

針對可延伸的純量資料常數，服務提供者廠商可以在指定的範圍內定義新值。 因為大部分的資料常數都是 **DWORD**，所以範圍0X00000000 到0x7fffffff 通常會保留給一般未來的延伸模組，而透過0xffffffff 的0x80000000 則適用于供應商專屬的延伸模組。 假設廠商會定義值，這些值是 API 所定義之資料類型的自然延伸。

 

 



