---
description: Collection 類別
ms.assetid: 2b2a70ff-2b49-44b2-b506-b0b2cc953ec4
title: Collection 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Collection
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 63f2d1be37ae244eee5960feb8d5eae22ce379a8567bd782c3b0c3e43eabb53b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593338"
---
# <a name="collection-object"></a>Collection 物件

Collection 類別

## <a name="members"></a>成員

**Collection** 物件有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Collection** 物件具有這些屬性。



| 屬性                                           | 存取類型          | 描述                                                |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**計數**](-wia-icollection-count.md)<br/> | 唯讀<br/> | 傳回集合中的成員數目。<br/> |
| [**項目**](-wia-icollection-item.md)<br/>   | 唯讀<br/> | 傳回集合中的指定專案。<br/>    |



 

## <a name="remarks"></a>備註

### <a name="creationaccess-functions"></a>建立 \\ 存取函數

使用下列任何一項來取得物件的參考：



[**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md)

[**Children**](-wia-iwiadispatchitem-children.md)

[**裝置**](-wia-iwia-devices.md)



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




