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
ms.openlocfilehash: 0283275856e8e68bf983aaeb9a7660a5a0a6bf59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975091"
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
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Processthreadsapi (包含) 的 Windows。h </dt> </dl> |



 

 




