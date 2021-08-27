---
description: Mobile 寬頻設定檔架構 v2。
ms.assetid: 0E140DCC-373C-44B3-8A91-F38AE7A5797C
title: Mobile 寬頻設定檔架構 v2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ea5420435b715c83757731d538b80857576982b2d4b0b426d96f86680f2b19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114348"
---
# <a name="mobile-broadband-profile-schema-v2"></a>Mobile 寬頻設定檔架構 v2

Windows 的8Mobile 寬頻設定檔架構 v2 可在命名空間中取得 `https://www.microsoft.com/networking/WWAN/profile/v2` 。

-   [Mobile 寬頻設定檔架構 v2 元素](mobile-broadband-profile-schema-v2-elements.md)

``` syntax
<xs:schema targetNamespace="https://www.microsoft.com/networking/WWAN/profile/v2"
    xmlns="https://www.microsoft.com/networking/WWAN/profile/v2" 
    xmlns:xs="https://www.w3.org/2001/XMLSchema"
    xmlns:WWAN_profile_v1="https://www.microsoft.com/networking/WWAN/profile/v1" 
    elementFormDefault="qualified">

    <xs:import namespace="https://www.microsoft.com/networking/WWAN/profile/v1" schemaLocation="WWAN_profile_v1.xsd"/>

    <!-- Flag to indicate whether this is a purchase profile, default is "false" -->
    <xs:element name="IsPurchaseProfile" type="xs:boolean"/>

    <!-- Display Provider Name -->
    <xs:element name="DisplayProviderName" type="WWAN_profile_v1:providerNameType"/>

</xs:schema>
```

 

 



