---
title: IWMPSettings2 mediaAccessRights 屬性
description: MediaAccessRights 屬性會取得值，指出目前授與存取程式庫的許可權。
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- mediaAccessRights 屬性 Windows Media Player
- mediaAccessRights 屬性 Windows Media Player，IWMPSettings2 介面
- IWMPSettings2 介面 Windows Media Player，mediaAccessRights 屬性
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 797e45c62b505033afd2126f79d5830de5bc9847a4de36199a6c919a4978f112
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122488"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a>IWMPSettings2：： mediaAccessRights 屬性

**MediaAccessRights** 屬性會取得值，指出目前授與存取程式庫的許可權。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a>屬性值

**System.string** ，這是下列其中一個值。



| 值 | 描述                      |
|-------|----------------------------------|
| 無  | 僅限目前的專案存取權限。 |
| 讀取  | 僅限讀取存取許可權。         |
| 完整  | 讀取/寫入存取權限。        |



 

## <a name="remarks"></a>備註

網頁必須先向使用者要求許可權，以讀取或寫入文件庫中的資料。 這表示，如果未授與適當的存取權限，就無法從程式碼存取某些方法、屬性和事件。 為了取得存取權限，應用程式會呼叫 **IWMPSettings2， \_** 並傳遞指定所需存取權限層級的參數。

在使用者電腦上執行的應用程式一律具有完整存取權限。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPSettings2 介面 (VB 和 c # )**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





