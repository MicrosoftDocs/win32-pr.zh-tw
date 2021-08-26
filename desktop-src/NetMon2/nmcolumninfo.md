---
description: NMCOLUMNINFO 結構會在事件檢視器的上方窗格中定義一個資料行。
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: 'NMCOLUMNINFO 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95683eb812a2b8a668664f7ad8092a91c1940d2c3f7185225e8364959777538b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037118"
---
# <a name="nmcolumninfo-structure"></a>NMCOLUMNINFO 結構

**NMCOLUMNINFO** 結構會在事件檢視器的上方窗格中定義一個資料行。

## <a name="syntax"></a>語法


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**szColumnName**
</dt> <dd>

特定資料行的可顯示名稱。 如果名稱太長，就不會在預設的事件檢視器設定中完全顯示。

</dd> <dt>

**VariantData**
</dt> <dd>

插入資料行中的資料。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




