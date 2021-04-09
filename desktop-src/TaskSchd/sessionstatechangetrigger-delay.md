---
title: SessionStateChangeTrigger Delay 屬性
description: 針對腳本，取得或設定值，這個值表示偵測到終端機伺服器會話狀態變更之後，啟動工作之前的延遲時間。
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Delay 屬性工作排程器
- Delay 屬性工作排程器，SessionStateChangeTrigger 物件
- SessionStateChangeTrigger 物件工作排程器，Delay 屬性
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd5afde8ebd2884aee19fbdafb785355b9fedb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094139"
---
# <a name="sessionstatechangetriggerdelay-property"></a>SessionStateChangeTrigger Delay 屬性

針對腳本，取得或設定值，這個值表示偵測到終端機伺服器會話狀態變更之後，啟動工作之前的延遲時間。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。

## <a name="syntax"></a>Syntax


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a>屬性值

偵測到終端機伺服器會話狀態變更之後，啟動工作之前所發生的延遲。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





