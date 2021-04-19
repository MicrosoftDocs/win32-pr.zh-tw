---
title: DomainChange 事件
description: 當 DVD 網域變更時，就會發生 DomainChange 事件。 |DomainChange 事件
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- DomainChange 事件 Windows Media Player
- DomainChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，DomainChange 事件
topic_type:
- apiref
api_name:
- Player.DomainChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9637913451aa5bba937906130899c46e0bd34d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989859"
---
# <a name="playerdomainchange-event"></a>DomainChange 事件

當 DVD 網域變更時，就會發生 **DomainChange** 事件。

## <a name="syntax"></a>語法


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strDomain* 
</dt> <dd>

表示新網域的 **字串**。 包含下列其中一個值。



| String            | Description                                                          |
|-------------------|----------------------------------------------------------------------|
| firstplay         | 執行 DVD 光碟的預設初始化。                     |
| videoManagerMenu  | 顯示整個光碟的功能表。也稱為根功能表或 topMenu。 |
| videoTitleSetMenu | 顯示目前標題集的功能表。 也稱為 titleMenu。     |
| title             | 顯示目前的標題。                                        |
| stop              | DVD 導覽器位於 DVD 停止網域中。                         |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | 適用于 Windows XP 或更新版本的 Windows Media Player。<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DVD 物件**](dvd-object.md)
</dt> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





