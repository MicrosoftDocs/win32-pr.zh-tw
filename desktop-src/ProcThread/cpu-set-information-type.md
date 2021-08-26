---
description: 表示系統 \_ CPU \_ 集資訊結構中的資訊類型 \_ 。
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: 'CPU_SET_INFORMATION_TYPE 列舉 (Processthreadapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPU_SET_INFORMATION_TYPE
api_type:
- HeaderDef
api_location:
- Processthreadapi.h
ms.openlocfilehash: 7c932a143553c1101d6a81bac86ba54e21603eaf80ed5d2613484bff22a7e625
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101928"
---
# <a name="cpu_set_information_type-enumeration"></a>CPU \_ 集 \_ 資訊 \_ 類型列舉

表示 [**系統 \_ CPU \_ 集 \_ 資訊**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) 結構中的資訊類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**
</dt> <dd>

此結構包含 CPU 集資訊。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                                       |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Processthreadsapi (包含 Windows .h) </dt> </dl> |



 

 




