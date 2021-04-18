---
title: IWMDRMLicenseManagement 介面
description: IWMDRMLicenseManagement 介面提供的方法會執行與本機授權存放相關的一般作業。若要取得這個介面的實例，請呼叫 IWMDRMProvider CreateObject。 將 IID \_ IWMDRMLicenseManagement 傳遞為 riid 參數。
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- IWMDRMLicenseManagement 介面 windows 媒體格式
- IWMDRMLicenseManagement 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14a7c555200e2eac99def75a1ad8c1d5dc1223fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312482"
---
# <a name="iwmdrmlicensemanagement-interface"></a>IWMDRMLicenseManagement 介面

**IWMDRMLicenseManagement** 介面提供的方法會執行與本機授權存放相關的一般作業。

若要取得這個介面的實例，請呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md)。 將 **IID \_ IWMDRMLicenseManagement** 傳遞為 *riid* 參數。

## <a name="members"></a>成員

**IWMDRMLicenseManagement** 介面繼承自 [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)。 **IWMDRMLicenseManagement** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMDRMLicenseManagement** 介面具有這些方法。



| 方法                                                                                               | 描述                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)                                     | 以非同步方式從指定的 URL 取得授權。<br/>                                                      |
| [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md)                                     | 在本機授權存放區中建立授權的備份。<br/>                                                 |
| [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md)                               | 從授權存放區移除標記的授權，並重組存放區以改善效能。<br/>             |
| [**CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | 根據參數值，建立以授權資訊填入的授權列舉值物件。<br/>            |
| [**CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | 產生授權撤銷挑戰。<br/>                                                                    |
| [**DeleteLicense**](iwmdrmlicensemanagement-deletelicense.md)                                       | 從暫時的本機授權存放區刪除授權。<br/>                                                    |
| [**MonitorLicenseAcquisition**](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | 開始監視授權取得程式。<br/>                                                      |
| [**ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | 刪除匯入的授權，以供原本以另一個內容保護系統保護的內容使用。<br/> |
| [**ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | 撤銷本機授權存放區的授權。<br/>                                                               |
| [**RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md)                                   | 還原先前備份的授權。<br/>                                                                      |
| [**StoreLicense**](iwmdrmlicensemanagement-storelicense.md)                                         | 將授權新增至本機授權存放區。<br/>                                                                   |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**介面**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





