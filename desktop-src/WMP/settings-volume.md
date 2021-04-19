---
title: 設定。磁片區
description: Volume 屬性會指定或抓取目前的磁片區。
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- 設定. 磁片區 Windows Media Player
topic_type:
- apiref
api_name:
- Settings.volume
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f5ec4299bf33ed16143eec8570b65c548599e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978686"
---
# <a name="settingsvolume"></a>設定。磁片區

**Volume** 屬性會指定或抓取目前的磁片區。

## <a name="syntax"></a>Syntax

player. 設定磁片區

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **號碼** (**長**) 範圍從0到100。

## <a name="remarks"></a>備註

零未指定磁片區，且100指定完整磁片區。 如果未指定此屬性的值，則會預設為播放程式的最後一個磁片區設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Settings 物件**](settings-object.md)
</dt> </dl>

 

 





