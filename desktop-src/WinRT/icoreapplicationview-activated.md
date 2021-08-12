---
description: 在啟用 Windows 存放區應用程式時發生。
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'ICoreApplicationView：：已啟用事件 (Windows。ApplicationModel) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e736d0fb5403fe76d6d402c261e6b7e5336dfc096d8c39d7b3300b93ab1332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560992"
---
# <a name="icoreapplicationviewactivated-event"></a>ICoreApplicationView：：已啟用事件

在啟用 Windows 存放區應用程式時發生。

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
| 標頭<br/>                   | <dl> <dt>Windows。ApplicationModel Core。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Windows。ApplicationModel</dt> </dl> |



 

 
