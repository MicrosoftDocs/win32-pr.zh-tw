---
description: 捕獲事件系統的版本號碼。
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: IEventSystem2：： GetVersion 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 77452ccebac71cb8de8357fee0199bc04b690d59cf8d113d57a5850db0771315
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070618"
---
# <a name="ieventsystem2getversion-method"></a>IEventSystem2：： GetVersion 方法

捕獲事件系統的版本號碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pnVersion* \[擴展\]
</dt> <dd>

事件系統的版本號碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期、e \_ 失敗和 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEventSystem2**](ieventsystem2.md)
</dt> </dl>

 

 




