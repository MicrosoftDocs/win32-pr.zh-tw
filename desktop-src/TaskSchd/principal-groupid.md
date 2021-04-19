---
title: Principal. GroupId 屬性
description: 針對腳本，取得或設定執行與主體相關聯之工作所需之使用者群組的識別碼。
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- GroupId 屬性工作排程器
- GroupId 屬性工作排程器、Principal 物件
- Principal 物件工作排程器，GroupId 屬性
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995166"
---
# <a name="principalgroupid-property"></a>Principal. GroupId 屬性

針對腳本，取得或設定執行與主體相關聯之工作所需之使用者群組的識別碼。

## <a name="syntax"></a>Syntax


```VB
Principal.GroupId As String
```



## <a name="property-value"></a>屬性值

與此主體相關聯之使用者群組的識別碼。

## <a name="remarks"></a>備註

如果在 [**UserId**](principal-userid.md) 屬性中指定使用者識別碼，請勿設定此屬性。

讀取或寫入工作的 XML 時，會在工作排程器架構的 [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) 元素中指定主體的群組識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**UserId**](principal-userid.md)
</dt> <dt>

[**主要**](principal.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





