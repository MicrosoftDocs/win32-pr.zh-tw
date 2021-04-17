---
title: IWMDRMLicenseBackupRestoreStatus 介面
description: IWMDRMLicenseBackupRestoreStatus 介面會提供方法，以取得有關授權備份或還原作業的詳細狀態資訊。此介面會隨授權備份和還原作業期間產生的進度事件一起傳遞。
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- IWMDRMLicenseBackupRestoreStatus 介面 windows 媒體格式
- IWMDRMLicenseBackupRestoreStatus 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9db5d95daab78a506a3cc994fb9dd22153d0907
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315994"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a>IWMDRMLicenseBackupRestoreStatus 介面

**IWMDRMLicenseBackupRestoreStatus** 介面會提供方法，以取得有關授權備份或還原作業的詳細狀態資訊。

此介面會隨授權備份和還原作業期間產生的進度事件一起傳遞。 在授權備份期間會產生數個 **MEWMDRMLicenseBackupProgress** 事件，每個事件都有伴隨此介面的實例。 在授權還原期間產生的 **MEWMDRMLicenseRestoreProgress** 事件也是如此。

若要取出 **IWMDRMLicenseBackupRestoreStatus** 介面實例的指標，您必須先呼叫進度事件的 **IMFMediaEvent：： GetValue** 方法。 您從事件中取出的值是實 **IWMDRMLicenseBackupRestoreStatus** 介面之物件的 **IUnknown** 介面指標。

## <a name="members"></a>成員

**IWMDRMLicenseBackupRestoreStatus** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWMDRMLicenseBackupRestoreStatus** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMDRMLicenseBackupRestoreStatus** 介面具有這些方法。



| 方法                                                          | 描述                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) | 捕獲有關授權備份或還原作業的詳細狀態資訊。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**介面**](drm-interfaces.md)
</dt> </dl>

 

