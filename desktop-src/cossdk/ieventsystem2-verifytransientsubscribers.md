---
description: 確認資料存放區中的所有暫時性訂閱者是否存在。 藉由呼叫這個方法，您可以確保資料存放區中列出的所有暫時性訂閱者都在作用中。
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: IEventSystem2：： VerifyTransientSubscribers 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936228"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a>IEventSystem2：： VerifyTransientSubscribers 方法

確認資料存放區中的所有暫時性訂閱者是否存在。 藉由呼叫這個方法，您可以確保資料存放區中列出的所有暫時性訂閱者都在作用中。

## <a name="syntax"></a>語法


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

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

 

 




