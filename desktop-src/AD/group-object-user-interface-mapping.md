---
title: 群組物件消費者介面對應
description: 本主題說明 [Active Directory 消費者和電腦] 嵌入式管理單元中的 [群組物件] 屬性工作表。屬性工作表 SheetManaged 之屬性 SheetMembers 屬性的一般屬性 SheetMember
ms.assetid: c0cd73f0-f09f-4645-966d-6149888ce482
ms.tgt_platform: multiple
keywords:
- 消費者介面對應 AD 的群組物件
- 消費者介面對應，群組物件廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308b3bafc24f8b8419b23c351d981f4f01961885cd535ac2d24b96cd62e17633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188962"
---
# <a name="group-object-user-interface-mapping"></a>群組物件消費者介面對應

本主題說明 [Active Directory 消費者和電腦] 嵌入式管理單元中的 [群組物件] 屬性工作表。

-   [一般屬性工作表](#general-property-sheet)
-   [屬性工作表的成員](#member-of-property-sheet)
-   [成員屬性表](#members-property-sheet)
-   [由屬性工作表管理](#managed-by-property-sheet)

## <a name="general-property-sheet"></a>一般屬性工作表

下表顯示 [ **一般** ] 屬性工作表的 UI 標籤。



| UI 標籤                      | Active Directory Domain Services 中的屬性     |
|-------------------------------|---------------------------------------------------|
| 組名 (預先 Windows 2000)  | [**SAM-帳戶-名稱**](/windows/desktop/ADSchema/a-samaccountname) |
| Description                   | [**描述**](/windows/desktop/ADSchema/a-description)         |
| 電子郵件                        | [**電子郵件地址**](/windows/desktop/ADSchema/a-mail)           |
| 群組領域                   | [**群組類型**](/windows/desktop/ADSchema/a-grouptype)            |
| 群組類型                    | [**群組類型**](/windows/desktop/ADSchema/a-grouptype)            |
| 備註                         | [**註解**](/windows/desktop/ADSchema/a-info)                    |



 

## <a name="member-of-property-sheet"></a>屬性工作表的成員

下表顯示內容表 **成員** 的 UI 標籤。



| UI 標籤  | Active Directory Domain Services 中的屬性 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 成員隸屬 | [**是-DL 的成員**](/windows/desktop/ADSchema/a-memberof)    | 包含此群組所屬群組的分辨名稱。 這份清單中每個群組的成員屬性包含此群組物件的分辨名稱。使用者介面不會直接修改是- [**DL**](/windows/desktop/ADSchema/a-memberof) 屬性的成員。 它會修改此物件所屬之群組物件的 [**成員**](/windows/desktop/ADSchema/a-member) 屬性。 Active Directory 伺服器 **會維護-DL** 屬性。<br/> |



 

## <a name="members-property-sheet"></a>成員屬性表

下表顯示 [ **成員** ] 屬性工作表的 UI 標籤。



| UI 標籤 | Active Directory Domain Services 中的屬性 | Description                                                           |
|----------|-----------------------------------------------|-----------------------------------------------------------------------|
| 成員  | [**成員**](/windows/desktop/ADSchema/a-member)               | 包含此群組物件成員的分辨名稱。 |



 

## <a name="managed-by-property-sheet"></a>由屬性工作表管理

下表顯示 [ **受管理** 的] 屬性工作表的 UI 標籤。



| UI 標籤                           | Active Directory Domain Services 中的屬性                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Name                               | [**管理者**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| 管理員可以更新成員資格清單 | 無。 具有「允許寫入成員」許可權的 ACE 會新增至依 **名稱** 識別的帳戶。                        |
| Office                             | 依 **名稱** 識別之帳戶的 [**實體傳遞 Office 名稱**](/windows/desktop/ADSchema/a-physicaldeliveryofficename)屬性。 |
| Street                             | 依 **名稱** 識別的帳戶 [**街道位址**](/windows/desktop/ADSchema/a-street)屬性。                                    |
| City                               | 依 **名稱** 識別之帳戶的 [**位置名稱**](/windows/desktop/ADSchema/a-l)屬性。                                          |
| 州/省                     | 依 **名稱** 識別之帳戶的 [**州/省名稱**](/windows/desktop/ADSchema/a-st)屬性。                                |
| 國家/區域                     | 依 **名稱** 識別之帳戶的 [**國家/地區名稱**](/windows/desktop/ADSchema/a-c)屬性。                                           |
| 電話號碼                   | 依 **名稱** 識別之帳戶的 [**電話號碼**](/windows/desktop/ADSchema/a-telephonenumber)屬性。                         |
| 傳真號碼                         | 依 **名稱** 識別之帳戶的 [**傳真呼叫號碼**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)屬性。      |



 

 

