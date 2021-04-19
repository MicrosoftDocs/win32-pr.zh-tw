---
title: IWMPLibraryServices getLibraryByType 方法
description: GetLibraryByType 方法會傳回 IWMPLibrary 介面，代表具有指定之類型和索引的程式庫。
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- getLibraryByType 方法 Windows Media Player
- getLibraryByType 方法 Windows Media Player，IWMPLibraryServices 介面
- IWMPLibraryServices 介面 Windows Media Player，getLibraryByType 方法
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994861"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a>IWMPLibraryServices：： getLibraryByType 方法

**GetLibraryByType** 方法會傳回 **IWMPLibrary** 介面，代表具有指定之類型和索引的程式庫。

## <a name="syntax"></a>語法


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a>參數

<dl> <dt>

*wmplt* \[在\]
</dt> <dd>

**WMPLib. WMPLibraryType** 列舉中的值，這個值會指定要取出的程式庫類型。

</dd> <dt>

*lIndex* \[在\]
</dt> <dd>

要抓取之程式庫索引的 **system.object。**

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回之程式庫的 **WMPLib IWMPLibrary** 介面。

## <a name="remarks"></a>備註

只有一個本機程式庫，而只有包含媒體內容的資料 Cd 和 Dvd 上才能使用光碟櫃。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPLibrary 介面 (VB 和 c # )**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**IWMPLibraryServices 介面 (VB 和 c # )**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





