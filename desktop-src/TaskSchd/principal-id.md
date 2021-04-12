---
title: Principal.Id 屬性
description: 針對腳本，取得或設定主體的識別碼。
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- Id 屬性工作排程器
- Id 屬性工作排程器、Principal 物件
- Principal 物件工作排程器、Id 屬性
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385009"
---
# <a name="principalid-property"></a>Principal.Id 屬性

針對腳本，取得或設定主體的識別碼。

## <a name="syntax"></a>Syntax


```VB
Principal.Id As String
```



## <a name="property-value"></a>屬性值

主體的識別碼。

## <a name="remarks"></a>備註

指定 [**actioncollection 動作**](actioncollection-context.md) 時，也會使用這個識別碼。

讀取或寫入工作的 XML 時，主體的識別碼會指定于工作排程器架構之 [**principal**](taskschedulerschema-principal-principaltype-element.md) 元素的 Id 屬性中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Actioncollection 動作。內容**](actioncollection-context.md)
</dt> <dt>

[**主要**](principal.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





