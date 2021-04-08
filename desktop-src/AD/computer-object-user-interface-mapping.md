---
title: 消費者介面對應的電腦物件
description: 下表列出 Active Directory 消費者和電腦嵌入式管理單元中電腦物件屬性工作表的元素。
ms.assetid: e2a7a42d-e854-43fc-a36b-f3031c1685a7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2a2b3ed4ec8cbf3c1af59e024fc5e04bc68ae8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681686"
---
# <a name="computer-object-user-interface-mapping"></a>消費者介面對應的電腦物件

下表列出 Active Directory 消費者和電腦嵌入式管理單元中電腦物件屬性工作表的元素。

## <a name="general-property-sheet"></a>一般屬性工作表

下表列出 [ **一般** ] 屬性工作表的 UI 標籤。



| UI 標籤                         | Active Directory Domain Services 屬性 | 註解                                         |
|----------------------------------|--------------------------------------------|--------------------------------------------------|
| 電腦名稱稱 (Windows 2000 之前的)  | sAMAccountName                             |                                                  |
| DNS 名稱                         | dNSHostName                                |                                                  |
| 角色                             | userAccountControl                         | 切換 userAccountControl 位元遮罩中的位。 |
| 描述                      | description                                |                                                  |
| 信任電腦以進行委派    | userAccountControl                         | 切換 userAccountControl 位元遮罩中的位。 |



 

## <a name="location-property-sheet"></a>位置屬性工作表

下表列出 **Location** 屬性工作表的 UI 標籤。



| UI 標籤 | Active Directory Domain Services 屬性 |
|----------|--------------------------------------------|
| Location | location                                   |



 

## <a name="member-of-property-sheet"></a>屬性工作表的成員

下表列出屬性工作表 **成員** 的 UI 標籤。



| UI 標籤          | Active Directory Domain Services 屬性 | 註解                                                                                                                                                                   |
|-------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 成員隸屬         | memberOf                                   | 包含 UI 清單中的所有群組（主要群組除外），而主要群組是透過 [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) 屬性在廣告中表示。 |
| 設定主要群組 | primaryGroupID                             | LDAP：系結至主要群組的 [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) 。                                                                                  |



 

## <a name="operating-system-property-sheet"></a>作業系統屬性工作表

下表列出 **作業系統** 屬性工作表的 UI 標籤。



| UI 標籤     | Active Directory Domain Services 屬性 |
|--------------|--------------------------------------------|
| Name         | operatingSystem                            |
| 版本      | operatingSystemVersion                     |
| Service Pack | operatingSystemServicePack                 |



 

 

 