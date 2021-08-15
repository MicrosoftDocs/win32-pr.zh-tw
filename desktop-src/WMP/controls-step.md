---
title: Controls 方法
description: Step 方法會導致目前的影片媒體專案凍結下一個畫面或上一個畫面格的播放。
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- 步驟方法 Windows Media Player
- 步驟方法 Windows Media Player、控制項類別
- Controls 類別 Windows Media Player、step 方法
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4626ff80aee55ad6c22be7580a07ef2319afb6792a8c11b815d72af23b5727fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118839823"
---
# <a name="controlsstep-method"></a>Controls 方法

**Step** 方法會導致目前的影片媒體專案凍結下一個畫面或上一個畫面格的播放。

## <a name="syntax"></a>語法


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*frameCount* \[在\]
</dt> <dd>

**Number** (**long**) 指出凍結前要執行的畫面格數目。 目前必須設定為1或-1。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法目前僅支援參數1或-1，因此您一次只能執行一個畫面格。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | 適用于 Windows XP 或更新版本的 Windows Media Player。<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Controls 物件**](controls-object.md)
</dt> <dt>

[**DVD 物件**](dvd-object.md)
</dt> </dl>

 

 





