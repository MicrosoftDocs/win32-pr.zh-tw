---
title: IWMPStringCollection count 屬性
description: Count 屬性會取得字串集合中的專案數。
ms.assetid: 0ba2d158-fa54-46a8-9124-8a412e71bd09
keywords:
- count 屬性 Windows Media Player
- count 屬性 Windows Media Player，IWMPStringCollection 介面
- IWMPStringCollection 介面 Windows Media Player，count 屬性
topic_type:
- apiref
api_name:
- IWMPStringCollection.count
- IWMPStringCollection.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e4147d1fbae6c98458c460df34d365d84fe0b2a9f23d508bff4eccb75935de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568451"
---
# <a name="iwmpstringcollectioncount-property"></a>IWMPStringCollection：： count 屬性

**Count** 屬性會取得字串集合中的專案數。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>屬性值

System.string **，是** 字串集合中的專案數。

## <a name="remarks"></a>備註

使用這個屬性之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPSettings2. mediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection 介面 (VB 和 c # )**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





