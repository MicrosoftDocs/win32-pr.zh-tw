---
description: 建立組名及其控制碼的關聯。
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: 'GROUPINFO 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5152b0a621a34e49d6f1024a81b7e91aed94a06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986299"
---
# <a name="groupinfo-structure"></a>GROUPINFO 結構

**GROUPINFO** 結構會將組名及其控制碼相關聯。

## <a name="syntax"></a>語法


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**szGroupName**
</dt> <dd>

**在擁有組結構中** 的陣列遞增值。

</dd> <dt>

**hGroup**
</dt> <dd>

群組的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




