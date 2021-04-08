---
description: Mobile 寬頻設定檔架構 v3。
ms.assetid: f7a3598f-57dd-4178-896f-31b4d2f65e56
title: Mobile 寬頻設定檔架構 v3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea42c0c4b6384b85e5373d6537f52cf8c9499e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847986"
---
# <a name="mobile-broadband-profile-schema-v3"></a><span data-ttu-id="0bab8-103">Mobile 寬頻設定檔架構 v3</span><span class="sxs-lookup"><span data-stu-id="0bab8-103">Mobile Broadband Profile Schema v3</span></span>

<span data-ttu-id="0bab8-104">Windows 8Mobile 寬頻設定檔架構 v3 可在命名空間中使用 `https://www.microsoft.com/networking/WWAN/profile/v3` 。</span><span class="sxs-lookup"><span data-stu-id="0bab8-104">The Windows 8Mobile Broadband Profile Schema v3 is available in the namespace `https://www.microsoft.com/networking/WWAN/profile/v3`.</span></span>

-   [<span data-ttu-id="0bab8-105">行動寬頻設定檔架構 v3 元素</span><span class="sxs-lookup"><span data-stu-id="0bab8-105">Mobile Broadband Profile Schema v3 Elements</span></span>](mobile-broadband-profile-schema-v3-elements.md)

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

 

 



