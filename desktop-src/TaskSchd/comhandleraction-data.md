---
title: ComHandlerAction 屬性
description: 針對腳本，取得或設定與處理常式相關聯的其他資料。
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- 資料屬性工作排程器
- Data 屬性工作排程器，ComHandlerAction 物件
- ComHandlerAction 物件工作排程器、Data 屬性
topic_type:
- apiref
api_name:
- ComHandlerAction.Data
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254457941d55d9a6b130ec504563236e60baf7ba1a1d44d5851ed3c712634afb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139601"
---
# <a name="comhandleractiondata-property"></a>ComHandlerAction 屬性

針對腳本，取得或設定與處理常式相關聯的其他資料。

## <a name="syntax"></a>Syntax


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a>屬性值

處理常式所需的引數。

## <a name="remarks"></a>備註

讀取或寫入 XML 時，會在工作排程器架構的 [**資料**](taskschedulerschema-data-comhandlertype-element.md) 元素中指定 COM 處理常式的資料。

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

 

 





