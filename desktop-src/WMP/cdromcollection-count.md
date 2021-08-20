---
title: CdromCollection 計數
description: Count 屬性會抓取系統上的可用 CD 和 DVD 光碟機數目。
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- CdromCollection Windows Media Player 計數
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db279f746640d09fac8b3852773afc27330fc9ca48d59a1470de7d42709e60f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864098"
---
# <a name="cdromcollectioncount"></a>CdromCollection 計數

**Count** 屬性會抓取系統上的可用 CD 和 DVD 光碟機數目。

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

DVD-ROM 磁片磁碟機的計算方式與 CD 光碟機完全一樣。 不過，Windows Media Player 控制項僅支援 Windows XP 或更新版本作業系統的 DVD 功能。 DVD 光碟機通常可以播放 CD 媒體，但 CD 光碟機無法播放 DVD 媒體。

**Windows Media Player 10** 行動裝置版：這個方法一律會傳回0。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *CdromCollection*。顯示使用者電腦上可用的 CD 和 DVD 光碟機數目的 **計數**。 使用 ID = "Player" 建立 player 物件。


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CdromCollection 物件**](cdromcollection-object.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





