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
ms.openlocfilehash: cf9c5fc6b01574b930b7b8b74186243d00fa5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319216"
---
# <a name="collection-object"></a>Collection 物件

Collection 類別

## <a name="members"></a>成員

**Collection** 物件有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Collection** 物件具有這些屬性。



| 屬性                                           | 存取類型          | Description                                                |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**計數**](-wia-icollection-count.md)<br/> | 唯讀<br/> | 傳回集合中的成員數目。<br/> |
| [**項目**](-wia-icollection-item.md)<br/>   | 唯讀<br/> | 傳回集合中的指定專案。<br/>    |



 

## <a name="remarks"></a>備註

### <a name="creationaccess-functions"></a>建立 \\ 存取函數

使用下列任何一項來取得物件的參考：



[**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md)

[**Children**](-wia-iwiadispatchitem-children.md)

[**設備**](-wia-iwia-devices.md)



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




