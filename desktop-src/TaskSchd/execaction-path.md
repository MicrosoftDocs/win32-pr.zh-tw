---
title: ExecAction 路徑屬性
description: 針對腳本，取得或設定可執行檔的路徑。
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- 路徑屬性工作排程器
- Path 屬性工作排程器，ExecAction 物件
- ExecAction 物件工作排程器，Path 屬性
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685747"
---
# <a name="execactionpath-property"></a>ExecAction 路徑屬性

針對腳本，取得或設定可執行檔的路徑。

## <a name="syntax"></a>Syntax


```VB
ExecAction.Path As String
```



## <a name="property-value"></a>屬性值

動作要執行之可執行檔的路徑。

## <a name="remarks"></a>備註

此動作會執行命令列操作。 例如，動作可以執行腳本或啟動可執行檔。

讀取或寫入 XML 時，命令列作業路徑是在工作排程器架構的 [**command**](taskschedulerschema-command-exectype-element.md) 元素中指定。

檢查此路徑以確定它在註冊工作時有效，而不是在設定這個屬性時有效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





