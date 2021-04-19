---
title: IWMPCdromBurn isAvailable 方法
description: IsAvailable 方法提供 CD 光碟機和媒體的相關資訊。
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- isAvailable 方法 Windows Media Player
- isAvailable 方法 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，isAvailable 方法
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992978"
---
# <a name="iwmpcdromburnisavailable-method"></a>IWMPCdromBurn：： isAvailable 方法

**IsAvailable** 方法提供 CD 光碟機和媒體的相關資訊。

## <a name="syntax"></a>語法


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrItem* \[在\]
</dt> <dd>

**System.string** ，包含下列其中一個值。



| 值 | 描述                 |
|-------|-----------------------------|
| 燒錄  | 磁片磁碟機是 CD 燒錄機。   |
| 光碟  | 磁片磁碟機中有 CD。 |
| 清除 | 您可以清除 CD。       |
| 寫入 | 您可以將 CD 寫入至。   |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

表示結果的 **system.object** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPCdromBurn 介面 (VB 和 c # )**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





