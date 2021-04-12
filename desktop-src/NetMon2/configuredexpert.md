---
description: CONFIGUREDEXPERT 結構會讓專家與其設定資料產生關聯。
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: 'CONFIGUREDEXPERT 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192963"
---
# <a name="configuredexpert-structure"></a>CONFIGUREDEXPERT 結構

**CONFIGUREDEXPERT** 結構會讓專家與其設定資料產生關聯。

## <a name="syntax"></a>語法


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a>成員

<dl> <dt>

**hExpert**
</dt> <dd>

專家的控點。

</dd> <dt>

**StartupFlags**
</dt> <dd>

專家的啟動旗標值。

</dd> <dt>

**pConfig**
</dt> <dd>

[**EXPERTCONFIG**](expertconfig.md)結構的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




