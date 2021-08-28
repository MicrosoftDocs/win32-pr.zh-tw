---
title: LogonType (principalType) 元素
description: 指定執行與主體相關聯之工作所需的安全性登入方法。
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- LogonType 元素工作排程器
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9121179b744857d5e7d0bec5a2ae814c603c6b1c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885857"
---
# <a name="logontype-principaltype-element"></a>LogonType (principalType) 元素

指定執行與主體相關聯之工作所需的安全性登入方法。

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

**LogonType** 元素是由 [**principalType**](taskschedulerschema-principaltype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                  | 衍生自                                                           | 說明                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**主要**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | 指定主體的安全性認證。<br/> |



## <a name="remarks"></a>備註

**LogonType** 元素和 [**UserId**](taskschedulerschema-userid-principaltype-element.md)元素會一起使用，以定義執行使用此主體之工作所需的使用者。

針對腳本開發，主體的登入類型是由 [**LogonType**](principal-logontype.md) 屬性所指定。

針對 c + + 開發，主體的登入類型是由 [**IPrincipal：： LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) 屬性所指定。

此元素 (由 [**logonType**](taskschedulerschema-logontype-simpletype.md) 簡單類型定義) 必須具有下列其中一個值。

-   S4U：使用者必須使用服務登入使用者 (S4U) 登入。 使用 S4U 登入時，系統不會儲存任何密碼，也無法存取網路或加密檔案。
-   密碼：使用者必須使用密碼登入。
-   InteractiveToken：使用者必須已經登入。 此工作只會在現有的互動式會話中執行。

對於包含訊息方塊動作的工作，如果工作已啟動且工作具有互動式登入類型，就會顯示訊息方塊。 若要將工作登入類型設定為互動式，請在工作主體的 **&lt; &gt; LogonType** 元素中指定 **InteractiveToken** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





