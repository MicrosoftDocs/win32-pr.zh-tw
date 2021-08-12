---
title: 設定。餘額
description: '[餘額] 屬性會指定或抓取目前的立體餘額。'
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- 設定餘額 Windows Media Player
topic_type:
- apiref
api_name:
- Settings.balance
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e569c40214655fc643762da8580bd8d6a16e098b99c649bb27e1a1485d498931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569573"
---
# <a name="settingsbalance"></a>設定。餘額

[ **餘額** ] 屬性會指定或抓取目前的立體餘額。

## <a name="syntax"></a>Syntax

播放機. 設定。餘額

## <a name="possible-values"></a>可能的值

這個屬性是 (**長**) 的讀取/寫入 **號碼**。 值的範圍是從100到100，預設值為零。

## <a name="remarks"></a>備註

值為零表示音訊在左右通道的相同磁片區上播放。 值為100表示音訊只會在左邊的頻道播放。 值為100表示音訊只會在右聲道上播放。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**設定物件**](settings-object.md)
</dt> </dl>

 

 





