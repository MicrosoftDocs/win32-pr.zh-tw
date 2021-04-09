---
title: '連接結構 (NapEnforcementClient .h) '
description: 包含 enforcer 所維護之連接清單的相關資訊。
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- 連接結構 NAP
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e79add74830dfa8ca77fa24a5d3233542a7e553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935141"
---
# <a name="connections-structure"></a>連接結構

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**連接** 結構包含 enforcer 所維護之連接清單的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a>成員

<dl> <dt>

**計數**
</dt> <dd>

目前由 enforcer 所維護的作用中連接數目，範圍 0 (零) 至 [**maxConnectionCountPerEnforcer**](nap-type-constants.md)。

</dd> <dt>

**連接**
</dt> <dd>

代表用戶端連接之 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) 介面清單的 COM 指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapEnforcementClient。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NAP 參考](nap-reference.md)
</dt> <dt>

[NAP 結構](nap-structures.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





