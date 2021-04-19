---
description: 指定用於驗證的認證類型。
ms.assetid: a56ce888-ec07-4ce8-a540-6d1890cb338d
title: authMode (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d699b27746226c3eb1550cfd9250e229b40a22e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991861"
---
# <a name="authmode-onex-element"></a>authMode (OneX) 元素

AuthMode (OneX) 元素會指定用於驗證的認證類型。 下表說明可能出現的值。



| 值         | 描述                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| machineOrUser | 使用電腦或使用者認證。 當使用者登入時，會使用使用者的認證進行驗證。 當使用者未登入時，會使用電腦認證。 |
| 機器       | 只使用電腦認證。                                                                                                                                           |
| 使用者          | 僅使用使用者認證。                                                                                                                                              |
| guest         | 僅使用來賓 (空白) 認證。                                                                                                                                     |



 

這是選擇性的項目。 當設定檔中未指定 authMode 時， `machineOrUser` 會使用的值。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。

``` syntax
<xs:element name="authMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="machineOrUser"
             />
            <xs:enumeration
                value="machine"
             />
            <xs:enumeration
                value="user"
             />
            <xs:enumeration
                value="guest"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**AuthMode** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。

## <a name="remarks"></a>備註

您可以使用 **netsh wlan set profileparameter** 命令，在命令列設定這個參數。 如需詳細資訊，請參閱 [無線區域網路 (wlan) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> </dl>

 

 
