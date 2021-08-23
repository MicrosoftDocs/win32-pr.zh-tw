---
description: 收集器實例的控制權。 需要系統管理員 (BA) 許可權。
ms.assetid: 83b485b2-b03b-4882-a3ff-187eac299755
ms.tgt_platform: multiple
title: Control 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5eeccd31f3d9ab1f0b0ec05ebf80ea9f880a73fed21b21fe67fe63257af28871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589018"
---
# <a name="control-class"></a>Control 類別

收集器實例的控制權。 需要系統管理員 (BA) 許可權。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Provider("BootEventCollectorWmiProvider"), AMENDMENT]
class Control
{
};
```

## <a name="members"></a>成員

**控制項** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**控制項** 類別具有這些方法。



| 方法                                                         | 描述                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**檢查站**](control-checkpoint.md)                       | 如果目前的設定是復原/重做/還原的結果，請將它標示為已明確設定，讓歷程記錄保留設定的時間，並在下一次設定變更時建立備份檔案。 如果已明確設定目前的設定，就不會有任何作用。 在成功時傳回1，錯誤則為0。<br/> |
| [**DumpDiagnostics**](control-dumpdiagnostics.md)             | 將診斷資訊傾印到記錄檔中。<br/>                                                                                                                                                                                                                                                                                                                  |
| [**FastShutdown**](control-fastshutdown.md)                   | 快速停止收集器，並捨棄所有已排入佇列的資料。<br/>                                                                                                                                                                                                                                                                                                    |
| [**清除**](control-flush.md)                                 | 清除轉寄站緩衝區。<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**GetConfiguration**](control-getconfiguration.md)           | 讀取收集器的主動式設定。<br/>                                                                                                                                                                                                                                                                                                                |
| [**IsConfigurationEqual**](control-isconfigurationequal.md)   | 將引數與收集器的使用中設定進行比較。 如果兩者相符，則傳回1，否則傳回0。<br/>                                                                                                                                                                                                                                                 |
| [**ListBackups**](control-listbackups.md)                     | 傳回可還原的已儲存備份配置檔案清單。<br/>                                                                                                                                                                                                                                                                                  |
| [**取消復原**](control-redo.md)                                   | 從較新的備份檔案中重設收集器的使用中設定， (從目前的原始時間戳記) 開始判斷。 如果設定已復原，這表示會重做復原的變更。 在成功時傳回1，錯誤則為0。<br/>                                                                                                    |
| [**RestoreFile**](control-restorefile.md)                     | 從備份檔案還原收集器的主動式設定。 在成功時傳回1，錯誤則為0。<br/>                                                                                                                                                                                                                                                        |
| [**RestoreFromTime**](control-restorefromtime.md)             | 從以時間戳記選取的備份檔案還原收集器的使用中設定。 在成功時傳回1，錯誤則為0。<br/>                                                                                                                                                                                                                               |
| [**SetConfiguration**](control-setconfiguration.md)           | 設定收集器的新使用中設定。 在成功時傳回1，錯誤則為0。<br/>                                                                                                                                                                                                                                                                           |
| [**關機**](control-shutdown.md)                           | 停止收集器。 如果收集器是以服務方式執行，則停止服務是較佳的方法。<br/>                                                                                                                                                                                                                                                     |
| [**復原**](control-undo.md)                                   | 從先前的備份檔案還原收集器的使用中設定， (由從目前的原始時間戳記) 來判斷。 如果設定是剛設定的，這表示還原該變更。 連續的呼叫將會復原到先前和先前的設定。 在成功時傳回1，錯誤則為0。<br/>                           |
| [**ValidateConfiguration**](control-validateconfiguration.md) | 驗證設定文字的正確性，而不將其設定為使用中。 在成功時傳回1，錯誤則為0。<br/>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                          |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                       |
| 命名空間<br/>                | 根 \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



 

 




