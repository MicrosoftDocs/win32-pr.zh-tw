---
title: RepetitionPattern Duration 屬性
description: 針對腳本，取得或設定重複模式的時間長度。
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Duration 屬性工作排程器
- Duration 屬性工作排程器，RepetitionPattern 物件
- RepetitionPattern 物件工作排程器，Duration 屬性
topic_type:
- apiref
api_name:
- RepetitionPattern.Duration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b649562d4d28f5427427e72c03172aecdc9cdac803b0239c020806673cb0bae8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759207"
---
# <a name="repetitionpatternduration-property"></a>RepetitionPattern Duration 屬性

針對腳本，取得或設定重複模式的時間長度。

## <a name="syntax"></a>Syntax


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a>屬性值

模式重複的時間長度。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。 允許的最小時間是一分鐘。

如果未在持續時間內指定任何值，則會無限期地重複模式。

## <a name="remarks"></a>備註

如果您指定工作的重複持續時間，您也必須指定重複間隔。

讀取或寫入工作的 XML 時，重複期間會指定在工作排程器架構的 [**duration**](taskschedulerschema-duration-repetitiontype-element.md) 元素中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





