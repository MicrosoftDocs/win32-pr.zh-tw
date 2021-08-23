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
ms.openlocfilehash: dc0982eeba16d5760af5ba4a7334ed3e5050b3b730d727f7a10cb4b4a260d956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059996"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





