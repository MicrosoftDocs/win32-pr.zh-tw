---
title: 'IEnumBackgroundCopyFiles Skip 方法 (>deliveryoptimization. h) '
description: 略過列舉順序中的下一個指定元素數目。 如果序列中剩餘的元素少於所要求的專案數，則會略過序列中的最後一個元素。
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Skip 方法
- Skip 方法，IEnumBackgroundCopyFiles 介面
- IEnumBackgroundCopyFiles 介面，Skip 方法
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Skip
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d88a7d971ab93b90c844fc8d9d92d7f154c0ebf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024740"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a>IEnumBackgroundCopyFiles：： Skip 方法

略過列舉順序中的下一個指定元素數目。 如果序列中剩餘的元素少於所要求的專案數，則會略過序列中的最後一個元素。

## <a name="syntax"></a>語法


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*celt* \[在\]
</dt> <dd>

要略過的元素數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                              | Description                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | 已成功跳過要求的元素數目。<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | 略過小於要求的元素數目。<br/>    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles 定義為 CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





