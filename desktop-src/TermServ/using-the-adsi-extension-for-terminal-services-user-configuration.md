---
title: 使用遠端桌面服務使用者設定的 ADSI 擴充功能
description: 您可以使用 Active Directory 服務介面所執行的方法來管理遠端桌面服務特定的使用者屬性， (ADSI) 延伸模組，該擴充功能會與動態連結程式庫 Tsuserex.dll 一起封裝。
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- 使用 ADSI 擴充功能遠端桌面服務遠端桌面服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f115fecf1cce5c518e93206402f76e077109611
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933544"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a><span data-ttu-id="8e4a1-104">使用遠端桌面服務使用者設定的 ADSI 擴充功能</span><span class="sxs-lookup"><span data-stu-id="8e4a1-104">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>

<span data-ttu-id="8e4a1-105">遠端桌面服務使用者設定的 Active Directory 服務介面 (ADSI) 延伸模組是以動態連結程式庫 Tsuserex.dll 封裝的程式庫。</span><span class="sxs-lookup"><span data-stu-id="8e4a1-105">The Active Directory Service Interfaces (ADSI) extension for Remote Desktop Services user configuration is a library that is packaged with the dynamic-link library Tsuserex.dll.</span></span> <span data-ttu-id="8e4a1-106">您可以使用擴充功能所執行的方法，來管理遠端桌面服務特定的使用者屬性。</span><span class="sxs-lookup"><span data-stu-id="8e4a1-106">Administration of Remote Desktop Services-specific user properties is possible using the methods implemented by the extension.</span></span> <span data-ttu-id="8e4a1-107">這些方法可讓您設定遠端桌面服務使用者的擴充介面中可用的屬性。</span><span class="sxs-lookup"><span data-stu-id="8e4a1-107">The methods allow configuration of the properties that are available in the extension interface for Remote Desktop Services users.</span></span>

<span data-ttu-id="8e4a1-108">遠端桌面服務使用者設定的 ADSI 擴充功能可讓您檢查和操作儲存在目錄服務資料庫中的遠端桌面服務使用者屬性。</span><span class="sxs-lookup"><span data-stu-id="8e4a1-108">The ADSI extension for Remote Desktop Services user configuration supports the examination and manipulation of Remote Desktop Services user properties stored in the Directory Service database.</span></span> <span data-ttu-id="8e4a1-109">擴充功能也支援透過輕量型目錄存取協定 (LDAP) API，來設定儲存在 Active Directory 中的使用者屬性。</span><span class="sxs-lookup"><span data-stu-id="8e4a1-109">The extension also supports configuration of user properties that are stored in the Active Directory, through the Lightweight Directory Access Protocol (LDAP) API.</span></span>

<span data-ttu-id="8e4a1-110">提供者會執行下列方法：</span><span class="sxs-lookup"><span data-stu-id="8e4a1-110">The provider implements the following methods:</span></span>

-   <span data-ttu-id="8e4a1-111">[**IADs：： Get**](/windows/desktop/api/iads/nf-iads-iads-get)。</span><span class="sxs-lookup"><span data-stu-id="8e4a1-111">[**IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get).</span></span> <span data-ttu-id="8e4a1-112">這個方法會在類別的實例上搜尋特定的屬性或屬性集。</span><span class="sxs-lookup"><span data-stu-id="8e4a1-112">This method searches for a specific property or set of properties on an instance of the class.</span></span>
-   <span data-ttu-id="8e4a1-113">[**IADs：:P 的內容**](/windows/desktop/api/iads/nf-iads-iads-put)。</span><span class="sxs-lookup"><span data-stu-id="8e4a1-113">[**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put).</span></span> <span data-ttu-id="8e4a1-114">這個方法會在類別的實例上設定特定的屬性或屬性集。</span><span class="sxs-lookup"><span data-stu-id="8e4a1-114">This method configures a specific property or set of properties on an instance of the class.</span></span>

<span data-ttu-id="8e4a1-115">如需您可以設定之特定遠端桌面服務使用者屬性的清單，請參閱 [遠端桌面服務使用者設定的 ADSI 擴充](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) 功能的參考。</span><span class="sxs-lookup"><span data-stu-id="8e4a1-115">See the [Reference for the ADSI Extension for Remote Desktop Services User Configuration](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) for a list of the specific Remote Desktop Services user properties you can configure.</span></span>

<span data-ttu-id="8e4a1-116">如需使用 ADSI 存取和修改屬性的詳細資訊，請參閱 [使用 Adsi 存取及運算元據](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi)。</span><span class="sxs-lookup"><span data-stu-id="8e4a1-116">For more information about accessing and modifying attributes with ADSI, see [Accessing and Manipulating Data with ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).</span></span>

<span data-ttu-id="8e4a1-117">如需使用 ADSI 命名慣例和 AdsPath 字串的詳細資訊，請參閱[Active Directory Service 介面](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)平臺軟體發展工具組 (SDK) 檔中個別[ADSI 服務提供者](/windows/desktop/ADSI/adsi-system-providers)的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8e4a1-117">For more information about using ADSI naming conventions and AdsPath strings, see the information about individual [ADSI Service Providers](/windows/desktop/ADSI/adsi-system-providers) in the [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform Software Development Kit (SDK) documentation.</span></span>

 

 