---
description: Mobile 寬頻設定檔架構 v3。
ms.assetid: f7a3598f-57dd-4178-896f-31b4d2f65e56
title: Mobile 寬頻設定檔架構 v3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3fb4e939da9cbedadf8549539f73d0776e1636c6a0aea64a2cee2e7134e3edc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881571"
---
# <a name="mobile-broadband-profile-schema-v3"></a>Mobile 寬頻設定檔架構 v3

Windows 的8Mobile 寬頻設定檔架構 v3 可在命名空間中取得 `https://www.microsoft.com/networking/WWAN/profile/v3` 。

-   [行動寬頻設定檔架構 v3 元素](mobile-broadband-profile-schema-v3-elements.md)

``` syntax
<xs:schema targetNamespace="https://www.microsoft.com/networking/WWAN/profile/v3" 
    xmlns="https://www.microsoft.com/networking/WWAN/profile/v3"  
    xmlns:xs="https://www.w3.org/2001/XMLSchema" 
    xmlns:WWAN_profile_v2="https://www.microsoft.com/networking/WWAN/profile/v2"  
    elementFormDefault="qualified"> 

    <xs:import namespace="https://www.microsoft.com/networking/WWAN/profile/v2" schemaLocation="WWAN_profile_v2.xsd"/> 

    <!-- Flag to indicate whether this is an additional PDP context profile, default is "false" --> 
    <xs:element name="IsAdditionalPdpContextProfile" type="xs:boolean"/> 
</xs:schema> 
```

 

 



