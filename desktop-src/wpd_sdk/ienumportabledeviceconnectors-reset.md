---
description: IEnumPortableDeviceConnectors：： Reset 方法-將列舉順序重設為開頭。
ms.assetid: 1df1ff95-06ae-4e5e-8064-17f832c5f0b3
title: 'IEnumPortableDeviceConnectors：： Reset 方法 (Devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Reset
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 10a356fbb8591568a9f99d9b92d681a46754a960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083204"
---
# <a name="ienumportabledeviceconnectorsreset-method"></a>IEnumPortableDeviceConnectors：： Reset 方法

**Reset** 方法會將列舉順序重設為開頭。

## <a name="syntax"></a>語法


```C++
HRESULT Reset();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                                                                             |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                                                              |
| 標頭<br/>                   | <dl> <dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi .idl</dt> </dl>                                                                |
| 程式庫<br/>                  | <dl> <dt>PortableDeviceGuids .lib</dt> </dl>                                                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




