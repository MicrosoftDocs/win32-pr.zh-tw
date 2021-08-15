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
ms.openlocfilehash: e7d2e67876cd32b1db2181aba491090d44679756f5503c078d1edff495afc1cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440586"
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
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Wiavideo。h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




