---
description: 這個類別是堆疊追蹤事件的父類別。
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: StackWalk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ad873815cb5cea40c1a9d2f694eca8d0e90d11b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972184"
---
# <a name="stackwalk-class"></a>StackWalk 類別

這個類別是堆疊追蹤事件的父類別。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**StackWalk** 類別不會定義任何成員。

## <a name="remarks"></a>備註

若要啟用核心事件的堆疊追蹤，請呼叫 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 函式，並指定您想要用來捕捉堆疊追蹤的核心事件和類型。 若要啟用其他事件的堆疊追蹤，請將 [[**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)的 **EnableProperty** 成員] 設定為 [**事件 \_ 啟用 \_ 屬性 \_ 堆疊 \_ 追蹤**]。

使用下列事件種類來識別使用事件時的實際事件。



| 事件類型           | 描述                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| 事件種類值，32 | 堆疊追蹤事件。 [**StackWalk \_ 事件**](stackwalk-event.md)MOF 類別會定義此事件的事件資料。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 
