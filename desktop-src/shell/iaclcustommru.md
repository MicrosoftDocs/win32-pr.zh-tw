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
ms.openlocfilehash: c4130ead959c326da55d2c02726c9db89ce363b616ea34cbfa545d179d1ee139
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937038"
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
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



 

 
