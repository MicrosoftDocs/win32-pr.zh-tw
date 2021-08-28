---
description: 指定應用程式的健全狀況狀態。
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: APPLICATION_STATE 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPLICATION_STATE
api_type:
- IDLDef
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 5f873e7a30a4cff6dc4cc89eaea225201a367f7c24ead11ad95da04c2ff1ab32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914158"
---
# <a name="application_state-enumeration"></a>應用程式 \_ 狀態列舉

指定應用程式的健全狀況狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**
</dt> <dd>

應用程式狀態為狀況良好。

</dd> <dt>

<span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**
</dt> <dd>

應用程式狀態為 [重大]。

</dd> </dl>

## <a name="remarks"></a>備註

若要使用這個程式設計項目，Windows 8 的整合元件必須安裝在執行應用程式的虛擬機器上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                      |
| 版本<br/>                  | Windows 8 的整合元件<br/>                                                           |
| IDL<br/>                      | <dl> <dt>VmApplicationHealthMonitor .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




