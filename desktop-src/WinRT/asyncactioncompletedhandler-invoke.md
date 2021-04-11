---
description: 叫用指定的非同步動作完成時所呼叫的方法。
ms.assetid: 97199C1A-7CE3-4BBD-86A3-2CA9B27CC05E
title: AsyncActionCompletedHandler：： Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler.Invoke
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 1cba9c48fa955b82fdc337ba641acbd4c62f6406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113132"
---
# <a name="asyncactioncompletedhandlerinvoke-method"></a>AsyncActionCompletedHandler：： Invoke 方法

叫用指定的非同步動作完成時所呼叫的方法。

## <a name="syntax"></a>語法


```C++
HRESULT Invoke(
  [in] IAsyncAction *asyncInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*system.runtime.interopservices.windowsruntime.asyncinfo* \[在\]
</dt> <dd>

類型： **[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) \** _

報告完成的非同步動作。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                    |
| 標頭<br/>                   | <dl> <dt>Windows .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)
</dt> </dl>

 

