---
title: DriveSpecifier
description: DriveSpecifier 屬性會抓取 CD 或 DVD 光碟機號。
ms.assetid: f592819e-61ba-4ae1-b748-b6f29df88067
keywords:
- DriveSpecifier Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom.driveSpecifier
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a358e54dabf9186dba3a2eb56f38d6fa846aab92f0a8cab6347f568788a1ae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864188"
---
# <a name="cdromdrivespecifier"></a>DriveSpecifier

**DriveSpecifier** 屬性會抓取 CD 或 DVD 光碟機號。

``` syntax
player.cdromCollection.item(
        index
        ).driveSpecifier
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串**。

## <a name="remarks"></a>備註

DVD 光碟機通常可以播放 CD 媒體，但 CD 光碟機無法播放 DVD 媒體。 這個屬性會在使用 *CdromCollection* 抓取的範圍內，針對以零為基礎的磁片磁碟機索引抓取磁片磁碟機規範。**計數**。 抓取的值採用 *x*：形式，其中 *X* 代表磁碟機號。

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

**Windows Media Player 10** 行動裝置版：不支援這個屬性。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *光碟*。**driveSpecifier** 以逗號分隔的可用 CD 和 DVD 光碟機清單來填滿名為 MYTEXT 的 HTML 文字區域。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Allocate an array to store the drive specifiers.
var MYdriveSpecifiers = new Array();

// Loop through the available drives using CdromCollection.count.
for (var i = 0; i < Player.cdRomCollection.count; i++){

// For each available drive, add a corresponding item 
// to the MYdriveSpecifiers array. 
    MYdriveSpecifiers[i] = Player.CDRomCollection.item(i).driveSpecifier;
}

// Write the array of drive letter specifiers to the text area.
myText.value = "Drive letters found: " + MYdriveSpecifiers;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 版本<br/>                  | Windows Media Player 7.0 版或更新版本<br/>                               |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Cdrom 物件**](cdrom-object.md)
</dt> <dt>

[**CdromCollection 計數**](cdromcollection-count.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





