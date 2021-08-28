---
title: 使用者識別屬性
description: 要求驗證的使用者身分識別會以數個不同的屬性提供給 NPS 擴充 Dll。
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- 屬性、使用者識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff099b46844f2259ad127346bb1ee2bfafccf4b116f3dba86dff3e175d11c28c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128758"
---
# <a name="user-identification-attributes"></a>使用者識別屬性

> [!Note]  
> 網際網路驗證服務 (IAS) 已重新命名網路原則伺服器 (NPS) 從 Windows Server 2008 開始。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

 

要求驗證的使用者身分識別會以數個不同的屬性提供給 NPS 擴充 Dll。

-   **ratUserName**
-   **ratStrippedUserName**
-   **ratFQUserName**

每個屬性都提供不同格式的使用者身分識別。 一般情況下，開發人員應該使用 **ratStrippedUserName**。 **RatUserName** 和 **ratFQUserName** 屬性的用法更加特製化。

> [!Note]  
> 當 User-Password 屬性（ **ratUserPassword**）傳送至擴充 DLL 時，已經解密，而且可以在該表單中使用。

 

## <a name="ratusername"></a>ratUserName

**RatUserName** 屬性包含實際透過網路傳送的名稱。 NPS 未以任何方式處理或驗證此屬性的內容。 這個屬性可能完全無法使用，因為使用者可能已經透過呼叫者識別碼之類的方法來識別。

使用 [**RadiusExtensionProcess/例如**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)，如果這個屬性可供使用，它只能在驗證延伸模組 DLL 外掛程式點使用。 **RatUserName** 屬性無法在授權延伸模組 dll 外掛程式點使用，因為在授權延伸 dll 中， **RadiusExtensionProcess/Ex** 函式只會看到 "傳出" 屬性。

使用 [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)時，如果此屬性可供使用，則可在驗證延伸模組 dll 外掛程式點和授權延伸模組 dll 外掛程式點上使用。

## <a name="ratstrippedusername"></a>ratStrippedUserName

在「領域移除」之後， **ratStrippedUserName** 是使用者的身分識別。 如需有關領域移除的詳細資訊，請參閱 HTTP： technet2.microsoft.com 的[領域名稱](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10))主題 \\ \\ 。

這個屬性可能存在於驗證延伸模組 DLL 外掛程式點、授權延伸模組 DLL 外掛程式點，或兩者。 這個屬性的格式保證如下：

* 網域 * 使用者 **\\** _名稱_

其中 *網域* 是 NetBIOS 功能變數名稱。

## <a name="ratfqusername"></a>ratFQUserName

**RatFQUserName** 屬性是「完整」使用者名稱。

這個屬性可能存在於驗證延伸模組 DLL 外掛程式點、授權延伸模組 DLL 外掛程式點或兩者中。 不過，這兩個外掛程式點之間的屬性格式可能不同。 在驗證延伸模組 DLL 外掛程式點上，這個屬性一律會採用下列格式：

* 網域 * 使用者 **\\** _名稱_

在授權延伸模組 DLL 外掛程式點的 **ratFQUserName** 屬性格式，取決於使用者是否為 Active Directory 的使用者。

-   如果使用者是本機使用者 **ratFQUserName** 與驗證延伸模組 DLL 外掛程式點的格式相同：

    * 網域 * 使用者 **\\** _名稱_

    .

-   如果使用者是 Active Directory 使用者， **ratFQUserName** 可能會以「標準」格式包含使用者的名稱。 標準格式是 Active Directory 用來識別使用者的格式。 它是從 Active Directory 樹狀結構的根路徑，其中包含使用者的組織單位 (OU) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定延伸模組 Dll](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[叫用擴充 Dll](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 