---
title: ITsSbResourcePluginStoreEx 介面
description: 公開可讓資源外掛程式儲存物件（例如會話和目標）的方法。
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- ITsSbResourcePluginStoreEx 介面遠端桌面服務
- ITsSbResourcePluginStoreEx 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23c3ba6689f52d592d9c9799b6c7bec0acd58e1afcbc8e7a18e0cb9dbe6db98b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351287"
---
# <a name="itssbresourcepluginstoreex-interface"></a>ITsSbResourcePluginStoreEx 介面

公開可讓資源外掛程式儲存物件（例如會話和目標）的方法。 這些方法會新增、刪除和查詢這些物件。

只有在已安裝[KB3091411](https://support.microsoft.com/kb/3091411)的 Windows Server 2012 R2 上才能使用此介面。 從 Windows Server 2016 開始，可以使用 [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)介面的 [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock)和 [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock)方法。

## <a name="members"></a>成員

**ITsSbResourcePluginStoreEx** 介面繼承自 [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)。 **ITsSbResourcePluginStoreEx** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITsSbResourcePluginStoreEx** 介面具有這些方法。



| 方法                                                                                                            | 描述                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**AcquireTargetLock**](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | 鎖定目標。<br/>                                                                                      |
| [**AddEnvironmentToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | 將環境新增至資源外掛程式存放區。<br/>                                                   |
| [**AddSessionToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | 將新的會話新增至資源外掛程式存放區。<br/>                                                    |
| [**AddTargetToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | 將目標新增至資源外掛程式存放區。<br/>                                                         |
| [**DeleteTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | 刪除目標。<br/>                                                                                    |
| [**EnumerateEnvironments**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | 傳回陣列，其中包含存在於資源外掛程式存放區中的環境。<br/>               |
| [**EnumerateFarms**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | 列舉已新增至資源外掛程式存放區的所有伺服器陣列。<br/>                         |
| [**EnumerateSessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | 列舉一組指定的會話。<br/>                                                              |
| [**EnumerateTargets**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | 傳回陣列，其中包含資源外掛程式存放區中存在的指定目標。<br/> |
| [**GetFarmProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | 抓取伺服器陣列的屬性。<br/>                                                                      |
| [**QueryEnvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | 傳回指定的環境物件。<br/>                                                            |
| [**QuerySessionBySessionId**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | 傳回具有指定之會話識別碼的會話物件。<br/>                                        |
| [**QueryTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | 傳回具有指定之目標名稱和伺服器陣列名稱的目標。<br/>                                 |
| [**ReleaseTargetLock**](itssbresourcepluginstoreex-releasetargetlock.md)                                         | 釋放目標的鎖定。<br/>                                                                         |
| [**RemoveEnvironmentFromStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | 從資源外掛程式存放區中移除指定的環境。<br/>                                   |
| [**SaveEnvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | 儲存環境。<br/>                                                                                |
| [**SaveSession**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | 儲存會話。<br/>                                                                                     |
| [**SaveTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | 儲存目標。<br/>                                                                                      |
| [**SetEnvironmentProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | 在環境上設定屬性。<br/>                                                                   |
| [**SetEnvironmentPropertyWithVersionCheck**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | 在環境上設定屬性。<br/>                                                                   |
| [**SetSessionState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | 設定工作階段的狀態。<br/>                                                                         |
| [**SetTargetProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | 設定目標上的屬性。<br/>                                                                         |
| [**SetTargetPropertyWithVersionCheck**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | 設定目標上的屬性。<br/>                                                                         |
| [**SetTargetState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | 設定目標的狀態。<br/>                                                                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                             |
| 伺服器支援結束<br/>    | Windows Server 2012 R2<br/>                                                             |
| IID<br/>                      | IID \_ ITsSbResourcePluginStoreEx 定義為80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[遠端桌面虛擬化介面](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 





