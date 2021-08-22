---
description: SaveBookmark 方法會儲存目前的光碟位置和 MSWebDVD 物件的狀態，讓使用者可以在稍後返回相同的位置。
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: 'SaveBookmark 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fec3a109b97c0ccbcb9a98736a01bba625537f1369fa7986cb6b5a669d35b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072712"
---
# <a name="savebookmark-method"></a>SaveBookmark 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`SaveBookmark`方法會儲存目前的光碟位置和 **MSWebDVD** 物件的狀態，讓使用者可以在稍後返回相同的位置。

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

書簽是 DVD 導覽器目前狀態的快照。 這包括在光碟上播放的位置，以及選取的音訊和 subpictures 串流等資訊。 藉由儲存書簽，使用者就可以關閉應用程式、關閉電腦，然後稍後再返回，以繼續在離開的地方繼續觀看光碟，並與之前一樣的設定。 在任何指定的時間都只能儲存一個書簽。 當您呼叫時 `SaveBookmark` ，會覆寫舊的書簽。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>區段。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RestoreBookmark**](restorebookmark-method.md)
</dt> </dl>

 

 




