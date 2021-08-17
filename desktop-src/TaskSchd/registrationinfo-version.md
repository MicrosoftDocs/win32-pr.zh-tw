---
title: RegistrationInfo 版本屬性
description: 針對腳本，取得或設定工作的版本號碼。
ms.assetid: 5f200948-b4ff-495c-9578-2a93b34fd75b
keywords:
- Version 屬性工作排程器
- Version 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器，Version 屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.Version
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08ef170004b7c9791f18cf65360c2446d5c87a6b835fb6fbcb048f47892c470
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059986"
---
# <a name="registrationinfoversion-property"></a>RegistrationInfo 版本屬性

針對腳本，取得或設定工作的版本號碼。

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Version As String
```



## <a name="property-value"></a>屬性值

工作的版本號碼。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**version**](taskschedulerschema-version-registrationinfotype-element.md) 元素來指定工作的版本號碼。

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

 

 





