---
title: IWMPControls2 步驟方法
description: Step 方法會讓目前的影片媒體專案進入下一個畫面格，或上一個畫面格，並凍結播放。
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- 步驟方法 Windows Media Player
- 步驟方法 Windows Media Player，IWMPControls2 介面
- IWMPControls2 介面 Windows Media Player，step 方法
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfb65dd20de506a8f303121b23668e2fbf14dc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995474"
---
# <a name="iwmpcontrols2step-method"></a>IWMPControls2：： step 方法

**Step** 方法會讓目前的影片媒體專案進入下一個畫面格，或上一個畫面格，並凍結播放。

## <a name="syntax"></a>語法


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a>參數

<dl> <dt>

*lStep* \[在\]
</dt> <dd>

System.string **值，** 表示凍結前要執行的畫面格數目。 必須設定為1或-1。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法目前僅支援參數1或-1，因此您一次只能執行一個畫面格。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPControls2 介面 (VB 和 c # )**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**IWMPDVD 介面 (VB 和 c # )**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





