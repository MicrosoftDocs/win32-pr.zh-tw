---
title: sessionStateChangeType 簡單類型
description: 定義終端機伺服器會話狀態變更的值，您可以用來觸發工作開始。
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- sessionStateChangeType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a77fb563b59ccd8d63d38c6c85f16ff74ac404b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466416"
---
# <a name="sessionstatechangetype-simple-type"></a>sessionStateChangeType 簡單類型

定義終端機伺服器會話狀態變更的值，您可以用來觸發工作開始。

``` syntax
<xs:simpleType name="sessionStateChangeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="ConsoleConnect"
         />
        <xs:enumeration
            value="ConsoleDisconnect"
         />
        <xs:enumeration
            value="RemoteConnect"
         />
        <xs:enumeration
            value="RemoteDisconnect"
         />
        <xs:enumeration
            value="SessionLock"
         />
        <xs:enumeration
            value="SessionUnlock"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>列舉值

**SessionStateChangeType** 簡單類型會定義下列值。



| 值             | 描述                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConsoleConnect    | 終端機伺服器主控台連接狀態變更。 例如，當您藉由切換電腦上的使用者，連接到本機電腦上的使用者會話時。 <br/>                            |
| ConsoleDisconnect | 終端機伺服器主控台中斷連接狀態變更。 例如，當您藉由切換電腦上的使用者，在本機電腦上中斷使用者會話的連線時。 <br/>                      |
| RemoteConnect     | 終端機伺服器遠端線上狀態變更。 例如，當使用者從遠端電腦使用遠端桌面連線程式連接到使用者會話時。 <br/>            |
| RemoteDisconnect  | 終端機伺服器遠端中斷連接狀態變更。 例如，當使用者從遠端電腦使用遠端桌面連線程式時，從使用者會話中斷連線。 <br/> |
| SessionLock       | 終端機伺服器會話鎖定狀態變更。 例如，此狀態變更會在電腦鎖定時執行工作。 <br/>                                                       |
| SessionUnlock     | 終端機伺服器會話已解除鎖定狀態變更。 例如，此狀態變更會在電腦解除鎖定時，讓工作執行。<br/>                                                    |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





