---
title: 設定。餘額
description: '[餘額] 屬性會指定或抓取目前的立體餘額。'
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- 設定。餘額 Windows Media Player
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
ms.openlocfilehash: 248cd3b2bbf735ef54382fb5b1be52755cad3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982522"
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

[**Settings 物件**](settings-object.md)
</dt> </dl>

 

 





