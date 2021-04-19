---
title: HeaderDisplayStyle 列舉
description: 由 IResultsViewer HeaderStyle 用來設定或傳回目前的標頭樣式。
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- HeaderDisplayStyle 列舉舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994077"
---
# <a name="headerdisplaystyle-enumeration"></a>HeaderDisplayStyle 列舉

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

由 [**IResultsViewer：： HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) 用來設定或傳回目前的標頭樣式。

## <a name="syntax"></a>Syntax


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**
</dt> <dd>

指出或設定完整標頭的使用。

</dd> <dt>

<span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**
</dt> <dd>

指出或設定壓縮標頭的使用。

</dd> <dt>

<span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**NoHeader**
</dt> <dd>

表示或設定不使用標頭。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>WdsView .idl</dt> </dl> |



 

 





