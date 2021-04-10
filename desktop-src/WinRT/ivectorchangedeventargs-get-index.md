---
description: 取得向量中發生變更的位置。
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: 'IVectorChangedEventArgs：： get_Index 方法 (IVectorChangedEventArgs .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 5c131567ec7fc2861ce11db9e5d7ec581f6f663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026224"
---
# <a name="ivectorchangedeventargsget_index-method"></a>IVectorChangedEventArgs：： get \_ Index 方法

取得向量中發生變更的位置。

## <a name="syntax"></a>語法


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[退出，retval\]
</dt> <dd>

類型： **未 \* 簽署* _

向量中發生變更之以零為起始的位置（如果適用）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

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

 

 




