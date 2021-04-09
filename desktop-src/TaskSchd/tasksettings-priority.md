---
title: TaskSettings Priority 屬性
description: 針對腳本，取得或設定工作的優先權層級。
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Priority 屬性工作排程器
- Priority 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器，Priority 屬性
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282c688d63bb21f2dc0bab43acde7f089fa960b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934011"
---
# <a name="tasksettingspriority-property"></a>TaskSettings Priority 屬性

針對腳本，取得或設定工作的優先權層級。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a>屬性值

工作的優先權層級 (0-10) 。 預設值為 7。

## <a name="remarks"></a>備註

優先權層級0是最高優先順序，而優先順序層級10是最低優先順序。 預設值為 7。 優先權層級7和8用於背景工作，而優先順序層級4、5和6則用於互動式工作。

工作的動作會在具有以優先權類別值為基礎之優先權的進程中啟動。 優先權層級值 (執行緒優先順序) 用於 COM 處理常式、訊息方塊，以及電子郵件工作動作。 如需優先順序類別和優先權層級值的詳細資訊，請參閱 [排程優先順序](/windows/desktop/ProcThread/scheduling-priorities)。 下表列出 *priority* 參數的可能值，以及對應的 priority 類別和優先權層級值。



| 工作 *優先順序* | Priority 類別                 | 優先權層級                   |
|-----------------|--------------------------------|----------------------------------|
| 0               | 即時 \_ 優先權 \_ 類別      | 執行緒 \_ 優先順序 \_ 時間 \_ 嚴重不足 |
| 1               | 高 \_ 優先順序 \_ 類別          | 執行緒 \_ 優先順序 \_ 最高        |
| 2               | 高於 \_ 一般 \_ 優先順序 \_ 類別 | \_ \_ 高於 \_ 一般的執行緒優先順序  |
| 3               | 高於 \_ 一般 \_ 優先順序 \_ 類別 | \_ \_ 高於 \_ 一般的執行緒優先順序  |
| 4               | 一般 \_ 優先順序 \_ 類別        | 執行緒 \_ 優先順序 \_ 正常         |
| 5               | 一般 \_ 優先順序 \_ 類別        | 執行緒 \_ 優先順序 \_ 正常         |
| 6               | 一般 \_ 優先順序 \_ 類別        | 執行緒 \_ 優先順序 \_ 正常         |
| 7               | 低於 \_ 一般 \_ 優先順序 \_ 類別 | 一般的執行緒 \_ 優先順序 \_ \_  |
| 8               | 低於 \_ 一般 \_ 優先順序 \_ 類別 | 一般的執行緒 \_ 優先順序 \_ \_  |
| 9               | 閒置 \_ 優先權 \_ 類別          | 執行緒 \_ 優先順序 \_ 最低         |
| 10              | 閒置 \_ 優先權 \_ 類別          | 執行緒 \_ 優先順序 \_ 閒置           |



 

在讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) 元素中指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> </dl>

 

