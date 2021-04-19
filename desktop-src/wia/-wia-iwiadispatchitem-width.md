---
description: 專案的寬度（以圖元為單位）。 唯讀。
ms.assetid: 4e636b76-af16-4fc1-8b88-2e0a2a24f841
title: Item. Width 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Width
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: db55ceb84a61b65c0e173c210e21fb486d0e1ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987547"
---
# <a name="itemwidth-property"></a>Item. Width 屬性

專案的寬度（以圖元為單位）。 唯讀。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Item.Width
```



## <a name="property-value"></a>屬性值

接收寬度的變數。

## <a name="remarks"></a>備註

如果專案是數位相機， **width** 屬性代表相機所產生影像的寬度。 如果專案是掃描器，這個屬性代表掃描床的寬度。 如果專案為影像，則此屬性代表影像的實際寬度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




