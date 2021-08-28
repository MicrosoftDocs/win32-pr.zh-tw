---
description: 為了增強 Windows Management Instrumentation (WMI) 共用的提供者主機進程 (wmiprvse.exe) 的安全性，已對 Windows 平臺進行了變更，以使用服務安全識別碼 (SID) 來保護提供者主機進程。
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: 用來控制提供者安全性的登錄機碼和值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916a5910a6ad21e9f9dfdcfc0992de10ae30da82
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884352"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a>用來控制提供者安全性的登錄機碼和值

為了增強 Windows Management Instrumentation (WMI) 共用的提供者主機進程 (wmiprvse.exe) 的安全性，已對 Windows 平臺進行了變更，以使用 [*服務安全識別碼 (SID)*](gloss-s.md)來保護提供者主機進程。 這些變更引進下列 WMI 共用主機的執行模式：安全且相容。

本主題包含下列章節：

-   [安全且相容的模式](#secure-and-compatible-modes)
-   [登錄機碼和值](#registry-keys-and-values)
-   [將提供者設定為在安全或相容模式中執行](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a>安全且相容的模式

從 Windows 7 開始，已新增下列兩個 WMI 共用主機進程的執行模式：

<dl> <dt>

<span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>安全模式
</dt> <dd>

WMI 提供者主機進程資源是以 [*服務 SID*](gloss-s.md)來保護。 只有 *服務 SID* 具有這些資源的許可權。

</dd> <dt>

<span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>相容模式
</dt> <dd>

WMI 共用提供者主機進程不會受到 [*服務 SID*](gloss-s.md)的保護。 視裝載模型而定，提供者主機進程允許存取 NetworkService 或 LocalService 帳戶。 如需裝載模型的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。

</dd> </dl>

**Windows Vista 和 Windows Server 2008：** 若要存取登錄機碼和值，以控制提供者主機進程的安全和相容模式，您必須在 [KB 959454](https://support.microsoft.com/kb/959454)中安裝安全性更新。 如需詳細資訊，請參閱 [Microsoft 資訊安全公告 MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx)。

## <a name="registry-keys-and-values"></a>登錄機碼和值

安全且相容的模式設定是透過登錄機碼來指定。 WMI 的登錄機碼位於 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ 的登錄中。

下列清單中所述的下列登錄機碼和 **DWORD** 值已加入，可控制 WMI 提供者的行為。

<dl> <dt>

<span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**
</dt> <dd>

此索引鍵控制個別提供者的行為。 此機碼中列出的所有提供者一律會在安全模式中執行。 隨附于 Windows 的所有收件匣提供者都會列在此機碼底下，並且預設會在安全模式下執行。

此索引鍵優先于 **CompatibleHostProviders** 索引鍵中所列的提供者。

</dd> <dt>

<span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**
</dt> <dd>

此索引鍵控制個別提供者的行為。 此機碼中列出的所有提供者一律會以相容模式執行。 依預設，此索引鍵是空的。

如果提供者同時列在 **SecuredHostProviders** 索引鍵和 **CompatibleHostProviders** 索引鍵中，則提供者會在安全模式中執行。

> [!Note]  
> 如果 **DefaultSecuredHost** 機碼設定為1，而且已知提供者無法在安全模式下運作， **CompatibleHostProviders** 索引鍵會為協力廠商應用程式提供應用程式相容性。

 

</dd> <dt>

<span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**
</dt> <dd>

全域登錄 **DWORD** 值，可判斷 **SecuredHostProviders** 或 **CompatibleHostProviders** 索引鍵中未列出的所有提供者是否在安全或相容模式中執行。 這個 **DWORD** 值可讓系統管理員決定協力廠商提供者必須執行的模式。 依預設，此值會設定為零，而且所有協力廠商提供者都會在相容模式中執行。 系統管理員可以藉由將 **DefaultSecuredHost** 值設定為1，使其電腦更安全。

> [!Note]  
> **DefaultSecuredHost** 值不會影響其他的登錄機碼。 **SecuredHostProviders** 索引鍵中所列的提供者會保留在安全模式中，而且 **CompatibleHostProviders** 機碼中列出的提供者仍會保持相容模式。

 

可能的設定如下：

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

指定提供者在相容模式中執行。

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

指定提供者在安全模式下執行。

</dd> </dl> </dd> </dl>

下列清單列出提供者的可能登錄設定和相關聯的執行模式。



| 列在 SecuredHostProviders 底下 | 列在 CompatibleHostProviders 底下 | DefaultSecuredHost 設定 | [模式]       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| 否                                | 否                                   | 0                          | 相容 |
| 否                                | 是                                  | 0                          | 相容 |
| 是                               | 否                                   | 0                          | 安全     |
| 是                               | 是                                  | 0                          | 安全     |
| 否                                | 否                                   | 1                          | 安全     |
| 否                                | 是                                  | 1                          | 相容 |
| 是                               | 否                                   | 1                          | 安全     |
| 是                               | 是                                  | 1                          | 安全     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a>將提供者設定為在安全或相容模式中執行

您可以使用群組原則管理主控台 (GPMC) 來修改登錄機碼。 如需詳細資訊，請參閱 [群組原則管理主控台](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal)。

下列程式說明如何使用群組原則喜好設定來管理安全且相容的模式設定。 如需群組原則喜好設定的詳細資訊，請參閱 [群組原則喜好設定總覽](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11))。

**使用群組原則將提供者新增至安全或相容模式**

1.  開啟 GPMC。
2.   (GPO) 建立群組原則物件。
3.  編輯 GPO。
4.  流覽至喜好設定/Windows 設定/Registry。
5.  以滑鼠右鍵按一下並選取 [新增]。 登錄。 此動作會顯示使用者介面，您可以在其中輸入登錄資訊。
6.  選取 [ **建立** ] 命令。
7.  選取下列登錄機碼路徑：

    **安全模式： HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **相容模式： HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  在 [ **名稱** ] 欄位中，輸入您要新增至此金鑰的提供者名稱。 提供者名稱的格式必須如下： &lt; 命名空間 &gt; ： <\_ \_ RELPATH>。 例如，根 \\ cimv2： \_ \_ win32provider. Name = "MyProvider"。
9.  在 [ **資料** ] 欄位中，輸入0。
10. 按一下 [確定]。

**若要使用群組原則從安全或相容模式移除提供者**

1.  開啟 GPMC。
2.  建立 GPO。
3.  編輯 GPO。
4.  流覽至喜好設定/Windows 設定/Registry。
5.  以滑鼠右鍵按一下並選取 [新增]。 登錄。 此動作會顯示使用者介面，您可以在其中輸入登錄資訊。
6.  選取 [ **移除** ] 命令。
7.  選取下列登錄機碼路徑：

    **安全模式： HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **相容模式： HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  在 [ **名稱** ] 欄位中，輸入您要從此索引鍵移除的提供者名稱。
9.  在 [ **資料** ] 欄位中，輸入0。
10. 按一下 [確定]。

下列程式提供有關如何修改未列在 **SecuredHostProviders** 或 **CompatibleHostProviders** 索引鍵中之提供者行為的詳細資料。

**使用群組原則來變更 DefaultSecuredHost 索引鍵的預設值**

1.  開啟 GPMC。
2.  建立 GPO。
3.  編輯 GPO。
4.  流覽至喜好設定/Windows 設定/Registry。
5.  以滑鼠右鍵按一下並選取 [新增]。 登錄。 此動作會顯示使用者介面，您可以在其中輸入登錄資訊。
6.  選取 [ **更新** ] 命令。
7.  選取下列登錄機碼路徑： **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**。
8.  在 [ **名稱** ] 欄位中，輸入 **DefaultSecuredHost**。
9.  在 [ **資料** ] 欄位中，輸入0表示相容模式，或輸入1表示安全模式。
10. 按一下 [確定]。

 

 
