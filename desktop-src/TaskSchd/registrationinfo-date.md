---
title: RegistrationInfo。 Date 屬性
description: 針對腳本，取得或設定註冊工作的日期和時間。
ms.assetid: ecff01b6-a1de-458a-9728-34169f17d42b
keywords:
- Date 屬性工作排程器
- Date 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器，日期屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.Date
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adfdfa8b2dd3f8dcaa3b2fd5778b1e50dabfab51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966489"
---
# <a name="registrationinfodate-property"></a>RegistrationInfo。 Date 屬性

針對腳本，取得或設定註冊工作的日期和時間。

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Date As String
```



## <a name="property-value"></a>屬性值

工作的註冊日期。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**日期**](taskschedulerschema-date-registrationinfotype-element.md) 元素來指定註冊日期。

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

 

 





