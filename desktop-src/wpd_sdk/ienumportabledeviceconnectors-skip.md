---
description: 略過列舉序列中指定的裝置數目。
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: 'IEnumPortableDeviceConnectors：： Skip 方法 (Devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Skip
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: ba704a2dd232ce5c8ba08d0271e5e0a8fda72f86f9aef89d2e89b04ca9fe94b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546548"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a>IEnumPortableDeviceConnectors：： Skip 方法

**Skip** 方法會在列舉順序中略過指定數目的裝置。

## <a name="syntax"></a>語法


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cConnectors* \[在\]
</dt> <dd>

要略過的裝置數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                             | 描述                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 此方法已成功。<br/>                                                                                                                                                          |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 無法略過指定的裝置數目。 其中一個可能的原因： *cConnectors* 參數指定的裝置數目超過實際保留在列舉順序中的數目。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                                                                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                                   |
| 標頭<br/>                   | <dl> <dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Portabledeviceconnectapi .idl</dt> </dl>                                                                |
| 程式庫<br/>                  | <dl> <dt>PortableDeviceGuids .lib</dt> </dl>                                                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




