---
description: 輕量型目錄存取協定 (LDAP) 需要您在 \) ldap Active Directory 服務介面 (ADSI) 路徑中使用反斜線 (字元來將某些字元換用。
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: 描述 ADSI 路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a6f3f28ffa5faa80dbd9f3d7906bba542e47e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513068"
---
# <a name="describing-the-adsi-path"></a><span data-ttu-id="8aa65-103">描述 ADSI 路徑</span><span class="sxs-lookup"><span data-stu-id="8aa65-103">Describing the ADSI Path</span></span>

<span data-ttu-id="8aa65-104">輕量型目錄存取協定 (LDAP) 需要您在 \) ldap Active Directory 服務介面 (ADSI) 路徑中使用反斜線 (字元來將某些字元換用。</span><span class="sxs-lookup"><span data-stu-id="8aa65-104">The Lightweight Directory Access Protocol (LDAP) requires that you escape some characters with a backslash (\) character when you use them in an LDAP Active Directory Service Interfaces (ADSI) path.</span></span>

<span data-ttu-id="8aa65-105">、= +<>\# ; \\ "</span><span class="sxs-lookup"><span data-stu-id="8aa65-105">,=+<>\#;\\"</span></span>

<span data-ttu-id="8aa65-106">只有 **ADSIPath** 屬性值才需要 escape 字元。</span><span class="sxs-lookup"><span data-stu-id="8aa65-106">The escape character is only required for the **ADSIPath** property value.</span></span>

<span data-ttu-id="8aa65-107">下列範例顯示如何定義 **ADSIPath** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8aa65-107">The following example shows how to define the **ADSIPath** property.</span></span> <span data-ttu-id="8aa65-108">請注意， \# **CN** 屬性值 abc 中的字元 \# 會被轉義。</span><span class="sxs-lookup"><span data-stu-id="8aa65-108">Note that the \# character in the **CN** property value of abc\# is escaped.</span></span>


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
> <span data-ttu-id="8aa65-109">如需有關在特定作業系統上支援和安裝此元件的詳細資訊，請參閱 [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md)。</span><span class="sxs-lookup"><span data-stu-id="8aa65-109">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



