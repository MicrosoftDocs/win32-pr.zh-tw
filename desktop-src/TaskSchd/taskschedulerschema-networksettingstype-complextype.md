---
title: networkSettingsType 複雜類型
description: 定義元素，這些專案提供工作排程器服務用來取得網路設定檔的設定。
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- networkSettingsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934590"
---
# <a name="networksettingstype-complex-type"></a>networkSettingsType 複雜類型

定義元素，這些專案提供工作排程器服務用來取得網路設定檔的設定。

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                              | 類型                                                        | Description                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**Id**](taskschedulerschema-id-networksettingstype-element.md)     | [**guidType**](taskschedulerschema-guidtype-simpletype.md) | 指定可識別網路設定檔的 GUID 值。 <br/>                       |
| [**Name**](taskschedulerschema-name-networksettingstype-element.md) | nonEmptyString                                              | 指定網路設定檔的名稱。 此名稱會用於顯示用途。 <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





