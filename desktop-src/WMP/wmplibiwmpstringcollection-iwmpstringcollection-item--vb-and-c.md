---
title: IWMPStringCollection Item 方法
description: Item 方法會傳回指定索引處的字串。
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Item 方法 Windows Media Player
- Item 方法 Windows Media Player，IWMPStringCollection 介面
- IWMPStringCollection 介面 Windows Media Player，Item 方法
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47928502dce9ed4deb12461763a499de5d962aa1303b4c9cc5eacb02c7619da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568424"
---
# <a name="iwmpstringcollectionitem-method"></a>IWMPStringCollection：： Item 方法

**Item** 方法會傳回指定索引處的字串。

## <a name="syntax"></a>語法


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a>參數

<dl> <dt>

*lIndex* \[在\]
</dt> <dd>

作為索引的 **system.object** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

System.string **，它** 是位於指定索引位置的字串。

## <a name="remarks"></a>備註

**IWMPStringCollection** 介面是用來取得屬性可用的值集。 例如，您可以使用 **IWMPMediaCollection. getAttributeStringCollection** 方法來取得 **IWMPStringCollection** 介面，代表音訊媒體類型內內容類型屬性的所有值。 然後，可以使用 Item 方法來逐一查看 [ **內容** 類型] 屬性的所有可能值。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPMediaCollection. getAttributeStringCollection (VB 和 c # )**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection 介面 (VB 和 c # )**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





