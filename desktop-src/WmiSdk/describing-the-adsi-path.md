---
description: 輕量型目錄存取協定 (LDAP) 需要您在 \) ldap Active Directory 服務介面 (ADSI) 路徑中使用反斜線 (字元來將某些字元換用。
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: 描述 ADSI 路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0ba1dafac273ab3564549a5caca44180161643
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387107"
---
# <a name="describing-the-adsi-path"></a>描述 ADSI 路徑

輕量型目錄存取協定 (LDAP) 需要您在 \\ ldap Active Directory 服務介面 (ADSI) 路徑中使用時，以反斜線 () 字元來 escape 某些字元。

、= +<>\# ; \\ "

只有 **ADSIPath** 屬性值才需要 escape 字元。

下列範例顯示如何定義 **ADSIPath** 屬性。 請注意， \# **CN** 屬性值 abc 中的字元 \# 會被轉義。


```C++
// #include <windows.h> for this code to compile

BSTR strObjPath = 
    SysAllocString(L"ds_user.ADSIPath=\"LDAP://CN=abc\#,"
                   L"CN=Users,DC=dsprovider,DC=nttest,"
                   L"DC=microsoft,DC=com\"");

// Use strObjectPath here.

SysFreeString(strObjPath); // Free memory resources.
```



> [!Note]  
> 如需有關在特定作業系統上支援和安裝此元件的詳細資訊，請參閱 [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md)。

 

 

 



