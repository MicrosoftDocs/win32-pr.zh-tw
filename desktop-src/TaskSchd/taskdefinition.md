---
title: TaskDefinition 物件
description: 腳本物件，定義工作的所有元件，例如工作設定、觸發程式、動作和註冊資訊。
ms.assetid: d5887024-21af-40cf-a97d-f695f60394d9
keywords:
- TaskDefinition 物件工作排程器
- TaskDefinition 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d911218f64b386c08091f981903126f7506e3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508775"
---
# <a name="taskdefinition-object"></a>TaskDefinition 物件

腳本物件，定義工作的所有元件，例如工作設定、觸發程式、動作和註冊資訊。

## <a name="members"></a>成員

**TaskDefinition** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**TaskDefinition** 物件具有這些屬性。



| 屬性                                                               | 存取類型           | Description                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**行動**](taskdefinition-actions.md)<br/>                   | 讀取/寫入<br/> | 取得或設定工作所執行的動作集合。<br/>                                                                                                         |
| [**資料**](taskdefinition-data.md)<br/>                         | 讀取/寫入<br/> | 取得或設定與工作相關聯的資料。 工作排程器的服務會忽略這項資料，但想要擴充工作格式的協力廠商會使用此資料。<br/> |
| [**主要**](taskdefinition-principal.md)<br/>               | 讀取/寫入<br/> | 取得或設定工作的主體，此工作會提供工作的安全性認證。<br/>                                                                                 |
| [**RegistrationInfo**](taskdefinition-registrationinfo.md)<br/> | 讀取/寫入<br/> | 取得或設定用來描述工作的註冊資訊，例如工作的描述、工作的作者，以及工作的註冊日期。<br/> |
| [**設定**](taskdefinition-settings.md)<br/>                 | 讀取/寫入<br/> | 取得或設定定義工作排程器服務如何執行工作的設定。<br/>                                                                                      |
| [**觸發程序**](taskdefinition-triggers.md)<br/>                 | 讀取/寫入<br/> | 取得或設定用來啟動工作的觸發程式集合。<br/>                                                                                                         |
| [**XmlText**](taskdefinition-xmltext.md)<br/>                   | 讀取/寫入<br/> | 取得或設定工作的 XML 格式化定義。<br/>                                                                                                                       |



 

## <a name="remarks"></a>備註

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**task**](taskschedulerschema-task-element.md) 元素來指定工作定義。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md) 、 [事件觸發程式範例 (腳本) ](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))、 [每日觸發程式範例 (腳本 ](daily-trigger-example--scripting-.md)) 、 [註冊觸發 ](registration-trigger-example--scripting-.md)程式範例 (腳本) 、 [的觸發程式 ](weekly-trigger-example--scripting-.md)範例、 [登入觸發 ](logon-trigger-example--scripting-.md)程式範例 (腳本) ，或啟動觸發程式範例 [ (腳本) ](boot-trigger-example--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





