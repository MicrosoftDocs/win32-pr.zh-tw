---
description: Item 物件的 TakePicture 方法會讓數位相機裝置拍攝圖片，並傳回代表所產生影像的專案物件。 此方法僅適用于數位相機裝置。
ms.assetid: d181048e-21ef-4fcc-a50a-5ba44bbde72e
title: 'TakePicture 方法 (Wiavideo .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.TakePicture
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: fd07f7ccd4f2c65c2d911dabdd0ca829dc241765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944315"
---
# <a name="itemtakepicture-method"></a>TakePicture 方法

[**Item**](-wia-item.md)物件的 **TakePicture** 方法會讓數位相機裝置拍攝圖片，並傳回代表所產生影像的 **專案** 物件。 此方法僅適用于數位相機裝置。

## <a name="syntax"></a>語法


```JScript
retVal = Item.TakePicture()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **IWiaDispatchItem**

代表這個方法所建立之影像的 [**專案**](-wia-item.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Wiavideo。h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




