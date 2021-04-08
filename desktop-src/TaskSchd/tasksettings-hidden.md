---
title: TaskSettings： Hidden 屬性
description: 針對腳本，取得或設定布林值，指出工作將不會顯示在 UI 中。
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Hidden 屬性工作排程器
- Hidden 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器，隱藏的屬性
topic_type:
- apiref
api_name:
- TaskSettings.Hidden
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057a3d920ba70260d23ad13a5888072ab5b07767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686217"
---
# <a name="tasksettingshidden-property"></a>TaskSettings： Hidden 屬性

針對腳本，取得或設定布林值，指出工作將不會顯示在 UI 中。 不過，系統管理員可以使用「主要交換器」來覆寫這項設定，讓所有工作都顯示在 UI 中。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a>屬性值

若 **為 True**，此值表示工作將不會顯示在 UI 中。 如果 **為 False**，則工作會顯示在 UI 中。 預設值為 **False**。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) 元素中指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





