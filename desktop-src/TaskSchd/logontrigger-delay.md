---
title: LogonTrigger Delay 屬性
description: 針對腳本，取得或設定值，這個值表示使用者登入和工作啟動時間之間的時間量。
ms.assetid: 42198357-18e9-4fff-a8bf-f2da36148dc8
keywords:
- Delay 屬性工作排程器
- Delay 屬性工作排程器，LogonTrigger 物件
- LogonTrigger 物件工作排程器，Delay 屬性
topic_type:
- apiref
api_name:
- LogonTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce709b5095ffaeb9fdb5a4532f496ffa34c24e5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384109"
---
# <a name="logontriggerdelay-property"></a>LogonTrigger Delay 屬性

針對腳本，取得或設定值，這個值表示使用者登入和工作啟動時間之間的時間量。

## <a name="syntax"></a>Syntax


```VB
LogonTrigger.Delay As String
```



## <a name="property-value"></a>屬性值

值，指出使用者登入和工作啟動時間之間的時間量。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**delay**](taskschedulerschema-delay-logontriggertype-element.md) 元素指定登入觸發程式延遲。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LogonTrigger**](logontrigger.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





