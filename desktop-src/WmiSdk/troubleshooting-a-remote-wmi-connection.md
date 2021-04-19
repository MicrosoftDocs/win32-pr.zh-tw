---
description: 下列各節描述開發人員建立遠端 WMI 連接時可能遇到的常見問題。
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: 疑難排解遠端 WMI 連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae475f91836b9e99b1c7faaf149c452e00a66722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993048"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a><span data-ttu-id="91e87-103">疑難排解遠端 WMI 連接</span><span class="sxs-lookup"><span data-stu-id="91e87-103">Troubleshooting a Remote WMI Connection</span></span>

<span data-ttu-id="91e87-104">下列各節描述開發人員建立遠端 WMI 連接時可能遇到的常見問題。</span><span class="sxs-lookup"><span data-stu-id="91e87-104">The following sections describe common issues developers may have with creating a remote WMI connection.</span></span>

<span data-ttu-id="91e87-105">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="91e87-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="91e87-106">DCOM 拒絕存取</span><span class="sxs-lookup"><span data-stu-id="91e87-106">DCOM Access Denied</span></span>](#dcom-access-denied)
-   [<span data-ttu-id="91e87-107">連接失敗</span><span class="sxs-lookup"><span data-stu-id="91e87-107">Failure to Connect</span></span>](#failure-to-connect)
-   [<span data-ttu-id="91e87-108">WMI 連接逾時</span><span class="sxs-lookup"><span data-stu-id="91e87-108">WMI Connection Timed Out</span></span>](#wmi-connection-timed-out)
-   [<span data-ttu-id="91e87-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="91e87-109">Related topics</span></span>](#related-topics)

## <a name="dcom-access-denied"></a><span data-ttu-id="91e87-110">DCOM 拒絕存取</span><span class="sxs-lookup"><span data-stu-id="91e87-110">DCOM Access Denied</span></span>

<dl> <dt>

<span data-ttu-id="91e87-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>症狀</span><span class="sxs-lookup"><span data-stu-id="91e87-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="91e87-112">您的連接失敗，並出現「DCOM 拒絕存取」錯誤，以及十進位值-2147024891 或 hex value0x80070005。</span><span class="sxs-lookup"><span data-stu-id="91e87-112">your connection failed with the error "DCOM Access Denied", along with the decimal value -2147024891 or hex value0x80070005.</span></span>

</dd> <dt>

<span data-ttu-id="91e87-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>問題</span><span class="sxs-lookup"><span data-stu-id="91e87-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="91e87-114">DCOM 可能未設定為允許 WMI 連接。</span><span class="sxs-lookup"><span data-stu-id="91e87-114">DCOM may not be configured to allow a WMI connection.</span></span>

</dd> <dt>

<span data-ttu-id="91e87-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>解析度</span><span class="sxs-lookup"><span data-stu-id="91e87-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="91e87-116">您可以使用 [DCOM 設定公用程式] (**DCOMCnfg.exe**) 在 **主控台** 的 [系統 **管理工具**] 中找到，來設定 WMI 的 dcom 設定。</span><span class="sxs-lookup"><span data-stu-id="91e87-116">You can configure DCOM settings for WMI using the DCOM Config utility (**DCOMCnfg.exe**) found in **Administrative Tools** in **Control Panel**.</span></span> <span data-ttu-id="91e87-117">此公用程式會公開設定，讓某些使用者透過 DCOM 從遠端連線到電腦。</span><span class="sxs-lookup"><span data-stu-id="91e87-117">This utility exposes the settings that enable certain users to connect to the computer remotely through DCOM.</span></span> <span data-ttu-id="91e87-118">系統管理員群組的成員預設允許遠端連線到電腦。</span><span class="sxs-lookup"><span data-stu-id="91e87-118">Members of the Administrators group are allowed to remotely connect to the computer by default.</span></span> <span data-ttu-id="91e87-119">您可以使用此公用程式來設定安全性，以啟動、存取及設定 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="91e87-119">With this utility you can set the security to start, access, and configure the WMI service.</span></span>

<span data-ttu-id="91e87-120">如需詳細資訊，請參閱 [保護遠端 WMI 連接](securing-a-remote-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="91e87-120">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

</dd> </dl>

## <a name="failure-to-connect"></a><span data-ttu-id="91e87-121">連接失敗</span><span class="sxs-lookup"><span data-stu-id="91e87-121">Failure to Connect</span></span>

<dl> <dt>

<span data-ttu-id="91e87-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>症狀</span><span class="sxs-lookup"><span data-stu-id="91e87-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="91e87-123">您無法連接到遠端系統上的 WMI。</span><span class="sxs-lookup"><span data-stu-id="91e87-123">You cannot connect to WMI on a remote system.</span></span>

</dd> <dt>

<span data-ttu-id="91e87-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>問題</span><span class="sxs-lookup"><span data-stu-id="91e87-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="91e87-125">您可能嘗試連接到不支援 WMI 的系統。</span><span class="sxs-lookup"><span data-stu-id="91e87-125">You may be trying to connect to a system that does not support WMI.</span></span> <span data-ttu-id="91e87-126">不支援下列作業系統版本之間的連接：</span><span class="sxs-lookup"><span data-stu-id="91e87-126">The following connections between operating system versions are not supported:</span></span>

-   <span data-ttu-id="91e87-127">您無法連接到執行 Starter、Basic 或 Home edition 的電腦。</span><span class="sxs-lookup"><span data-stu-id="91e87-127">You cannot connect to a computer that is running a Starter, Basic, or Home edition.</span></span>

<span data-ttu-id="91e87-128">或者，您可能嘗試連接到需要加密連接的命名空間，而該命名空間需要驗證層級 `pktPrivacy` 、 **WbemAuthenticationLevelPktPrivacy** 或 **RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權**。</span><span class="sxs-lookup"><span data-stu-id="91e87-128">Alternately, you may be trying to connect to a namespace which requires an encrypted connection, one that requires an authentication level of `pktPrivacy`, **WbemAuthenticationLevelPktPrivacy**, or **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

</dd> <dt>

<span data-ttu-id="91e87-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>解析度</span><span class="sxs-lookup"><span data-stu-id="91e87-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="91e87-130">如需詳細資訊，請參閱 [保護 WMI 命名空間](securing-wmi-namespaces.md)、 [保護 c + + 用戶端和提供者](securing-c---clients-and-providers.md)，或 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="91e87-130">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md), [Securing C++ Clients and Providers](securing-c---clients-and-providers.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

</dd> </dl>

## <a name="wmi-connection-timed-out"></a><span data-ttu-id="91e87-131">WMI 連接逾時</span><span class="sxs-lookup"><span data-stu-id="91e87-131">WMI Connection Timed Out</span></span>

<dl> <dt>

<span data-ttu-id="91e87-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>症狀</span><span class="sxs-lookup"><span data-stu-id="91e87-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="91e87-133">您的 WMI 連接逾時。</span><span class="sxs-lookup"><span data-stu-id="91e87-133">Your WMI connection times out.</span></span>

</dd> <dt>

<span data-ttu-id="91e87-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>問題</span><span class="sxs-lookup"><span data-stu-id="91e87-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="91e87-135">由於網路延遲問題，電腦只是無法及時回應。</span><span class="sxs-lookup"><span data-stu-id="91e87-135">Due to network lag issues, the computer is simply not able to respond in time.</span></span>

</dd> <dt>

<span data-ttu-id="91e87-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>解析度</span><span class="sxs-lookup"><span data-stu-id="91e87-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="91e87-137">當您透過呼叫 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 或 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)來連線到 WMI 時，可以將 **wbemConnectFlagUseMaxWait** 旗標 (腳本) 或 **WBEM 旗 \_ 標 \_ CONNECT \_ USE \_ MAX \_ WAIT** in c + + 值設定為 128 (0x80) 在呼叫上強加兩 (2) 分鐘的超時時間。</span><span class="sxs-lookup"><span data-stu-id="91e87-137">When connecting to WMI through a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) or [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), you can set the **wbemConnectFlagUseMaxWait** flag (scripting) or the **WBEM\_FLAG\_CONNECT\_USE\_MAX\_WAIT** in C++ value to 128 (0x80) to impose a two (2) minute time-out on the call.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="91e87-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="91e87-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91e87-139">連接至遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="91e87-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



