---
title: DownloadCollection 計數
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 Count 屬性會抓取集合中的暫止下載數目。
ms.assetid: 8f9245aa-6d92-4dd3-9b45-97ee37de680d
keywords:
- DownloadCollection Windows Media Player 計數
topic_type:
- apiref
api_name:
- DownloadCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95f161143cf599dcfbc71b2e55764009ec5d4e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995673"
---
# <a name="downloadcollectioncount"></a>DownloadCollection 計數

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**Count** 屬性會抓取集合中的暫止下載數目。

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).count
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DownloadCollection 物件**](downloadcollection-object.md)
</dt> </dl>

 

 





