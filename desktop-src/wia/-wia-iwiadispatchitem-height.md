---
description: 專案的高度（以圖元為單位）。 唯讀。
ms.assetid: 0df73d33-c1ae-43e1-b906-00540e04dfd9
title: Item. Height 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Height
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b9828fddf5630bfa1513fdb7913087054ad2c2c533468d69ca9b1b63e79b0341
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208344"
---
# <a name="itemheight-property"></a>Item. Height 屬性

專案的高度（以圖元為單位）。 唯讀。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Item.Height
```



## <a name="property-value"></a>屬性值

接收高度的變數。

## <a name="remarks"></a>備註

如果專案是數位相機， **height** 屬性代表此攝影機所產生影像的高度。 如果專案是掃描器，這個屬性代表掃描床的高度。 如果專案為影像，則此屬性代表影像的實際高度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




