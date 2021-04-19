---
title: IWMPLibraryServices getCountByType 方法
description: GetCountByType 方法會傳回指定類型的可用程式庫計數。
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- getCountByType 方法 Windows Media Player
- getCountByType 方法 Windows Media Player，IWMPLibraryServices 介面
- IWMPLibraryServices 介面 Windows Media Player，getCountByType 方法
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978482"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a>IWMPLibraryServices：： getCountByType 方法

**GetCountByType** 方法會傳回指定類型的可用程式庫計數。

## <a name="syntax"></a>語法


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a>參數

<dl> <dt>

*wmplt* \[在\]
</dt> <dd>

**WMPLib. WMPLibraryType** 列舉中的值，這個值會指定要計算的程式庫類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

為程式庫計數的 **system.object** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPLibraryServices 介面 (VB 和 c # )**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





