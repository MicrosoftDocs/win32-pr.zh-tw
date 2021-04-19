---
description: 取得物件之 agile 參考的介面識別碼。
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: IAgileReference：： Resolve 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001669"
---
# <a name="iagilereferenceresolve-method"></a>IAgileReference：： Resolve 方法

取得物件之 agile 參考的介面識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*riid* \[在\]
</dt> <dd>

要從 agile 參考中取出的介面介面識別碼。 它不一定要與註冊的介面相同。

</dd> <dt>

*ppvObjectReference* \[退出，retval\]
</dt> <dd>

成功完成時， \* *ppvObjectReference* 是由 *riid* 所指定之介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回值                                                                              | 描述                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ 確定</dt> </dl>          | 已成功完成命令。<br/>                                  |
| <dl> <dt>E \_ NOINTERFACE</dt> </dl> | 要求的介面不會在已註冊的物件上執行。<br/> |



 

## <a name="remarks"></a>備註

呼叫 [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) 函數，以建立物件的 agile 參考。 呼叫 **resolve** 方法，將物件當地語系化至呼叫 **解析** 的單元中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>            |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




