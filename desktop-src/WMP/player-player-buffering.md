---
title: Media Player. 緩衝事件
description: 當 Windows Media Player 控制項開始或結束緩衝或下載時，就會發生緩衝事件。 |Media Player. 緩衝事件
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- 緩衝事件 Windows Media Player
- 緩衝事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player、緩衝事件
topic_type:
- apiref
api_name:
- Player.Buffering
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a73ac77f9b8e81162a6cc0f9220562caba26eae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995698"
---
# <a name="playerbuffering-event"></a>Media Player. 緩衝事件

當 Windows Media Player 控制項開始或結束緩衝或下載時，就會發生 **緩衝** 事件。

## <a name="syntax"></a>語法


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*開始* 
</dt> <dd>

包含下列其中一個值的 **布林** 值。



| 值 | 描述            |
|-------|------------------------|
| true  | 已開始緩衝。 |
| false | 緩衝處理已結束。   |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

您可以使用此事件來判斷何時啟動或停止緩衝或下載。 您可以針對案例和測試 *網路* 使用相同的事件區塊。**bufferingProgress** 和 *網路*。**downloadProgress** ，以判斷 Windows Media Player 目前是否正在緩衝或正在下載內容。

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BufferingProgress**](network-bufferingprogress.md)
</dt> <dt>

[**DownloadProgress**](network-downloadprogress.md)
</dt> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





