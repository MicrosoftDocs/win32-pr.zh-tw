---
description: IPortableDeviceKeyCollection 介面會保存 PROPERTYKEY 值的集合。 您可以從方法中取出這個介面，或者，如果需要新的物件，請使用 CLSID PortableDeviceKeyCollection 呼叫 CoCreate \_ 。
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: 'IPortableDeviceKeyCollection 介面 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0f648020ddb82db2a619f75bb125e94c7679f8dd3061ac282fcc0f911a498a77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839388"
---
# <a name="iportabledevicekeycollection-interface"></a>IPortableDeviceKeyCollection 介面

**IPortableDeviceKeyCollection** 介面會保存 **PROPERTYKEY** 值的集合。 您可以從方法中取出這個介面，或者，如果需要新的物件，請使用 **CLSID \_ PortableDeviceKeyCollection** 呼叫 **CoCreate** 。

## <a name="members"></a>成員

**IPortableDeviceKeyCollection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IPortableDeviceKeyCollection** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IPortableDeviceKeyCollection** 介面具有這些方法。



| 方法                                                    | 描述                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**添加**](iportabledevicekeycollection-add.md)           | 將屬性索引鍵加入至集合。<br/>                                   |
| [**清除**](iportabledevicekeycollection-clear.md)       | 刪除集合中的所有專案。<br/>                                   |
| [**GetAt**](iportabledevicekeycollection-getat.md)       | 依據索引，從集合抓取 **PROPERTYKEY** 。<br/>                |
| [**GetCount**](iportabledevicekeycollection-getcount.md) | 捕獲此集合中的索引鍵數目。<br/>                         |
| [**RemoveAt**](iportabledevicekeycollection-removeat.md) | 移除儲存在指定索引所指定之位置的元素。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**集合介面**](collection-interfaces.md)
</dt> </dl>

 

