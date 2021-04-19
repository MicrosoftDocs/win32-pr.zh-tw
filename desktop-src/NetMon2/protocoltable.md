---
description: PROTOCOLTABLE 結構包含通訊協定清單。
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: 'PROTOCOLTABLE 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3ad79beca7ce79611747a02704ffc05da5fc3d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983796"
---
# <a name="protocoltable-structure"></a>PROTOCOLTABLE 結構

**PROTOCOLTABLE** 結構包含通訊協定清單。

## <a name="syntax"></a>語法


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a>成員

<dl> <dt>

**nProtocols**
</dt> <dd>

已啟用的通訊協定數目。

</dd> <dt>

**hProtocol**
</dt> <dd>

啟用的通訊協定之控制碼的陣列。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




