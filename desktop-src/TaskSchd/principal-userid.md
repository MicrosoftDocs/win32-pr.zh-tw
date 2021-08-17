---
title: Principal. UserId 屬性
description: 針對腳本，取得或設定執行與主體相關聯之工作所需的使用者識別碼。
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- UserId 屬性工作排程器
- UserId 屬性工作排程器、Principal 物件
- Principal 物件工作排程器，UserId 屬性
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9501184f3316e464aa26f42d51e0b4c27eccaeb72d447faa91edaa33b0b4774c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060026"
---
# <a name="principaluserid-property"></a>Principal. UserId 屬性

針對腳本，取得或設定執行與主體相關聯之工作所需的使用者識別碼。

## <a name="syntax"></a>Syntax


```VB
Principal.UserId As String
```



## <a name="property-value"></a>屬性值

執行工作所需的使用者識別碼。

## <a name="remarks"></a>備註

如果在 [**GroupId**](principal-groupid.md) 屬性中指定群組識別碼，請勿設定此屬性。

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**UserId**](taskschedulerschema-userid-principaltype-element.md) 元素來指定主體的使用者識別碼。

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
</dt> <dt>

[**主要**](principal.md)
</dt> <dt>

[**Principal**](principal-groupid.md)
</dt> </dl>

 

 





