---
title: RunAs
description: 當遠端用戶端未撰寫為服務應用程式時，將類別設定為在特定使用者帳戶下執行。
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- RunAs 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106965866"
---
# <a name="runas"></a><span data-ttu-id="db8e6-104">RunAs</span><span class="sxs-lookup"><span data-stu-id="db8e6-104">RunAs</span></span>

<span data-ttu-id="db8e6-105">當遠端用戶端未撰寫為服務應用程式時，將類別設定為在特定使用者帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="db8e6-105">Configures a class to run under a specific user account when activated by a remote client without being written as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="db8e6-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="db8e6-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a><span data-ttu-id="db8e6-107">備註</span><span class="sxs-lookup"><span data-stu-id="db8e6-107">Remarks</span></span>

<span data-ttu-id="db8e6-108">值會指定使用者 *名稱，而且* 必須是 [使用者名稱]、[ *網域 ***\\*** 使用者* 名稱] 或 [互動式使用者] 字串格式。</span><span class="sxs-lookup"><span data-stu-id="db8e6-108">The value specifies the user name and must be either of the form *UserName*, *Domain ***\\*** UserName* or of the string "Interactive User".</span></span> <span data-ttu-id="db8e6-109">您也可以指定 "nt 授權 \\ localservice" (用於本機服務) 和 "nt 授權 \\ networkservice" (For Network service) 。</span><span class="sxs-lookup"><span data-stu-id="db8e6-109">You can also specify the strings "nt authority\\localservice" (for Local Service) and "nt authority\\networkservice" (for Network Service).</span></span> <span data-ttu-id="db8e6-110">\\當 {*AppID \_ GUID*} 參考到已啟動或在類別資料表中有專案的 COM 伺服器時，您也可以指定 "nt 授權單位系統" 字串。</span><span class="sxs-lookup"><span data-stu-id="db8e6-110">You can also specify the string "nt authority\\system" when {*AppID\_GUID*} refers to a COM server that is already started or that has an entry in the class table.</span></span> <span data-ttu-id="db8e6-111">不過，您無法使用「nt 授權單位系統」搭配 \\ 尚未啟動的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="db8e6-111">However, you cannot use "nt authority\\system" with a COM server that is not already started.</span></span> <span data-ttu-id="db8e6-112">"Nt 授權單位 \\ localservice"、"nt 授權單位 \\ networkservice" 和 "nt 授權單位系統" 的預設密碼 \\ 為 "" (空白字串) 。</span><span class="sxs-lookup"><span data-stu-id="db8e6-112">The default password for "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system" is "" (empty string).</span></span>

> [!Note]  
> <span data-ttu-id="db8e6-113">從 Windows Vista，您不再需要使用空白密碼來設定 "nt 授權單位 \\ localservice"、"nt 授權單位 \\ networkservice" 和 "nt 授權單位 \\ 系統" **RunAs** 設定。</span><span class="sxs-lookup"><span data-stu-id="db8e6-113">As of Windows Vista, an empty password is no longer required to configure the "nt authority\\localservice", "nt authority\\networkservice" and "nt authority\\system" **RunAs** settings.</span></span>

 

<span data-ttu-id="db8e6-114">設定為以特定使用者身分執行的類別可能無法在任何其他身分識別下註冊，因此使用此 CLSID 的 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) 呼叫會失敗，除非 COM 會代表實際的啟用要求啟動進程。</span><span class="sxs-lookup"><span data-stu-id="db8e6-114">Classes configured to run as a particular user may not be registered under any other identity, so calls to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) with this CLSID fail unless the process was launched by COM on behalf of an actual activation request.</span></span>

<span data-ttu-id="db8e6-115">使用者名稱是取自類別的 **AppID** 金鑰底下的 **RunAs** 值。</span><span class="sxs-lookup"><span data-stu-id="db8e6-115">The user-name is taken from the **RunAs** value under the class's **AppID** key.</span></span> <span data-ttu-id="db8e6-116">如果使用者名稱為「互動式使用者」，則會以目前登入之使用者的身分識別來執行伺服器，並連接到互動式桌面。</span><span class="sxs-lookup"><span data-stu-id="db8e6-116">If the user name is "Interactive User", the server is run in the identity of the user currently logged on and is connected to the interactive desktop.</span></span>

<span data-ttu-id="db8e6-117">否則，系統會從登錄的一部分取出密碼，而這部分只適用于電腦的系統管理員和系統的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="db8e6-117">Otherwise, the password is retrieved from a portion of the registry that is available only to administrators of the computer and to the system.</span></span> <span data-ttu-id="db8e6-118">然後，使用者名稱和密碼會用來建立伺服器執行所在的登入會話。</span><span class="sxs-lookup"><span data-stu-id="db8e6-118">The user-name and password are then used to create a logon session in which the server is run.</span></span> <span data-ttu-id="db8e6-119">以這種方式啟動時，使用者會使用自己的桌面和視窗來執行，且不會與互動式使用者或其他使用者帳戶中執行的其他使用者共用視窗控制碼、剪貼簿或其他 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="db8e6-119">When launched in this way, the user runs with its own desktop and window station and does not share window-handles, the clipboard, or other UI elements with the interactive user or other user running in other user accounts.</span></span>

<span data-ttu-id="db8e6-120">若要建立 **RunAs** 類別的密碼，您必須使用安裝在系統目錄中的 DCOMCNFG 系統管理工具。</span><span class="sxs-lookup"><span data-stu-id="db8e6-120">To establish a password for a **RunAs** class, you must use the DCOMCNFG administrative tool installed in the system directory.</span></span>

<span data-ttu-id="db8e6-121">針對 DCOM 伺服器所使用的 **RunAs** 身分識別，值中所指定的使用者帳戶必須具有以批次工作登入的許可權。</span><span class="sxs-lookup"><span data-stu-id="db8e6-121">For **RunAs** identities used by DCOM servers, the user account specified in the value must have the rights to log on as a batch job.</span></span> <span data-ttu-id="db8e6-122">您可以使用「本機安全性原則」系統管理工具來新增此許可權。</span><span class="sxs-lookup"><span data-stu-id="db8e6-122">This right can be added using Local Security Policy administrative tool.</span></span> <span data-ttu-id="db8e6-123">移至 [ **本機原則** ]，並開啟 [ **使用者權限指派**]。</span><span class="sxs-lookup"><span data-stu-id="db8e6-123">Go to **Local Policies** and open **User Rights Assignment**.</span></span> <span data-ttu-id="db8e6-124">選取 [ **以批次工作登** 入]，然後新增使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="db8e6-124">Select **Log on as a batch job**, and add the user account.</span></span>

<span data-ttu-id="db8e6-125">**RunAs** 值不會用於設定要以服務方式執行的伺服器。</span><span class="sxs-lookup"><span data-stu-id="db8e6-125">The **RunAs** value is not used for servers configured to be run as services.</span></span> <span data-ttu-id="db8e6-126">需要以 LocalSystem 以外的身分識別執行的 COM 服務應該使用服務控制台小程式或服務控制器功能來設定適當的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="db8e6-126">COM services that need to run under an identity other than LocalSystem should set the appropriate user name and password using the services control panel applet or the service controller functions.</span></span> <span data-ttu-id="db8e6-127"> (如需這些函式的詳細資訊，請參閱 [服務](/windows/desktop/Services/services)。 ) </span><span class="sxs-lookup"><span data-stu-id="db8e6-127">(For more information about these functions, see [Services](/windows/desktop/Services/services).)</span></span>

> [!Note]  
> <span data-ttu-id="db8e6-128">從 Microsoft Windows Server 2003 開始，類別 AppID 會明確地從 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ appid**（不同于大部分的登錄機碼）進行讀取，而無法與 **HKEY \_ 類別 \_ 根目錄 \\ appid** 交換。</span><span class="sxs-lookup"><span data-stu-id="db8e6-128">As of Microsoft Windows Server 2003, the class AppID is explicitly read from **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\AppID**, which, unlike most registry keys, is not interchangeable with **HKEY\_CLASSES\_ROOT\\AppID**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="db8e6-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="db8e6-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db8e6-130">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="db8e6-130">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 