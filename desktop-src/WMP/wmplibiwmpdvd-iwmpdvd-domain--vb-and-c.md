---
title: IWMPDVD 網域屬性
description: 網域屬性會取得 DVD 的目前網域。
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- 網域屬性 Windows Media Player
- 網域屬性 Windows Media Player、IWMPDVD 介面
- IWMPDVD 介面 Windows Media Player，網域屬性
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996051"
---
# <a name="iwmpdvddomain-property"></a>IWMPDVD：:d omain 屬性

**網域** 屬性會取得 DVD 的目前網域。

## <a name="syntax"></a>Syntax


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a>屬性值

**System.string** ，這是下列其中一個值。



| 值                                                                                        | 意義                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>firstPlay</dt> </dl>         | 執行 DVD 光碟的預設初始化。<br/>                                                                                      |
| <dl> <dt>videoManagerMenu</dt> </dl>  | 顯示整個光碟的功能表。也稱為 Windows Media Player 的 topMenu。 通常稱為標題功能表或頂端功能表。<br/> |
| <dl> <dt>videoTitleSetMenu</dt> </dl> | 顯示目前標題集的功能表。 也稱為 Windows Media Player 的 titleMenu。 通常稱為根功能表。<br/>          |
| <dl> <dt>title</dt> </dl>             | 通常會顯示目前的標題。<br/>                                                                                                |
| <dl> <dt>停止</dt> </dl>              | DVD 導覽器位於 DVD 停止網域中。<br/>                                                                                          |
| <dl> <dt>定義</dt> </dl>         | Windows Media Player 不在任何 DVD 網域中。<br/>                                                                                        |



 

## <a name="remarks"></a>備註

每個 DVD 的撰寫方式不同。 某些 Dvd 不包含 firstPlay、videoManagerMenu 或 videoTitleSetMenu 網域。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPDVD 介面 (VB 和 c # )**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





