---
description: IPortableDeviceValuesCollection：： GetAt 方法-GetAt 方法會依據以零為基底的索引，從集合中抓取專案。
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: 'IPortableDeviceValuesCollection：： GetAt 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 089c6c5c523b6f05f91efb5524904c942a539a7ebbb3cd863c1c07d413cdf1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704628"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a>IPortableDeviceValuesCollection：： GetAt 方法

**GetAt** 方法會依據以零為基底的索引，從集合中抓取專案。

## <a name="syntax"></a>語法


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwIndex* \[在\]
</dt> <dd>

**DWORD** ，指定集合中以零為基底的索引。

</dd> <dt>

*ppValues* \[擴展\]
</dt> <dd>

從集合接收 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面指標的變數位址。 當呼叫端完成時，呼叫端會負責呼叫此介面上的 **釋放** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                  | 描述                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法已成功。<br/>                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 傳入的以零為基底的索引超出範圍。<br/>             |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | 必要的指標引數為 **Null**。<br/>                             |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 集合包含 **Null** **IPortableDeviceValues** 指標。<br/> |



 

## <a name="remarks"></a>備註

對已抓取介面中的值所做的任何變更，都會對儲存在集合中的版本進行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValuesCollection 介面**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




