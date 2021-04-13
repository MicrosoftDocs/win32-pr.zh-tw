---
title: RegistrationInfo URI 屬性
description: 針對腳本，取得或設定工作的 URI。
ms.assetid: 49085ee4-65e1-412c-ac1c-9c0f9efe5679
keywords:
- URI 屬性工作排程器
- URI 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器，URI 屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.URI
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77598d556fdec29f41004529471c8098314a6faf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509052"
---
# <a name="registrationinfouri-property"></a>RegistrationInfo URI 屬性

針對腳本，取得或設定工作的 URI。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.URI As String
```



## <a name="property-value"></a>屬性值

工作的 URI。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**URI**](taskschedulerschema-uri-registrationinfotype-element.md) 元素來指定工作 URI。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





