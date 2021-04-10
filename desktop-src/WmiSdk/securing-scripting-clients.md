---
description: 腳本和 Visual Basic 應用程式必須設定 DCOM 安全性，特別是針對遠端存取，而且可能也需要啟用許可權。
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: 保護腳本用戶端
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192072"
---
# <a name="securing-scripting-clients"></a><span data-ttu-id="64b68-103">保護腳本用戶端</span><span class="sxs-lookup"><span data-stu-id="64b68-103">Securing Scripting Clients</span></span>

<span data-ttu-id="64b68-104">腳本和 Visual Basic 應用程式必須設定 DCOM 安全性，特別是針對遠端存取，而且可能也需要啟用許可權。</span><span class="sxs-lookup"><span data-stu-id="64b68-104">Scripts and Visual Basic applications must set DCOM security, especially for remote access, and may also need to enable privileges.</span></span>

## <a name="default-access-permissions"></a><span data-ttu-id="64b68-105">預設存取權限</span><span class="sxs-lookup"><span data-stu-id="64b68-105">Default Access Permissions</span></span>

<span data-ttu-id="64b68-106">本機和遠端電腦之間的 WMI 存取不同。</span><span class="sxs-lookup"><span data-stu-id="64b68-106">WMI access differs between local and remote computers.</span></span> <span data-ttu-id="64b68-107">如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="64b68-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="64b68-108">以下是依帳戶的預設存取權限：</span><span class="sxs-lookup"><span data-stu-id="64b68-108">The following are the default access permissions by account:</span></span>

-   <span data-ttu-id="64b68-109">每個人、LocalService、NetworkService</span><span class="sxs-lookup"><span data-stu-id="64b68-109">Everyone, LocalService, NetworkService</span></span>

    <span data-ttu-id="64b68-110">讀取或寫入資料，以及在本機電腦上執行 [*提供者方法*](gloss-p.md) 的許可權。</span><span class="sxs-lookup"><span data-stu-id="64b68-110">Permission to read or write data and to run [*provider methods*](gloss-p.md) on the local computer.</span></span> <span data-ttu-id="64b68-111">這些帳戶無法建立新的類別或安裝新的提供者。</span><span class="sxs-lookup"><span data-stu-id="64b68-111">These accounts cannot create new classes or install new providers.</span></span>

-   <span data-ttu-id="64b68-112">系統管理員帳戶</span><span class="sxs-lookup"><span data-stu-id="64b68-112">Administrator accounts</span></span>

    <span data-ttu-id="64b68-113">在本機電腦上完全控制。</span><span class="sxs-lookup"><span data-stu-id="64b68-113">Full control on local computer.</span></span> <span data-ttu-id="64b68-114">當連接到遠端電腦時，該帳戶也必須是遠端電腦上的本機系統管理員。</span><span class="sxs-lookup"><span data-stu-id="64b68-114">When connecting to a remote computer, the account must be a local administrator on the remote computer also.</span></span>

## <a name="securing-a-scripting-client"></a><span data-ttu-id="64b68-115">保護腳本用戶端</span><span class="sxs-lookup"><span data-stu-id="64b68-115">Securing a Scripting Client</span></span>

<span data-ttu-id="64b68-116">WMI 腳本和 Visual Basic 應用程式必須適當地為其設為目標的作業系統設定 DCOM 安全性層級。</span><span class="sxs-lookup"><span data-stu-id="64b68-116">WMI scripting and Visual Basic applications must set DCOM security levels appropriately for the operating systems they are targeting.</span></span> <span data-ttu-id="64b68-117">如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="64b68-117">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="64b68-118">連接到遠端電腦時，您可能需要變更處理驗證 (NTLM 或 Kerberos) 的服務。</span><span class="sxs-lookup"><span data-stu-id="64b68-118">When connecting to a remote computer, you may need to change the service (NTLM or Kerberos) that handles authentication.</span></span> <span data-ttu-id="64b68-119">如需詳細資訊，請參閱 [使用 VBScript 設定驗證服務](setting-the-authentication-service-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="64b68-119">For more information, see [Setting the Authentication Service Using VBScript](setting-the-authentication-service-using-vbscript.md).</span></span>

<span data-ttu-id="64b68-120">存取某些 WMI 類別或資料可能需要未啟用的許可權。</span><span class="sxs-lookup"><span data-stu-id="64b68-120">Access to some WMI classes or data may require a privilege that is not enabled.</span></span> <span data-ttu-id="64b68-121">例如，連接到 [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) 類別時，您必須包含安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="64b68-121">For example, you must include the Security privilege when connecting to the [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) class.</span></span> <span data-ttu-id="64b68-122">如需詳細資訊，請參閱 [使用 VBScript 執行特殊許可權作業](executing-privileged-operations-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="64b68-122">For more information, see [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="64b68-123">如果您要從 Active Server Page (ASP) 存取 WMI，則需要進行一些 IIS 設定。</span><span class="sxs-lookup"><span data-stu-id="64b68-123">If you are accessing WMI from an Active Server Page (ASP), then some IIS configuration is required.</span></span> <span data-ttu-id="64b68-124">如需詳細資訊，請參閱 [為 WMI ASP 腳本設定 IIS 5.0 和更新版本](configuring-iis-5-for-wmi-asp-scripting.md)。</span><span class="sxs-lookup"><span data-stu-id="64b68-124">For more information, see [Configuring IIS 5.0 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>

<span data-ttu-id="64b68-125">您可能嘗試連接到需要加密連接的命名空間，換句話說，需要驗證層級的 pktPrivacy。</span><span class="sxs-lookup"><span data-stu-id="64b68-125">You may be trying to connect to a namespace which requires an encrypted connection, in other words, one that requires an authentication level of pktPrivacy.</span></span> <span data-ttu-id="64b68-126">如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="64b68-126">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

 

 
