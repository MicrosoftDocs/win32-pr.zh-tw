---
title: ResultsDisplayStyle 列舉
description: 由 IResultsViewer ResultsStyle 用來設定或決定結果的顯示方式。
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- ResultsDisplayStyle 列舉舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- ResultsDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a045765b53f29e978c286a14a1d82b86ffb21b5046dee606029a957ee0434c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726520"
---
# <a name="resultsdisplaystyle-enumeration"></a>ResultsDisplayStyle 列舉

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

由 [**IResultsViewer：： ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) 用來設定或決定結果的顯示方式。

## <a name="syntax"></a>Syntax


```C++
typedef enum ResultsDisplayStyleEnum { 
  SmallIconResults  = 0,
  LargeIconResults  = 1
} ResultsDisplayStyle;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**
</dt> <dd>

表示以小圖示顯示結果。

</dd> <dt>

<span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**
</dt> <dd>

指出結果會顯示為大型圖示。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>WdsView .idl</dt> </dl> |



 

 





