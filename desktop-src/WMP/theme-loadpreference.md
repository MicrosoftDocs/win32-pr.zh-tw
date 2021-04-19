---
title: LoadPreference
description: LoadPreference 方法會從登錄載入喜好設定。
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- LoadPreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979619"
---
# <a name="themeloadpreference"></a>LoadPreference

**LoadPreference** 方法會從登錄載入喜好設定。

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

**字串**，指定要載入之喜好設定值的索引鍵。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串**。

## <a name="remarks"></a>備註

喜好設定是一組索引鍵/值組，可以儲存在登錄中，以保留執行之間 Windows Media Player 狀態的相關資訊。 例如，您可以使用這項功能來儲存自訂設定，這樣就不需要在每次啟動 Windows Media Player 時重新輸入。

喜好設定不會加密，因此不是保存資料的安全方法。 請勿使用喜好設定來儲存私用資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**主題元素**](theme-element.md)
</dt> <dt>

[**SavePreference**](theme-savepreference.md)
</dt> </dl>

 

 





