---
description: IPortableDevicePropVariantCollection 介面會保存相同 VARTYPE 之索引 PROPVARIANT 值的集合。
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: 'IPortableDevicePropVariantCollection 介面 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 14ba07894c74567487704bb1f63e7242542af313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000752"
---
# <a name="iportabledevicepropvariantcollection-interface"></a>IPortableDevicePropVariantCollection 介面

**IPortableDevicePropVariantCollection** 介面會保存相同 VARTYPE 之索引 **PROPVARIANT** 值的集合。 加入至集合的第一個專案的 VARTYPE 會決定集合的 VARTYPE。 如果 **PROPVARIANT** 值無法變更為集合的目前 VARTYPE，嘗試加入不同 VARTYPE 的專案可能會失敗。 若要變更集合的 VARTYPE，請呼叫 **ChangeType**。

您可以從方法中取出這個介面，或者，如果需要新的物件，請使用 **CLSID \_ PortableDevicePropVariantCollection** 呼叫 **CoCreate** 。

## <a name="members"></a>成員

**IPortableDevicePropVariantCollection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IPortableDevicePropVariantCollection** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IPortableDevicePropVariantCollection** 介面具有這些方法。



| 方法                                                                | 描述                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**添加**](iportabledevicepropvariantcollection-add.md)               | 將項目新增至集合。<br/>                                          |
| [**ChangeType**](iportabledevicepropvariantcollection-changetype.md) | 將集合中的所有專案轉換為指定的 VARTYPE。<br/>           |
| [**清楚**](iportabledevicepropvariantcollection-clear.md)           | 釋放和移除集合中的所有專案。<br/>                  |
| [**GetAt**](iportabledevicepropvariantcollection-getat.md)           | 以零為基底的索引，從集合中抓取專案。<br/>             |
| [**GetCount**](iportabledevicepropvariantcollection-getcount.md)     | 捕獲此集合中的專案數。<br/>                        |
| [**GetType**](iportabledevicepropvariantcollection-gettype.md)       | 抓取集合中專案的資料類型。<br/>                  |
| [**RemoveAt**](iportabledevicepropvariantcollection-removeat.md)     | 移除儲存在指定索引所指定之位置的元素。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**集合介面**](collection-interfaces.md)
</dt> </dl>

 

