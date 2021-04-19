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
ms.openlocfilehash: 26d564e0a7bb8a10b44e2957f26aa20a07afa535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980174"
---
# <a name="resultsdisplaystyle-enumeration"></a>ResultsDisplayStyle 列舉

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

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
| Idl<br/> | <dl> <dt>WdsView .idl</dt> </dl> |



 

 





