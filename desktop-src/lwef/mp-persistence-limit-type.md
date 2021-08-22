---
title: 'MP_PERSISTENCE_LIMIT_TYPE 列舉 (MpClient .h) '
description: 持續性限制類型。
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- MP_PERSISTENCE_LIMIT_TYPE 列舉舊版 Windows 環境功能
- PMP_PERSISTENCE_LIMIT_TYPE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MP_PERSISTENCE_LIMIT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a56d4962467abe0ad338af257aca2581e612c100468fbdf2853aa4d71290ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608998"
---
# <a name="mp_persistence_limit_type-enumeration"></a>MP \_ 持續性 \_ 限制 \_ 類型列舉

持續性限制類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMP_PERSISTENCE_LIMIT_TYPE { 
  MP_PERSISTENCE_UNKNOWN      = 0,
  MP_PERSISTENCE_NO_LIMIT     = 1,
  MP_PERSISTENCE_DURATION     = 2,
  MP_PERSISTENCE_VDM_VERSION  = 3,
  MP_PERSISTENCE_TIMESTAMP    = 4,
  MP_PERSISTENCE_FORCED       = 5
} MP_PERSISTENCE_LIMIT_TYPE, *PMP_PERSISTENCE_LIMIT_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**MP \_ 持續性 \_ 不明**
</dt> <dd>

未知。

</dd> <dt>

<span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**MP \_ 持續性 \_ 無 \_ 限制**
</dt> <dd>

沒有限制。

</dd> <dt>

<span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**MP \_ 持續 \_ 時間**
</dt> <dd>

持續期間。

</dd> <dt>

<span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**MP \_ 持續性的 \_ VDM \_ 版本**
</dt> <dd>

VDM 版本。

</dd> <dt>

<span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**MP \_ 持續 \_ 時間戳記**
</dt> <dd>

Timestamp：

</dd> <dt>

<span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**強制執行 MP \_ 持續性 \_**
</dt> <dd>

強迫。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





