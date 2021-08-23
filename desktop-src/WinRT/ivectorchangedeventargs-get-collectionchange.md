---
description: 取得在向量中發生的變更類型。
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'IVectorChangedEventArgs：： get_CollectionChange 方法 (IVectorChangedEventArgs .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 2476f9563b4e2a0cabf9babbcfc265ee4f3549416c2fdfda0dbb0f204b7ca9bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504808"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a>IVectorChangedEventArgs：： get \_ CollectionChange 方法

取得在向量中發生的變更類型。

## <a name="syntax"></a>語法


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[退出，retval\]
</dt> <dd>

類型： **CollectionChange \***

[**CollectionChange**](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041)列舉中的值，可描述變更。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                       |
| 標頭<br/>                   | <dl> <dt>IVectorChangedEventArgs。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVectorChangedEventArgs**](ivectorchangedeventargs.md)
</dt> </dl>

 

 
