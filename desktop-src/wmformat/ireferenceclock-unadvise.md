---
title: IReferenceClock Unadvise 方法
description: Unadvise 方法會取消通知要求。
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Unadvise 方法 windows Media 格式
- Unadvise 方法 windows Media Format，IReferenceClock 介面
- IReferenceClock 介面 windows Media Format，Unadvise 方法
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104092416"
---
# <a name="ireferenceclockunadvise-method"></a>IReferenceClock：： Unadvise 方法

**Unadvise** 方法會取消通知要求。

## <a name="syntax"></a>語法


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwAdviseCookie* 
</dt> <dd>

要移除之要求的識別碼。 使用 AdviseTime 在 pdwAdviseCookie 參數中所傳回的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                             | Description                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 此方法已成功。<br/>                    |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 傳入的識別碼不存在。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IReferenceClock 介面**](ireferenceclock.md)
</dt> </dl>

 

 





