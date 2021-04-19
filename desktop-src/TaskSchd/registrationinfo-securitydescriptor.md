---
title: RegistrationInfo. SecurityDescriptor 屬性
description: 針對腳本，取得或設定工作的安全描述項。
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- SecurityDescriptor 屬性工作排程器
- SecurityDescriptor 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器、SecurityDescriptor 屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001290"
---
# <a name="registrationinfosecuritydescriptor-property"></a>RegistrationInfo. SecurityDescriptor 屬性

針對腳本，取得或設定工作的安全描述項。 如果在工作註冊期間提供不同的安全描述項，則會取代此屬性所設定的安全描述項。

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a>屬性值

與工作相關聯的安全描述項。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) 元素來指定工作的安全描述項。

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

 

 





