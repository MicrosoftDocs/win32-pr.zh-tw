---
title: Principal (principalType) 元素
description: 指定主體的安全性認證。
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Principal 元素工作排程器
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8301371acc7624b4beb9b548191afa641ed267592b246cca7ba71ff170a9bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059776"
---
# <a name="principal-principaltype-element"></a>Principal (principalType) 元素

指定主體的安全性認證。 這些認證會定義工作執行所在的安全性內容。

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

**Principal** 元素是由 [**principalType**](taskschedulerschema-principaltype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                               | 衍生自                                                             | 描述                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**主體**](taskschedulerschema-principals-tasktype-element.md) | [**principalsType**](taskschedulerschema-principalstype-complextype.md) | 指定與工作相關聯的安全性主體。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                      | 類型                                                          | 描述                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) | **string**                                                    | 指定工作排程器 UI 中顯示之主體的名稱。<br/>                 |
| [**GroupId**](taskschedulerschema-groupid-principaltype-element.md)         | **string**                                                    | 指定執行與主體相關聯之工作所需之使用者群組的識別碼。<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)     | [**logonType**](taskschedulerschema-logontype-simpletype.md) | 指定執行與主體相關聯之工作所需的安全性登入方法。<br/>  |
| [**UserId**](taskschedulerschema-userid-principaltype-element.md)           | **string**                                                    | 指定執行與主體相關聯之工作所需的使用者識別碼。<br/>              |



## <a name="attributes"></a>屬性



| 名稱 | 類型 | 描述                                        |
|------|------|----------------------------------------------------|
| 識別碼   | 識別碼   | 主體定義的識別碼。<br/> |



## <a name="remarks"></a>備註

針對開發腳本，系統會使用 [**principal**](principal.md) 物件來指定主體的安全性認證。

針對 c + + 開發，系統會使用 [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) 介面來指定主體的安全性認證。

上方所列的子專案是由 [**principalType**](taskschedulerschema-principaltype-complextype.md) 複雜型別定義。 如需這些子項目的排序資訊，請參閱 [**principalType**](taskschedulerschema-principaltype-complextype.md)。

## <a name="examples"></a>範例

下列 XML 會定義具有使用者識別碼的主體。


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



下列 XML 會定義具有群組識別碼的主體。


```XML
<Principals>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





