---
description: 公開方法，這些方法可用來初始化自動完成物件的最近使用 (MRU) 清單。
title: IACLCustomMRU 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU
api_type:
- COM
api_location: ''
ms.assetid: 6ebf64da-9eba-4ea7-91aa-242474097be1
ms.openlocfilehash: f47a9df320da5c710c21ddbab83ca87b49c28e12
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842009"
---
# <a name="iaclcustommru-interface"></a>IACLCustomMRU 介面

公開方法，這些方法可用來初始化自動完成物件的最近使用 (MRU) 清單。

## <a name="members"></a>成員

**IACLCustomMRU** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IACLCustomMRU** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IACLCustomMRU** 介面具有這些方法。



| 方法                                             | 描述                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [**AddMRUString**](iaclcustommru-addmrustring.md) | 將專案加入至 MRU 清單。<br/>                               |
| [**初始化**](iaclcustommru-initialize.md)     | 從登錄將字串清單載入至 MRU 清單。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



 

 
