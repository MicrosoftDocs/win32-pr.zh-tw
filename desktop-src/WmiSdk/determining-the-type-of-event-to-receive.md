---
description: 在您註冊以接收事件之前，您必須決定要接收的事件種類：內部或外部。
ms.assetid: 46cdfcfa-42c6-4169-bc4d-725867224889
ms.tgt_platform: multiple
title: 判斷要接收的事件種類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9172e3246a31cb42ada3b9f5099bc3b0575959c125dedd44d7c6ed745134a4a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374648"
---
# <a name="determining-the-type-of-event-to-receive"></a>判斷要接收的事件種類

在您註冊以接收事件之前，您必須決定要接收的事件種類： [內部](#intrinsic-events) 或 [外部](#extrinsic-events)。 如需如何接收事件的詳細資訊，請參閱 [接收 WMI 事件](receiving-a-wmi-event.md)。 如需有關提供事件的詳細資訊，請參閱 [開發 WMI 提供者](developing-a-wmi-provider.md) 和 [撰寫事件提供者](writing-an-event-provider.md)。 如需有關接收和提供事件之安全性考慮的詳細資訊，請參閱 [保護 WMI 事件。](securing-wmi-events.md)

## <a name="intrinsic-events"></a>內建事件

內建事件是回應標準 WMI 資料模型變更時所發生的事件。 每個內建事件類別都表示特定的變更類型，並且會在 WMI 或提供者建立、刪除或修改命名空間、類別或類別執行個體時發生。 例如，建立 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)實例會導致 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)實例。

WMI 會針對儲存在 WMI 儲存機制中的物件建立內部事件。 提供者會為動態類別產生內建事件，但如果沒有可用的提供者，WMI 可以建立動態類別的實例。 WMI 會使用輪詢來偵測變更。 下表列出 WMI 用來報告內部事件的系統類別。



| System 類別                                                           | Description                                                                                                                                                                                             |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_\_ClassCreationEvent**](--classcreationevent.md)                 | 在建立類別時通知取用者。                                                                                                                                                            |
| [**\_\_ClassDeletionEvent**](--classdeletionevent.md)                 | 在類別刪除時通知取用者。                                                                                                                                                            |
| [**\_\_ClassModificationEvent**](--classmodificationevent.md)         | 在類別修改時通知取用者。                                                                                                                                                           |
| [**\_\_InstanceCreationEvent**](--instancecreationevent.md)           | 建立類別實例時通知取用者。                                                                                                                                                   |
| [**\_\_InstanceOperationEvent**](--instanceoperationevent.md)         | 當發生任何實例事件時（例如建立、刪除或修改實例），通知取用者。 您可以在查詢中使用這個類別，以取得與實例相關聯的所有類型事件。 |
| [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)           | 刪除實例時通知取用者。                                                                                                                                                        |
| [**\_\_InstanceModificationEvent**](--instancemodificationevent.md)   | 在修改實例時通知取用者。                                                                                                                                                       |
| [**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)         | 建立命名空間時通知取用者。                                                                                                                                                        |
| [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)         | 刪除命名空間時通知取用者。                                                                                                                                                        |
| [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) | 在命名空間遭到修改時通知取用者。                                                                                                                                                       |
| [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md)             | 當某些其他事件因為事件取用者的一部分而發生失敗時，通知取用者。                                                                                                 |
| [**\_\_EventDroppedEvent**](--eventdroppedevent.md)                   | 當某些其他事件遭到捨棄而不是傳遞給提出要求的事件取用者時，通知取用者。                                                                                       |
| [**\_\_EventQueueOverflowEvent**](--eventqueueoverflowevent.md)       | 當傳遞佇列溢位的結果卸載事件時，通知取用者。                                                                                                                  |
| [**\_\_MethodInvocationEvent**](--methodinvocationevent.md)           | 在方法呼叫事件發生時通知取用者。                                                                                                                                                    |



 

## <a name="extrinsic-events"></a>外來事件

外建事件是預先定義的出現專案，無法直接連結至 WMI 資料模型中的變更。 因此，WMI 會讓事件提供者定義描述事件的事件類別。 例如，描述切換至「待命」模式之電腦的事件是外來事件。 提供者衍生自 [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md)系統類別的外建事件，這是 [**\_ \_ 事件**](--event.md)系統類別的子類別。 [系統登錄](/previous-versions/windows/desktop/regprov/system-registry-provider)和 [SNMP](snmp-provider.md)提供者會定義外建事件類別，例如 **RegistryKeyChangeEvent**，這會在登錄機碼變更時通知取用者。 如需詳細資訊，請參閱 [註冊系統登錄事件](registering-for-system-registry-events.md) 和 [寫入事件提供者](writing-an-event-provider.md)。

在下列範例中，事件提供者會向一或多個大樓報告安全性違規。 您可以針對代表安全性違規的外來事件定義下列類別。

``` syntax
class SecurityViolationEvent : __ExtrinsicEvent
{
   string Building;           // building where violation occurred
   sint32 EntranceNumber;     // entrance where violation occurred
   datetime TimeOfDetection;  // date and time of violation
}
```

若要接收安全性違規通知，取用者會註冊 SecurityViolationEvent 事件種類。 除非另有指定，否則取用者會收到所有時間週期和所有大樓中所有安全性違規的通知。 事件類別也包含取用者可用來要求更多特定事件的資訊。

在下列範例中，查詢只會在建立24中註冊安全性違規事件的取用者。

`SELECT * FROM SecurityViolationEvent WHERE Building = 24;`

 

 
