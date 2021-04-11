---
description: 取得非同步動作的結果。
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: IAsyncAction：： GetResults 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 292c73846227f1bb8884b24b7e709bc6b2296e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191351"
---
# <a name="iasyncactiongetresults-method"></a>IAsyncAction：： GetResults 方法

取得非同步動作的結果。

## <a name="syntax"></a>語法


```C++
HRESULT GetResults();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **HRESULT**

這個方法一律會傳回 **S \_ OK**。

## <a name="remarks"></a>備註

如果目前的實有動態類型的 [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)，則呼叫 **GetResults** 方法不會有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                    |
| 標頭<br/>                   | <dl> <dt>Windows .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
