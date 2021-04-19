---
title: ClosedCaption. getSAMIStyleName 方法
description: GetSAMIStyleName 方法會抓取目前的薩米文檔案所支援的樣式名稱。
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- getSAMIStyleName 方法 Windows Media Player
- getSAMIStyleName 方法 Windows Media Player，ClosedCaption 類別
- ClosedCaption 類別 Windows Media Player，getSAMIStyleName 方法
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMIStyleName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96480e28e0341b822aaf6726e63a6038681a577f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977477"
---
# <a name="closedcaptiongetsamistylename-method"></a>ClosedCaption. getSAMIStyleName 方法

**GetSAMIStyleName** 方法會抓取目前的薩米文檔案所支援的樣式名稱。

## <a name="syntax"></a>語法


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

**數值** (**long**) 指定要抓取之樣式名稱的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串** ，其中包含以薩米文檔案指定的樣式名稱。

## <a name="remarks"></a>備註

薩米文檔案中的樣式會依照檔案中顯示的順序編制索引，從零開始。

在 (*播放機* 開啟數位媒體檔案之前，無法使用此方法。**openState** 等於13個) 。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption 物件**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.SAMIStyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 





