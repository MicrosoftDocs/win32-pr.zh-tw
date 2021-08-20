---
title: IWMPCdromBurn getItemInfo 方法
description: GetItemInfo 方法會抓取 CD 的指定屬性值。
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2cf1a91ad60826e19051a59617157110fbcd8d75eff325f94f9b3f84d759aa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116226"
---
# <a name="iwmpcdromburngetiteminfo-method"></a>IWMPCdromBurn：： getItemInfo 方法

**GetItemInfo** 方法會抓取 CD 的指定屬性值。

## <a name="syntax"></a>語法


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrItem* \[在\]
</dt> <dd>

**System.string** ，包含下列其中一個值。



| 值         | 描述                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| AvailableTime | 抓取 CD 上的可用時間（以秒為單位）。                                          |
| Blank         | 抓取 system.string **(表示** 為字串，) 指出 CD 是否為空白。 |
| FreeSpace     | 抓取 CD 上的可用空間（以位元組為單位）。                                                |
| TotalSpace    | 抓取 CD 上的總空間（以位元組為單位）。                                               |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

**System.string** ，這是指定之屬性的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11<br/>                                                                                     |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPCdromBurn 介面 (VB 和 c # )**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





