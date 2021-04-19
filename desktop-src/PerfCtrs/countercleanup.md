---
description: 移除提供者註冊。
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: CounterCleanup 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969362"
---
# <a name="countercleanup-function"></a>CounterCleanup 函式

移除提供者的註冊。

## <a name="syntax"></a>語法


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

您的提供者會呼叫這個函數。 此函數會呼叫 [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) 函式，以移除提供者的註冊。

當您指定 **-o** 引數時， [**CTRPP**](ctrpp.md)工具會產生這個內嵌函數。 如果您指定 **-prefix** 引數 (例如 **_prefix_CounterCleanup**，則函式的名稱會包含 *前置* 詞字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 




