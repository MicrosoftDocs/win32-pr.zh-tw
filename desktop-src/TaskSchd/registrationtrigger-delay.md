---
title: RegistrationTrigger Delay 屬性
description: 針對腳本，取得或設定在註冊工作與啟動工作之間的時間長度。
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Delay 屬性工作排程器
- Delay 屬性工作排程器，RegistrationTrigger 物件
- RegistrationTrigger 物件工作排程器，Delay 屬性
topic_type:
- apiref
api_name:
- RegistrationTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad86017547ac4476f430e13e2566ddd6d3494226
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509124"
---
# <a name="registrationtriggerdelay-property"></a>RegistrationTrigger Delay 屬性

針對腳本，取得或設定在註冊工作與啟動工作之間的時間長度。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。

## <a name="syntax"></a>Syntax


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a>屬性值

註冊系統與啟動工作之間的時間長度。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**delay**](taskschedulerschema-delay-registrationtriggertype-element.md) 元素指定開機延遲。

如果註冊了具有延遲註冊觸發程式的工作，且在延遲期間關閉或重新開機工作的電腦，在執行工作之前，工作將不會執行，而且會遺失延遲。

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

 

 





