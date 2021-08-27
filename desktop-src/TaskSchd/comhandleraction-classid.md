---
title: ComHandlerAction 的 ClassId 屬性
description: 針對腳本，取得或設定處理常式類別的識別碼。
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- ClassId 屬性工作排程器
- ClassId 屬性工作排程器，ComHandlerAction 物件
- ComHandlerAction 物件工作排程器，ClassId 屬性
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72338d4fe15936fcfe8f158098a798c4a3630cbd0587f46dc2f9346405477a59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100458"
---
# <a name="comhandleractionclassid-property"></a>ComHandlerAction 的 ClassId 屬性

針對腳本，取得或設定處理常式類別的識別碼。

## <a name="syntax"></a>Syntax


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a>屬性值

類別的識別碼，這個類別會定義要引發的處理常式。

## <a name="remarks"></a>備註

讀取或寫入 XML 時，會在工作排程器架構的 [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) 元素中指定 COM 處理常式的類別。

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

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





