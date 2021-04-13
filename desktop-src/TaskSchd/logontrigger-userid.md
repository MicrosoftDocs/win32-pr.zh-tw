---
title: LogonTrigger。 UserId 屬性
description: 針對腳本，取得或設定使用者的識別碼。
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- UserId 屬性工作排程器
- UserId 屬性工作排程器，LogonTrigger 物件
- LogonTrigger 物件工作排程器，UserId 屬性
topic_type:
- apiref
api_name:
- LogonTrigger.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dde08f82742325303e62e405cd13d2b9e7c1191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384106"
---
# <a name="logontriggeruserid-property"></a>LogonTrigger。 UserId 屬性

針對腳本，取得或設定使用者的識別碼。

## <a name="syntax"></a>Syntax


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a>屬性值

使用者的識別碼。 例如，"MyDomain \\ MyName" 或本機帳戶 "Administrator"。

這個屬性可以是下列其中一種格式：

-   使用者名稱或 SID：當使用者登入電腦時，就會啟動工作。
-   Null：當任何使用者登入電腦時，就會啟動工作。

## <a name="remarks"></a>備註

如果您想要在群組的任何成員登入電腦而非特定使用者登入時觸發工作，則不要將值指派給 **LogonTrigger。 UserId** 屬性。 相反地，請使用 **LogonTrigger 的 UserId** 屬性建立登入觸發程式，並使用 [**principal**](principal-groupid.md) 屬性將值指派給工作的主體。

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) 元素來指定登入使用者識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LogonTrigger**](logontrigger.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





