---
title: SavePreference
description: SavePreference 方法會在登錄中儲存喜好設定。
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- SavePreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89633d71dd75f4ef5e804aefddc85cf00ad5c03b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981656"
---
# <a name="themesavepreference"></a>SavePreference

**SavePreference** 方法會在登錄中儲存喜好設定。

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

**字串**，指定要儲存之喜好設定值的索引鍵。

</dd> <dt>

<span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*表示*
</dt> <dd>

**字串**，指定要儲存的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

喜好設定是一組索引鍵/值組，可以儲存在登錄中，以保留執行之間 Windows Media Player 狀態的相關資訊。 例如，您可以使用這項功能來儲存自訂設定，這樣就不需要在每次啟動 Windows Media Player 時重新輸入。

喜好設定不會加密，因此不是保存資料的安全方法。 請勿使用喜好設定來儲存私用資料。

## <a name="examples"></a>範例


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**主題元素**](theme-element.md)
</dt> <dt>

[**LoadPreference**](theme-loadpreference.md)
</dt> </dl>

 

 





