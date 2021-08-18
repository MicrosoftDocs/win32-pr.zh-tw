---
title: 'IPropertyFilter NestingDepth 屬性 (WdsSharedIDL .h) '
description: 篩選一組嵌套括弧內的深度。
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- NestingDepth 屬性舊版 Windows 環境功能
- NestingDepth 屬性舊版 Windows 環境功能，IPropertyFilter 介面
- IPropertyFilter 介面舊版 Windows 環境功能，NestingDepth 屬性
topic_type:
- apiref
api_name:
- IPropertyFilter.NestingDepth
- IPropertyFilter.get_NestingDepth
- IPropertyFilter.put_NestingDepth
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2499d7a3d5505f4cb428cbc8831ec0ea4e0a71843693f5a8ba1250995071df32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481206"
---
# <a name="ipropertyfilternestingdepth-property"></a>IPropertyFilter：： NestingDepth 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

篩選一組嵌套括弧內的深度。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_NestingDepth(
  [in]          long depth
);

HRESULT get_NestingDepth(
  [out, retval] long *depth
);
```



## <a name="property-value"></a>屬性值

設定表示嵌套括弧深度的數位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





