---
title: ExecAction 物件
description: 腳本物件，代表執行命令列操作的動作。
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- 執行動作工作排程器，介面
- ExecAction 物件工作排程器
- ExecAction 物件工作排程器，說明
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cddd1b9b44612b4ce896fb3ceb99a6deeaa5e3a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105690"
---
# <a name="execaction-object"></a>ExecAction 物件

腳本物件，代表執行命令列操作的動作。

## <a name="members"></a>成員

**ExecAction** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ExecAction** 物件具有這些屬性。



| 屬性                                                            | 存取類型           | Description                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**引數**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | 讀取/寫入<br/> | 取得或設定與命令列操作相關聯的引數。<br/>                                                 |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | 讀取/寫入<br/> | 繼承自 [**動作**](action.md) 物件。 取得或設定動作的識別碼。<br/>                         |
| [**路徑**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | 讀取/寫入<br/> | 取得或設定可執行檔的路徑。<br/>                                                                           |
| [**類型**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | 唯讀<br/>  | 繼承自 [**動作**](action.md) 物件。 取得動作的類型。<br/>                                       |
| [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | 讀取/寫入<br/> | 取得或設定包含可執行檔的目錄，或可執行檔所使用的檔案。<br/> |



 

## <a name="remarks"></a>備註

如果在 [**Path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)、 [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)或 [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) 屬性中使用環境變數，則在啟動工作引擎) 的 Taskeng.exe (時，會快取並使用環境變數的值。 工作引擎啟動後所發生的環境變數變更將不會由工作引擎使用。

此動作會執行命令列操作。 例如，動作可以執行腳本或啟動可執行檔。

讀取或寫入 XML 時，會在工作排程器架構的 [**Exec**](taskschedulerschema-exec-actiongroup-element.md) 元素中指定執行動作。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





