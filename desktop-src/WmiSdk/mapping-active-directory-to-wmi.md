---
description: 目錄服務提供者會將 Active Directory 中的類別和實例鏡像至 WMI 輕量型目錄存取協定 (LDAP) 命名空間。
ms.assetid: 0215b614-cb10-4195-837d-bf81d523c560
ms.tgt_platform: multiple
title: 將 Active Directory 對應至 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0162f722eb8a053270ac2a8e75eaed4f1cd405
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987674"
---
# <a name="mapping-active-directory-to-wmi"></a><span data-ttu-id="492b2-103">將 Active Directory 對應至 WMI</span><span class="sxs-lookup"><span data-stu-id="492b2-103">Mapping Active Directory to WMI</span></span>

<span data-ttu-id="492b2-104">目錄服務提供者會將 Active Directory 中的類別和實例鏡像至 WMI 輕量型目錄存取協定 (LDAP) 命名空間。</span><span class="sxs-lookup"><span data-stu-id="492b2-104">The Directory Services Provider mirrors classes and instances from Active Directory into the WMI Lightweight Directory Access Protocol (LDAP) namespace.</span></span> <span data-ttu-id="492b2-105">由於這兩種環境的基本差異，您不能只是重新命名 Active Directory 的類別和實例，希望能夠正確地存取 WMI 中的類別和實例。</span><span class="sxs-lookup"><span data-stu-id="492b2-105">Because of fundamental differences in the two environments, you cannot simply rename the Active Directory classes and instances and hope to properly access those classes and instances in WMI.</span></span> <span data-ttu-id="492b2-106">目錄服務提供者會改為遵循命名規則，以保留存在於 Active Directory 類別和實例之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="492b2-106">Instead, the Directory Services provider follows naming rules to preserve the relationships that exist between the Active Directory classes and instances.</span></span>

<span data-ttu-id="492b2-107">下列主題提供對應 Active Directory 類別和實例的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="492b2-107">The following topics provide information about mapping Active Directory classes and instances:</span></span>

-   [<span data-ttu-id="492b2-108">對應 Active Directory 類別</span><span class="sxs-lookup"><span data-stu-id="492b2-108">Mapping Active Directory Classes</span></span>](mapping-active-directory-classes.md)
-   [<span data-ttu-id="492b2-109">Active Directory 實例的對應</span><span class="sxs-lookup"><span data-stu-id="492b2-109">Mapping Active Directory Instances</span></span>](mapping-active-directory-instances.md)

> [!Note]  
> <span data-ttu-id="492b2-110">如需有關在特定作業系統上支援和安裝此元件的詳細資訊，請參閱 [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md)。</span><span class="sxs-lookup"><span data-stu-id="492b2-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



