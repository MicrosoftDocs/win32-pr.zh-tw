---
title: attachmentsType 複雜類型
description: 定義用來指定與電子郵件訊息一起傳送之附件的元素。
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- attachmentsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce5bc25b74221112b487be58a729bffa47b8688d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999610"
---
# <a name="attachmentstype-complex-type"></a>attachmentsType 複雜類型

定義用來指定與電子郵件訊息一起傳送之附件的元素。

``` syntax
<xs:complexType name="attachmentsType">
    <xs:sequence>
        <xs:element name="File"
            type="nonEmptyString"
            minOccurs="0"
            maxOccurs="8"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                          | 類型                                                                    | Description                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**檔案**](taskschedulerschema-file-attachmentstype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | 指定以電子郵件訊息中的附件形式傳送之檔案的路徑。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





