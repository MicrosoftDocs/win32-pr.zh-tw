---
description: IPortableDeviceValuesCollection 介面會保存以零為基底的索引 IPortableDeviceValues 介面集合。
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: 'IPortableDeviceValuesCollection 介面 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cd6547a96013b2b83ce9962a62f0837dd01cacac6f3e64adc3b964754c148c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928378"
---
# <a name="iportabledevicevaluescollection-interface"></a>IPortableDeviceValuesCollection 介面

**IPortableDeviceValuesCollection** 介面會保存以零為基底的索引 **IPortableDeviceValues** 介面集合。 您可以從方法中取出這個介面，或者，如果需要新的物件，請使用 **CLSID \_ PortableDeviceValuesCollection** 呼叫 **CoCreate** 。

## <a name="members"></a>成員

**IPortableDeviceValuesCollection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IPortableDeviceValuesCollection** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IPortableDeviceValuesCollection** 介面具有這些方法。



| 方法                                                       | 描述                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**添加**](iportabledevicevaluescollection-add.md)           | 將項目加入集合<br/>                                           |
| [**清除**](iportabledevicevaluescollection-clear.md)       | 釋放集合中的所有專案。<br/>                                  |
| [**GetAt**](iportabledevicevaluescollection-getat.md)       | 以零為基底的索引，從集合中抓取專案。<br/>             |
| [**GetCount**](iportabledevicevaluescollection-getcount.md) | 抓取集合中的專案數。<br/>                         |
| [**RemoveAt**](iportabledevicevaluescollection-removeat.md) | 移除儲存在指定索引所指定之位置的元素。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**集合介面**](collection-interfaces.md)
</dt> </dl>

 

