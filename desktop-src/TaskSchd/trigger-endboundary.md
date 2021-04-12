---
title: EndBoundary 屬性
description: 針對腳本，取得或設定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- EndBoundary 屬性工作排程器
- EndBoundary 屬性工作排程器，觸發程式物件
- 觸發程式物件工作排程器，EndBoundary 屬性
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b385dddf186484bc17cff9f92d979cd64381335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024878"
---
# <a name="triggerendboundary-property"></a>EndBoundary 屬性

針對腳本，取得或設定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。

## <a name="syntax"></a>Syntax


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a>屬性值

停用觸發程式的日期和時間。 日期和時間必須採用下列格式： YYYY-MM-DD DDTHH： MM： SS (+-) HH： MM。 例如，太平洋時區2005年10月11日的日期將會寫入1:21:17 至 2005-10-11T13：21： 17-08：00。 格式的 (+-) HH： MM 區段會將時區描述為提前或後方的特定時數，國際標準時間 (格林尼治平均時間) 。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) 元素來指定 enabled 屬性。

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

 

 





