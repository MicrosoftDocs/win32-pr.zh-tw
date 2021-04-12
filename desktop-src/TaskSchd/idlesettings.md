---
title: IdleSettings 物件
description: 腳本物件，指定當電腦處於閒置狀態時，工作排程器如何執行工作。
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- IdleSettings 物件工作排程器
- IdleSettings 物件工作排程器，說明
topic_type:
- apiref
api_name:
- IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 819ff226386f30483de96fac6213b35d7dd51a52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384366"
---
# <a name="idlesettings-object"></a>IdleSettings 物件

腳本物件，指定當電腦處於閒置狀態時，工作排程器如何執行工作。 如需有關閒置條件的詳細資訊，請參閱工作 [閒置條件](task-idle-conditions.md)。

## <a name="members"></a>成員

**IdleSettings** 物件具有下列類型的成員：

- [屬性](#properties)

### <a name="properties"></a>屬性

**IdleSettings** 物件具有這些屬性。

> [!NOTE]
> *IdleDuration* 和 *WaitTimeout* 設定已淘汰。 它們仍然存在於工作排程器的使用者介面中，而且其介面方法可能仍會傳回有效值，但不再使用這些值。

| 屬性                                                       | 存取類型           | Description                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](idlesettings-restartonidle.md)<br/> | 讀取/寫入<br/> | 取得或設定布林值，這個值表示當電腦迴圈進入閒置條件超過一次時，是否重新開機工作。<br/>            |
| [**StopOnIdleEnd**](idlesettings-stoponidleend.md)<br/> | 讀取/寫入<br/> | 取得或設定布林值，這個值表示如果閒置條件在工作完成之前結束，工作排程器將終止工作。<br/> |
| 已 **淘汰**： [ **IdleDuration**](idlesettings-idleduration.md)<br/>   | 讀取/寫入<br/> | 取得或設定值，這個值表示在工作執行之前，電腦必須處於閒置狀態的時間量。<br/>                            |
| 已 **淘汰**： [ **WaitTimeout**](idlesettings-waittimeout.md)<br/>     | 讀取/寫入<br/> | 取得或設定值，這個值會指出工作排程器等候閒置條件發生的時間量。<br/>                             |

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) 元素中指定。

如果工作是由閒置觸發程式觸發，則會忽略 [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) 屬性。

> [!NOTE]
> *IdleSettings. IdleDuration* 和 *IdleSettings. WaitTimeout* 已被取代。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |

## <a name="see-also"></a>另請參閱

[工作排程器物件](task-scheduler-objects.md)

[工作排程器](task-scheduler-start-page.md)
