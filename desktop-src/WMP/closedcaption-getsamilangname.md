---
title: ClosedCaption. getSAMILangName 方法
description: GetSAMILangName 方法會抓取目前的薩米文檔案所支援的語言名稱。
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- getSAMILangName 方法 Windows Media Player
- getSAMILangName 方法 Windows Media Player，ClosedCaption 類別
- ClosedCaption 類別 Windows Media Player，getSAMILangName 方法
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d4150289eb7637d1772443a5437c6d245993ea0825a37d11bd7ec5accae918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764028"
---
# <a name="closedcaptiongetsamilangname-method"></a>ClosedCaption. getSAMILangName 方法

**GetSAMILangName** 方法會抓取目前的薩米文檔案所支援的語言名稱。

## <a name="syntax"></a>語法


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

**(** **long**) 指定要取出之語言名稱的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串** ，其中包含以薩米文檔案指定的語言名稱。

## <a name="remarks"></a>備註

薩米文檔案中的語言會依照檔案中顯示的順序編制索引，從零開始。

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

[**ClosedCaption.SAMILang**](closedcaption-samilang.md)
</dt> </dl>

 

 





