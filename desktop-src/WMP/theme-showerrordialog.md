---
title: ShowErrorDialog
description: ShowErrorDialog 方法會顯示 [標準錯誤] 對話方塊。
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- ShowErrorDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf5affd0989f0bebf57c821b32679fcbd03b03093e9e6d66f176bb66bdbd57d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117932503"
---
# <a name="themeshowerrordialog"></a>ShowErrorDialog

**ShowErrorDialog** 方法會顯示 [標準錯誤] 對話方塊。

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果 **設定 enableErrorDialogs** ，則可以使用這個方法，以程式設計方式顯示錯誤對話方塊。 如果錯誤佇列中沒有任何錯誤，則不會顯示 [錯誤] 對話方塊。

若為 Windows Media Player 9 系列或更新版本，則必須從錯誤事件處理常式呼叫這個方法。 Windows Media Player 9 系列或更新版本會在引發錯誤事件之後，清除面板的錯誤佇列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**主題元素**](theme-element.md)
</dt> <dt>

[**設定. enableErrorDialogs**](settings-enableerrordialogs.md)
</dt> </dl>

 

 





