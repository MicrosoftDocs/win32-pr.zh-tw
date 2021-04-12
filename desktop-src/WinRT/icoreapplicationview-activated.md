---
description: 在啟用 Windows Store 應用程式時發生。
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'ICoreApplicationView：：啟動的事件 (ApplicationModel) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612f7110aa149396b18815afe664ee404c70fc52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191350"
---
# <a name="icoreapplicationviewactivated-event"></a>ICoreApplicationView：：已啟用事件

在啟用 Windows Store 應用程式時發生。

## <a name="syntax"></a>語法


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*處理常式* \[在\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

請勿從 *處理常式* 內呼叫 [**Exit**](/previous-versions//hh438368(v=vs.85))方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                         |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                               |
| 標頭<br/>                   | <dl> <dt>ApplicationModel Core。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ApplicationModel。</dt> </dl> |



 

 
