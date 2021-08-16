---
description: LIKE 運算子會判斷字元字串是否符合指定的模式。
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: LIKE 運算子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e5df500091fac8b15bcdcb448b7a97fc00dc62807ba854757e447f07e6f4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317867"
---
# <a name="like-operator"></a>LIKE 運算子

LIKE 運算子會判斷字元字串是否符合指定的模式。 指定的模式可以剛好包含要比對的字元，或可包含中繼字元。 實際上，LIKE 運算子會使用下表中的萬用字元來比對子字串。



| 字元       | 描述                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[ \]           | 指定範圍內的任何一個字元 (\[ a-f \]) 或設定 (\[ abcdef \]) 。                                                                                                                 |
| ^               | 不在範圍內的任何一個字元 (\[ ^ a-f \]) 或設定 (\[ ^ abcdef \] 。 )                                                                                                                      |
| %               | 0 () 零或多個字元的任何字串。 下列範例會尋找在類別名稱中任何位置都找到 "Win" 的所有實例： `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"` |
| \_ (底線)  | 任何一個字元。 在查詢字串中使用的任何常值底線都必須透過將其放在 \[ \] (方括弧) 內進行轉義。                                                             |



 

例如，下列 Power shell 程式碼會抓取 **名稱** 屬性以 **FirstName** 開頭的 **Win32 \_ 作業系統** 類別的所有實例：

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

因為底線是中繼字元，所以如果查詢目標有底線，則 " \[ \] " escape 字元必須括住。 例如，您可以查詢名稱中有雙底線的所有類別。

若要在名稱中找出具有雙底線的所有類別，您必須使用 (方括弧) 來將這兩個底線進行 escape \[ \] ，例如：

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

您可以使用 NOT 來否定 LIKE 語句;若要這樣做，請務必將不直接放在功能變數名稱前面。 例如：

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WQL 運算子](wql-operators.md)
</dt> </dl>

 

 



