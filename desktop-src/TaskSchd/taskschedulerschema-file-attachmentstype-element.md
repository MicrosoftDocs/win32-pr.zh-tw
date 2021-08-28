---
title: File (attachmentsType) 元素
description: 包含以電子郵件訊息中的附件形式傳送之檔案的路徑。
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- File 元素工作排程器
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 793b23bc6b9d75ac809c42063fa9c300542705b718cd22253f6f2d3a1a76caa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125848"
---
# <a name="file-attachmentstype-element"></a>File (attachmentsType) 元素

包含以電子郵件訊息中的附件形式傳送之檔案的路徑。

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

**File** 元素是由 [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                      | 衍生自                                                               | 描述                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**附件 (sendEmailType)**](taskschedulerschema-attachments-sendemailtype-element.md) | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) | 包含電子郵件訊息中的附件清單。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IEmailAction 的附件屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments)。

如需腳本開發，請參閱 [**EmailAction。**](emailaction-attachments.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





