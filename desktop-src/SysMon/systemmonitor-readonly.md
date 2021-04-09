---
title: SystemMonitor ReadOnly 屬性
description: 抓取或設定值，這個值會決定使用者是否可以修改控制項的屬性值。
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- ReadOnly 屬性 SysMon
- ReadOnly 屬性 SysMon，SystemMonitor 類別
- SystemMonitor 類別 SysMon，ReadOnly 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.ReadOnly
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f42481e1bb0df0966f09ee354421af6378969f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934335"
---
# <a name="systemmonitorreadonly-property"></a>SystemMonitor ReadOnly 屬性

抓取或設定值，這個值會決定使用者是否可以修改控制項的屬性值。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a>屬性值

如果您不想讓使用者修改控制項的屬性值，則為 True。否則為 false。 預設值為 false，表示使用者可以修改控制項的屬性值。

## <a name="remarks"></a>備註

當此屬性的值為 True 時，下列條件就會生效：

-   使用者無法使用內容功能表。
-   下列工具列按鈕已停用：
    -   新的計數器集合
    -   檢視目前的活動
    -   檢視記錄檔資料
    -   加
    -   刪除
    -   貼上計數器清單
    -   屬性

請注意，此屬性只會影響使用者透過使用者介面修改屬性值的能力，而不會讓您無法以程式設計方式修改屬性值或計數器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





