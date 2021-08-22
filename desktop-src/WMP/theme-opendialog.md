---
title: OpenDialog
description: OpenDialog 方法會開啟 [檔案] 對話方塊。
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- OpenDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d57218105aa081ddebcb98fadbdb40b4bbd42511de9df94e204320ce78cf03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134551"
---
# <a name="themeopendialog"></a>OpenDialog

**OpenDialog** 方法會開啟 [檔案] 對話方塊。

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*
</dt> <dd>

指定對話方塊類型的 **字串** 。 必須設定為 "FILE \_ OPEN"。

</dd> <dt>

<span id="parameters"></span><span id="PARAMETERS"></span>*參數*
</dt> <dd>

可以用來取得其他資訊的 **字串** 。 必須設定為 "FILES \_ ALLMEDIA"。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果使用者按一下 [取消]，這個方法會傳回 **字串** ，其中包含所選取檔案的 URL，或 "" (空白字串) 。

## <a name="remarks"></a>備註

此方法可用於本機硬碟或網路磁碟機機上的檔案。

## <a name="examples"></a>範例


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
    </BUTTON>
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
</dt> </dl>

 

 





