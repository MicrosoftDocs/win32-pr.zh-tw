---
title: StartBoundary 屬性
description: 針對腳本，取得或設定啟動觸發程式的日期和時間。
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- StartBoundary 屬性工作排程器
- StartBoundary 屬性工作排程器，觸發程式物件
- 觸發程式物件工作排程器，StartBoundary 屬性
topic_type:
- apiref
api_name:
- Trigger.StartBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141e7e4d80d090e92ecb951917f60f972587d4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685731"
---
# <a name="triggerstartboundary-property"></a>StartBoundary 屬性

針對腳本，取得或設定啟動觸發程式的日期和時間。

## <a name="syntax"></a>Syntax


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a>屬性值

啟用觸發程式的日期和時間。 日期和時間必須採用下列格式： YYYY-MM-DD DDTHH： MM： SS (+-) HH： MM。 例如，太平洋時區2005年10月11日的日期將會寫入1:21:17 至 2005-10-11T13：21： 17-08：00。 格式的 (+-) HH： MM 區段會將時區描述為提前或後方的特定時數，國際標準時間 (格林尼治平均時間) 。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，觸發程式起始界限是在工作排程器架構的 [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) 元素中指定。

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

 

 





