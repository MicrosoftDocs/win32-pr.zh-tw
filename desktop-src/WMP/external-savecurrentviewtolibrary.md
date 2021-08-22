---
title: SaveCurrentViewToLibrary 方法
description: SaveCurrentViewToLibrary 方法會從目前視圖中的媒體專案建立播放清單，並將播放清單儲存在本機文件庫中。
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- saveCurrentViewToLibrary 方法 Windows Media Player
- saveCurrentViewToLibrary 方法 Windows Media Player、External 類別
- External class Windows Media Player，saveCurrentViewToLibrary 方法
topic_type:
- apiref
api_name:
- External.saveCurrentViewToLibrary
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf14a6f712a72116860e7251edae73c91c4ef1dfb70876fd5f80dc329591673a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648438"
---
# <a name="externalsavecurrentviewtolibrary-method"></a>SaveCurrentViewToLibrary 方法

**SaveCurrentViewToLibrary** 方法會從目前視圖中的媒體專案建立播放清單，並將播放清單儲存在本機文件庫中。

## <a name="syntax"></a>語法


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*FriendlyListName* \[在\]
</dt> <dd>

**字串** ，指定播放清單的易記名稱。 Windows Media Player 在其使用者介面中顯示此名稱。

</dd> <dt>

*本機* \[在\]
</dt> <dd>

指定播放清單為動態或靜態的 **布林值**。 **TRUE** 指定動態，而 **FALSE** 指定靜態。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





