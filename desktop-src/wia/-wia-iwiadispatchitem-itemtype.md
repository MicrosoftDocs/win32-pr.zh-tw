---
description: 這個專案的型別。 唯讀。
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Item. ItemType 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ItemType
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 3cbf60c935a88a62786c7c516ec0e768d65019c02d4419c44d928cee704a67b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450778"
---
# <a name="itemitemtype-property"></a>Item. ItemType 屬性

這個專案的型別。 唯讀。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a>屬性值

可能的值如下：



| 值  | 描述                                     |
|--------|-------------------------------------------------|
| 裝置 | 專案是 WIA 硬體裝置。              |
| folder | 專案是包含其他專案的資料夾。 |
| file   | 此專案是影像或音訊檔案。             |
| 音訊  | 專案是音訊剪輯。                      |
| image  | 此專案為影像。                           |



 

## <a name="remarks"></a>備註

一個專案可以有一個以上的類型。 例如，每個影像都是 "image" 和 "file" 類型。 **ItemType** 會傳回字串，其中包含專案的所有有效類型（以分號分隔）。 例如，"image; file"。 這個字串中沒有空格，結尾沒有分號。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




