---
title: IWMPSettings2 requestMediaAccessRights 方法
description: RequestMediaAccessRights 方法會要求存取程式庫的指定層級。 |IWMPSettings2 requestMediaAccessRights 方法
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- requestMediaAccessRights 方法 Windows Media Player
- requestMediaAccessRights 方法 Windows Media Player，IWMPSettings2 介面
- IWMPSettings2 介面 Windows Media Player，requestMediaAccessRights 方法
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c609afffc1d9b228d908d905e0eb1a6ef8741032
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000808"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a>IWMPSettings2：： requestMediaAccessRights 方法

**RequestMediaAccessRights** 方法會要求存取程式庫的指定層級。

## <a name="syntax"></a>語法


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrDesiredAccess* \[在\]
</dt> <dd>

**System.string** ，這是下列其中一個值。



| 值 | 描述                      |
|-------|----------------------------------|
| 無  | 僅限目前的專案存取權限。 |
| 讀取  | 僅限讀取存取許可權。         |
| 完整  | 讀取/寫入存取權限。        |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

指出是否已授與所要求之存取權限的 **system.object** 。

## <a name="remarks"></a>備註

網頁必須先向使用者要求許可權，以讀取或寫入文件庫中的資料。 叫用這個方法會提示使用者一個對話方塊，要求指定的許可權等級。 這表示，如果未授與適當的存取權限，就無法從程式碼存取某些方法、屬性和事件。 您可以使用 **IWMPSettings2 mediaAccessRights** 來抓取目前的存取權限層級。

在使用者電腦上執行的應用程式不需要使用這個方法。

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

[**IWMPSettings2. mediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





