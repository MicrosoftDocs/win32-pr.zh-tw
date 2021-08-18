---
title: Wide-Character 類型
description: Microsoft RPC 支援寬字元類型 wchar \_ t。
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eff57cf22e4836032acb59e1585da15285f55718b6c5b91733b1955ea85072a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010396"
---
# <a name="wide-character-types"></a>Wide-Character 類型

Microsoft RPC 支援寬字元類型 [**wchar \_ t**](/windows/desktop/Midl/wchar-t)。 寬字元類型會針對每個字元使用2個位元組。 ANSI C 語言定義可讓您將長字元和長字串初始化為：

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 