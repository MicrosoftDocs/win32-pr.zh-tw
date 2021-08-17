---
title: ExecAction. WorkingDirectory 屬性
description: 針對腳本，取得或設定包含可執行檔或可執行檔所使用之檔案的目錄。
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- WorkingDirectory 屬性工作排程器
- WorkingDirectory 屬性工作排程器，ExecAction 物件
- ExecAction 物件工作排程器、WorkingDirectory 屬性
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 362b6cbb977e66a92425da1355f0747660d867f67aec0ad684f7e8e3956edc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139441"
---
# <a name="execactionworkingdirectory-property"></a>ExecAction. WorkingDirectory 屬性

針對腳本，取得或設定包含可執行檔或可執行檔所使用之檔案的目錄。

## <a name="syntax"></a>Syntax


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a>屬性值

包含可執行檔或可執行檔所使用之檔案的目錄。

## <a name="remarks"></a>備註

讀取或寫入 XML 時，會在工作排程器架構的 [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) 元素中指定應用程式的工作目錄。

檢查此路徑以確定它在註冊工作時有效，而不是在設定這個屬性時有效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





