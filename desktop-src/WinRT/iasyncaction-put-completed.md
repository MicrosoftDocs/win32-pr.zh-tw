---
description: 設定非同步動作完成時所呼叫的方法。
ms.assetid: 632800E4-D02B-4D45-8A9B-B373AC938558
title: IAsyncAction：:p ut_Completed 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.put_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: aff219d5e6847c64034eed1b057e300ea601eedaa8aa7a131f1467aeacc42422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323161"
---
# <a name="iasyncactionput_completed-method"></a>IAsyncAction：:p 的 ui \_ 已完成方法

設定非同步動作完成時所呼叫的方法。

## <a name="syntax"></a>語法


```C++
HRESULT put_Completed(
  [out] AsyncActionCompletedHandler *handler
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*處理常式* \[擴展\]
</dt> <dd>

類型： **[ **AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\***

處理完成通知的方法。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                    |
| 標頭<br/>                   | <dl> <dt>Windows。Foundation .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
