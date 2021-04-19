---
title: AudioLanguageChange 事件
description: 當目前的音訊語言變更時，就會發生 AudioLanguageChange 事件。 |AudioLanguageChange 事件
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- AudioLanguageChange 事件 Windows Media Player
- AudioLanguageChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，AudioLanguageChange 事件
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981119"
---
# <a name="playeraudiolanguagechange-event"></a>AudioLanguageChange 事件

當目前的音訊語言變更時，就會發生 **AudioLanguageChange** 事件。

## <a name="syntax"></a>語法


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*LangID* 
</dt> <dd>

 (**long**) 指定新地區設定識別碼 (LCID) 的 **數位**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

LCID 可唯一識別特定語言方言，稱為地區設定。

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入的 Microsoft JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CurrentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





