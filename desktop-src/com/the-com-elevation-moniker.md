---
title: COM 提高許可權的標記
description: COM 提高許可權的標記可讓在 [使用者帳戶控制] 下執行的應用程式 (UAC) ，以較高的許可權啟動 COM 類別。 如需詳細資訊，請參閱將焦點放在最低許可權。
ms.assetid: 1595ebb8-65af-4609-b3e7-a21209e64391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc80774764cb99e63ed3334a8c0f9c8cedd2500
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463805"
---
# <a name="the-com-elevation-moniker"></a><span data-ttu-id="01082-104">COM 提高許可權的標記</span><span class="sxs-lookup"><span data-stu-id="01082-104">The COM Elevation Moniker</span></span>

<span data-ttu-id="01082-105">COM 提高許可權的標記可讓在 [使用者帳戶控制] 下執行的應用程式 (UAC) ，以較高的許可權啟動 COM 類別。</span><span class="sxs-lookup"><span data-stu-id="01082-105">The COM elevation moniker allows applications that are running under user account control (UAC) to activate COM classes with elevated privileges.</span></span> <span data-ttu-id="01082-106">如需詳細資訊，請參閱將 [焦點放在最低許可權](/previous-versions/dotnet/articles/aa480194(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="01082-106">For more information, see [Focus on Least Privilege](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).</span></span>

## <a name="when-to-use-the-elevation-moniker"></a><span data-ttu-id="01082-107">使用提高許可權的標記時機</span><span class="sxs-lookup"><span data-stu-id="01082-107">When to Use the Elevation Moniker</span></span>

<span data-ttu-id="01082-108">提高許可權的標記是用來啟動 COM 類別，以完成需要較高許可權的特定且受限功能，例如變更系統日期和時間。</span><span class="sxs-lookup"><span data-stu-id="01082-108">The elevation moniker is used to activate a COM class to accomplish a specific and limited function that requires elevated privileges, such as changing the system date and time.</span></span>

<span data-ttu-id="01082-109">提高許可權需要同時參與 COM 類別和其用戶端。</span><span class="sxs-lookup"><span data-stu-id="01082-109">Elevation requires participation from both a COM class and its client.</span></span> <span data-ttu-id="01082-110">COM 類別必須設定為支援提高許可權，方法是標注其登錄專案，如需求一節中所述。</span><span class="sxs-lookup"><span data-stu-id="01082-110">The COM class must be configured to support elevation by annotating its registry entry, as described in the Requirements section.</span></span> <span data-ttu-id="01082-111">COM 用戶端必須使用提升許可權的標記來要求提高許可權。</span><span class="sxs-lookup"><span data-stu-id="01082-111">The COM client must request elevation by using the elevation moniker.</span></span>

<span data-ttu-id="01082-112">提高許可權的標記並非為了提供應用程式相容性。</span><span class="sxs-lookup"><span data-stu-id="01082-112">The elevation moniker is not intended to provide application compatibility.</span></span> <span data-ttu-id="01082-113">例如，如果您想要以提升許可權的伺服器來執行舊版 COM 應用程式（例如 WinWord），則應該將 COM 用戶端可執行檔設定為需要提高許可權，而不是使用提高許可權的標記來啟動繼承應用程式的類別。</span><span class="sxs-lookup"><span data-stu-id="01082-113">For example, if you want to run a legacy COM application such as WinWord as an elevated server, you should configure the COM client executable to require elevation, rather than activating the legacy application's class with the elevation moniker.</span></span> <span data-ttu-id="01082-114">當提高許可權的 COM 用戶端使用繼承應用程式的 CLSID 呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 時，用戶端的提高許可權狀態將會流向伺服器進程。</span><span class="sxs-lookup"><span data-stu-id="01082-114">When the elevated COM client calls [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) using the legacy application's CLSID, the client's elevated state will flow to the server process.</span></span>

<span data-ttu-id="01082-115">並非所有 COM 功能都與提高許可權相容。</span><span class="sxs-lookup"><span data-stu-id="01082-115">Not all COM functionality is compatible with elevation.</span></span> <span data-ttu-id="01082-116">將無法運作的功能包括：</span><span class="sxs-lookup"><span data-stu-id="01082-116">The functionality that will not work includes:</span></span>

-   <span data-ttu-id="01082-117">提高許可權不會從用戶端流向遠端 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="01082-117">Elevation does not flow from a client to a remote COM server.</span></span> <span data-ttu-id="01082-118">如果用戶端以提高許可權的標記啟動遠端 COM 伺服器，伺服器將不會提高許可權，即使它支援提高許可權也一樣。</span><span class="sxs-lookup"><span data-stu-id="01082-118">If a client activates a remote COM server with the elevation moniker, the server will not be elevated, even if it supports elevation.</span></span>
-   <span data-ttu-id="01082-119">如果提升許可權的 COM 類別在 COM 呼叫期間使用模擬，它可能會在模擬期間失去其較高的許可權。</span><span class="sxs-lookup"><span data-stu-id="01082-119">If an elevated COM class uses impersonation during a COM call, it might lose its elevated privileges during the impersonation.</span></span>
-   <span data-ttu-id="01082-120">如果提高許可權的 COM 伺服器在執行中的物件資料表中註冊類別 (衰減) ，則該類別將無法供非提高許可權的用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="01082-120">If an elevated COM server registers a class in the running object table (ROT), the class will not be available to non-elevated clients.</span></span>
-   <span data-ttu-id="01082-121">使用 UAC 機制提高許可權的進程不會在 COM 啟用期間載入每個使用者類別。</span><span class="sxs-lookup"><span data-stu-id="01082-121">A process elevated by using the UAC mechanism does not load per-user classes during COM activations.</span></span> <span data-ttu-id="01082-122">針對 COM 應用程式，這表示如果應用程式是由非特殊許可權的帳戶和特殊許可權帳戶使用，則必須在 **HKEY \_ 本機 \_ 電腦** 登錄 hive 中安裝應用程式的 COM 類別。</span><span class="sxs-lookup"><span data-stu-id="01082-122">For COM applications, this means that the application's COM classes must be installed in the **HKEY\_LOCAL\_MACHINE** registry hive if the application is to be used both by non-privileged and privileged accounts.</span></span> <span data-ttu-id="01082-123">如果特殊許可權帳戶從未使用過應用程式，則應用程式的 COM 類別只需要安裝在 **HKEY \_ USERS** hive 中。</span><span class="sxs-lookup"><span data-stu-id="01082-123">The application's COM classes need only be installed in the **HKEY\_USERS** hive if the application is never used by privileged accounts.</span></span>
-   <span data-ttu-id="01082-124">不允許從非提高許可權到提升許可權的應用程式使用拖放功能。</span><span class="sxs-lookup"><span data-stu-id="01082-124">Drag and drop is not allowed from non-elevated to elevated applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="01082-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="01082-125">Requirements</span></span>

<span data-ttu-id="01082-126">若要使用提升許可權的標記來啟動 COM 類別，必須將類別設定為以啟動使用者或 ' Activate as Activator ' 應用程式身分識別來執行。</span><span class="sxs-lookup"><span data-stu-id="01082-126">In order to use the elevation moniker to activate a COM class, the class must be configured to run as the launching user or the 'Activate as Activator' application identity.</span></span> <span data-ttu-id="01082-127">如果將類別設定為在任何其他身分識別下執行，則啟用會傳回錯誤的共同 \_ E \_ RUNAS \_ 值 \_ 必須 \_ 是 \_ AAA。</span><span class="sxs-lookup"><span data-stu-id="01082-127">If the class is configured to run under any other identity, the activation returns the error CO\_E\_RUNAS\_VALUE\_MUST\_BE\_AAA.</span></span>

<span data-ttu-id="01082-128">類別也必須以「易記」顯示名稱標注，該名稱是多語系使用者介面 (MUI) 相容。</span><span class="sxs-lookup"><span data-stu-id="01082-128">The class must also be annotated with a "friendly" display name that is multilingual user interface (MUI) compatible.</span></span> <span data-ttu-id="01082-129">這需要下列登錄專案：</span><span class="sxs-lookup"><span data-stu-id="01082-129">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

<span data-ttu-id="01082-130">如果遺漏此專案，啟用會傳回錯誤（共 E），即 \_ \_ 遺漏 \_ DISPLAYNAME。</span><span class="sxs-lookup"><span data-stu-id="01082-130">If this entry is missing, the activation returns the error CO\_E\_MISSING\_DISPLAYNAME.</span></span> <span data-ttu-id="01082-131">如果缺少 MUI 檔案，則會傳回 [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) 函式的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="01082-131">If the MUI file is missing, the error code from the [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) function is returned.</span></span>

<span data-ttu-id="01082-132">（選擇性）若要指定 UAC 使用者介面所顯示的應用程式圖示，請新增下列登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="01082-132">Optionally, to specify an application icon to be displayed by the UAC user interface, add the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

<span data-ttu-id="01082-133">**IconReference** 會使用與 **>localizedstring** 相同的格式：</span><span class="sxs-lookup"><span data-stu-id="01082-133">**IconReference** uses the same format as **LocalizedString**:</span></span>

<span data-ttu-id="01082-134">@*pathtobinary*、*-resourcenumber*</span><span class="sxs-lookup"><span data-stu-id="01082-134">@*pathtobinary*,*-resourcenumber*</span></span>

<span data-ttu-id="01082-135">此外，COM 元件也必須經過簽署，才能顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="01082-135">In addition, the COM component must be signed for the icon to be displayed.</span></span>

<span data-ttu-id="01082-136">COM 類別也必須標注為啟用 LUA。</span><span class="sxs-lookup"><span data-stu-id="01082-136">The COM class must also be annotated as LUA-Enabled.</span></span> <span data-ttu-id="01082-137">這需要下列登錄專案：</span><span class="sxs-lookup"><span data-stu-id="01082-137">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

<span data-ttu-id="01082-138">如果遺漏此專案，則啟用會傳回 \_ \_ 已停用的共同電子提高許可權錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="01082-138">If this entry is missing, then the activation returns the error CO\_E\_ELEVATION\_DISABLED.</span></span>

<span data-ttu-id="01082-139">請注意，這些專案必須存在於 HKEY \_ 本機 \_ 電腦 hive 中，而不是 HKEY \_ CURRENT \_ USER 或 HKEY \_ USERS hive。</span><span class="sxs-lookup"><span data-stu-id="01082-139">Note that these entries must exist in the HKEY\_LOCAL\_MACHINE hive, not the HKEY\_CURRENT\_USER or HKEY\_USERS hive.</span></span> <span data-ttu-id="01082-140">這可防止使用者提高本身沒有註冊之許可權的 COM 類別。</span><span class="sxs-lookup"><span data-stu-id="01082-140">This prevents users from elevating COM classes that they did not also have the privileges to register.</span></span>

## <a name="the-elevation-moniker-and-the-elevation-ui"></a><span data-ttu-id="01082-141">提高許可權的標記和提高許可權 UI</span><span class="sxs-lookup"><span data-stu-id="01082-141">The Elevation Moniker and the Elevation UI</span></span>

<span data-ttu-id="01082-142">如果用戶端已經提高許可權，使用提高許可權的標記將不會造成提高許可權的 UI 顯示。</span><span class="sxs-lookup"><span data-stu-id="01082-142">If the client is already elevated, using the elevation moniker will not cause the Elevation UI to display.</span></span>

## <a name="how-to-use-the-elevation-moniker"></a><span data-ttu-id="01082-143">如何使用提升許可權的標記</span><span class="sxs-lookup"><span data-stu-id="01082-143">How to Use the Elevation Moniker</span></span>

<span data-ttu-id="01082-144">提高許可權的標記是標準的 COM 標記，類似于會話、資料分割或佇列的名字。</span><span class="sxs-lookup"><span data-stu-id="01082-144">The elevation moniker is a standard COM moniker, similar to the session, partition, or queue monikers.</span></span> <span data-ttu-id="01082-145">它會將啟用要求導向具有指定提高許可權層級的指定伺服器。</span><span class="sxs-lookup"><span data-stu-id="01082-145">It directs an activation request to a specified server with the specified elevation level.</span></span> <span data-ttu-id="01082-146">要啟用的 CLSID 會出現在 [標記] 字串中。</span><span class="sxs-lookup"><span data-stu-id="01082-146">The CLSID to be activated appears in the moniker string.</span></span>

<span data-ttu-id="01082-147">提高許可權的標記支援下列執行層級權杖：</span><span class="sxs-lookup"><span data-stu-id="01082-147">The elevation moniker supports the following Run level tokens:</span></span>

1.  <span data-ttu-id="01082-148">系統管理員</span><span class="sxs-lookup"><span data-stu-id="01082-148">Administrator</span></span>
2.  <span data-ttu-id="01082-149">最高</span><span class="sxs-lookup"><span data-stu-id="01082-149">Highest</span></span>

<span data-ttu-id="01082-150">其語法如下所示：</span><span class="sxs-lookup"><span data-stu-id="01082-150">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

<span data-ttu-id="01082-151">上述語法使用 "new" 標記來傳回 *guid* 所指定之 COM 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="01082-151">The preceding syntax uses the "new" moniker to return an instance of the COM class specified by *guid*.</span></span> <span data-ttu-id="01082-152">請注意，"new" 標記會在內部使用 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 介面取得類別物件，然後在其上呼叫 [**IClassFactory：： CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) 。</span><span class="sxs-lookup"><span data-stu-id="01082-152">Note that the "new" moniker internally uses the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface to obtain a class object and then calls [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) on it.</span></span>

<span data-ttu-id="01082-153">提高許可權的標記也可以用來取得 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)的類別物件。</span><span class="sxs-lookup"><span data-stu-id="01082-153">The elevation moniker can also be used to get a class object, which implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="01082-154">呼叫端接著會呼叫 [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) 來取得物件實例。</span><span class="sxs-lookup"><span data-stu-id="01082-154">The caller then calls [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) to get an object instance.</span></span> <span data-ttu-id="01082-155">其語法如下所示：</span><span class="sxs-lookup"><span data-stu-id="01082-155">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a><span data-ttu-id="01082-156">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="01082-156">Sample code</span></span>

<span data-ttu-id="01082-157">下列程式碼範例示範如何使用提升許可權的標記。</span><span class="sxs-lookup"><span data-stu-id="01082-157">The following code example shows how to use the elevation moniker.</span></span> <span data-ttu-id="01082-158">它會假設您已經在目前的執行緒上初始化 COM。</span><span class="sxs-lookup"><span data-stu-id="01082-158">It assumes that you have already initialized COM on the current thread.</span></span>


```C++
HRESULT CoCreateInstanceAsAdmin(HWND hwnd, REFCLSID rclsid, REFIID riid, __out void ** ppv)
{
    BIND_OPTS3 bo;
    WCHAR  wszCLSID[50];
    WCHAR  wszMonikerName[300];

    StringFromGUID2(rclsid, wszCLSID, sizeof(wszCLSID)/sizeof(wszCLSID[0])); 
    HRESULT hr = StringCchPrintf(wszMonikerName, sizeof(wszMonikerName)/sizeof(wszMonikerName[0]), L"Elevation:Administrator!new:%s", wszCLSID);
    if (FAILED(hr))
        return hr;
    memset(&bo, 0, sizeof(bo));
    bo.cbStruct = sizeof(bo);
    bo.hwnd = hwnd;
    bo.dwClassContext  = CLSCTX_LOCAL_SERVER;
    return CoGetObject(wszMonikerName, &bo, riid, ppv);
}
```



<span data-ttu-id="01082-159">系結 [**\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1)是 Windows Vista 的新功能。</span><span class="sxs-lookup"><span data-stu-id="01082-159">[**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) is new in Windows Vista.</span></span> <span data-ttu-id="01082-160">它衍生自 [**BIND \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1)。</span><span class="sxs-lookup"><span data-stu-id="01082-160">It is derived from [**BIND\_OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).</span></span>

<span data-ttu-id="01082-161">唯一的加法是 **hwnd** 欄位 **hwnd**。</span><span class="sxs-lookup"><span data-stu-id="01082-161">The only addition is an **HWND** field, **hwnd**.</span></span> <span data-ttu-id="01082-162">這個控制碼代表的視窗會成為提高許可權 UI 的擁有者（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="01082-162">This handle represents a window that becomes the owner of the Elevation UI, if applicable.</span></span>

<span data-ttu-id="01082-163">如果 **hwnd** 為 **Null**，COM 將會呼叫 [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) 來尋找與目前線程相關聯的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="01082-163">If **hwnd** is **NULL**, COM will call [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) to find a window handle associated with the current thread.</span></span> <span data-ttu-id="01082-164">如果用戶端是無法填入系結 [**\_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) 結構的腳本，就可能會發生此情況。</span><span class="sxs-lookup"><span data-stu-id="01082-164">This case might occur if the client is a script, which cannot fill in a [**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) structure.</span></span> <span data-ttu-id="01082-165">在此情況下，COM 將會嘗試使用與腳本執行緒相關聯的視窗。</span><span class="sxs-lookup"><span data-stu-id="01082-165">In this case, COM will try to use the window associated with the script thread.</span></span>

## <a name="over-the-shoulder-ots-elevation"></a><span data-ttu-id="01082-166">過度 (OTS) 提高許可權</span><span class="sxs-lookup"><span data-stu-id="01082-166">Over-The-Shoulder (OTS) Elevation</span></span>

<span data-ttu-id="01082-167"> (的 OTS) 提高許可權是指用戶端以系統管理員的認證（而非自己的認證）執行 COM 伺服器的案例。</span><span class="sxs-lookup"><span data-stu-id="01082-167">Over-the-shoulder (OTS) elevation refers to the scenario in which a client runs a COM server with an administrator's credentials rather than his or her own.</span></span> <span data-ttu-id="01082-168"> (「超過肩」一詞表示系統管理員會在用戶端執行伺服器時，監看用戶端的肩。 ) </span><span class="sxs-lookup"><span data-stu-id="01082-168">(The term "over the shoulder" means that the administrator is watching over the client's shoulder as the client runs the server.)</span></span>

<span data-ttu-id="01082-169">這種情況可能會對伺服器造成 COM 呼叫的問題，因為伺服器可能不會明確 (地呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ，也就是以程式設計方式) 或隱含 (以宣告方式使用登錄) 。</span><span class="sxs-lookup"><span data-stu-id="01082-169">This scenario might cause a problem for COM calls into the server, because the server might not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) either explicitly (that is, programmatically) or implicitly (that is, declaratively, using the registry).</span></span> <span data-ttu-id="01082-170">針對這類伺服器，COM 會計算安全描述項，只允許自助、系統和內建系統 \\ 管理員對伺服器進行 COM 呼叫。</span><span class="sxs-lookup"><span data-stu-id="01082-170">For such servers, COM computes a security descriptor that allows only SELF, SYSTEM, and Builtin\\Administrators to makes COM calls into the server.</span></span> <span data-ttu-id="01082-171">在 OTS 案例中，這種相片順序將無法運作。</span><span class="sxs-lookup"><span data-stu-id="01082-171">This arrangement will not work in OTS scenarios.</span></span> <span data-ttu-id="01082-172">相反地，伺服器必須明確或隱含地呼叫 **CoInitializeSecurity**，並指定包含互動式群組 SID 和系統的 ACL。</span><span class="sxs-lookup"><span data-stu-id="01082-172">Instead, the server must call **CoInitializeSecurity**, either explicitly or implicitly, and specify an ACL that includes the INTERACTIVE group SID and SYSTEM.</span></span>

<span data-ttu-id="01082-173">下列程式碼範例示範如何使用互動式群組 SID (SD) 建立安全描述項。</span><span class="sxs-lookup"><span data-stu-id="01082-173">The following code example shows how to create a security descriptor (SD) with the INTERACTIVE group SID.</span></span>

``` syntax
BOOL GetAccessPermissionsForLUAServer(SECURITY_DESCRIPTOR **ppSD)
{
// Local call permissions to IU, SY
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0x3;;;IU)(A;;0x3;;;SY)";
    SECURITY_DESCRIPTOR *pSD;
    *ppSD = NULL;

    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }

    return FALSE;
}
```

<span data-ttu-id="01082-174">下列程式碼範例示範如何使用先前程式碼範例中的 SD 來隱含呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ：</span><span class="sxs-lookup"><span data-stu-id="01082-174">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implicitly with the SD from the previous code example:</span></span>


```C++
// hKey is the HKCR\AppID\{GUID} key
BOOL SetAccessPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "AccessPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
}
```



<span data-ttu-id="01082-175">下列程式碼範例示範如何使用上述 SD 明確呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ：</span><span class="sxs-lookup"><span data-stu-id="01082-175">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explicitly with the above SD:</span></span>


```C++
// Absolute SD values
PSECURITY_DESCRIPTOR pAbsSD = NULL;
DWORD AbsSdSize = 0;
PACL  pAbsAcl = NULL;
DWORD AbsAclSize = 0;
PACL  pAbsSacl = NULL;
DWORD AbsSaclSize = 0;
PSID  pAbsOwner = NULL;
DWORD AbsOwnerSize = 0;
PSID  pAbsGroup = NULL;
DWORD AbsGroupSize = 0;

MakeAbsoluteSD (
    pSD,
    pAbsSD,
    &AbsSdSize,
    pAbsAcl,
    &AbsAclSize,
    pAbsSacl,
    &AbsSaclSize,
    pAbsOwner,
    &AbsOwnerSize,
    pAbsGroup,
    &AbsGroupSize
);

if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
{
    pAbsSD = (PSECURITY_DESCRIPTOR)LocalAlloc(LMEM_FIXED, AbsSdSize);
    pAbsAcl = (PACL)LocalAlloc(LMEM_FIXED, AbsAclSize);
    pAbsSacl = (PACL)LocalAlloc(LMEM_FIXED, AbsSaclSize);
    pAbsOwner = (PSID)LocalAlloc(LMEM_FIXED, AbsOwnerSize);
    pAbsGroup = (PSID)LocalAlloc(LMEM_FIXED, AbsGroupSize);

    if ( ! (pAbsSD && pAbsAcl && pAbsSacl && pAbsOwner && pAbsGroup))
    {
        hr = E_OUTOFMEMORY;
        goto Cleanup;
    }
    if ( ! MakeAbsoluteSD(
        pSD,
        pAbsSD,
        &AbsSdSize,
        pAbsAcl,
        &AbsAclSize,
        pAbsSacl,
        &AbsSaclSize,
        pAbsOwner,
        &AbsOwnerSize,
        pAbsGroup,
        &AbsGroupSize
        ))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto Cleanup;
    }
}
else
{
    hr = HRESULT_FROM_WIN32(GetLastError());
    goto Cleanup;
}

// Call CoinitilizeSecurity.
```



## <a name="com-permissions-and-mandatory-access-labels"></a><span data-ttu-id="01082-176">COM 許可權和強制存取標籤</span><span class="sxs-lookup"><span data-stu-id="01082-176">COM Permissions and Mandatory Access Labels</span></span>

<span data-ttu-id="01082-177">Windows Vista 引進了安全描述項中 *強制存取標籤* 的概念。</span><span class="sxs-lookup"><span data-stu-id="01082-177">Windows Vista introduces the notion of *mandatory access labels* in security descriptors.</span></span> <span data-ttu-id="01082-178">標籤會指示用戶端是否可以取得 COM 物件的執行存取權。</span><span class="sxs-lookup"><span data-stu-id="01082-178">The label dictates whether clients can get execute access to a COM object.</span></span> <span data-ttu-id="01082-179">標籤會指定在系統存取控制清單中， (SACL) 部分的安全描述項中。</span><span class="sxs-lookup"><span data-stu-id="01082-179">The label is specified in the system access control list (SACL) portion of the security descriptor.</span></span> <span data-ttu-id="01082-180">在 Windows Vista 中，COM 支援「系統 \_ 強制 \_ 標籤 \_ 無執行」卷 \_ \_ 標。</span><span class="sxs-lookup"><span data-stu-id="01082-180">In Windows Vista, COM supports the SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP label.</span></span> <span data-ttu-id="01082-181">在 Windows Vista 之前的作業系統上，系統會忽略 COM 許可權中的 Sacl。</span><span class="sxs-lookup"><span data-stu-id="01082-181">SACLs in the COM permissions are ignored on operating systems prior to Windows Vista.</span></span>

<span data-ttu-id="01082-182">在 Windows Vista 中，dcomcnfg.exe 不支援將 (IL) 的完整性層級變更為 COM 許可權。</span><span class="sxs-lookup"><span data-stu-id="01082-182">As of Windows Vista, dcomcnfg.exe does not support changing the integrity level (IL) in COM permissions.</span></span> <span data-ttu-id="01082-183">它必須以程式設計的方式設定。</span><span class="sxs-lookup"><span data-stu-id="01082-183">It must be set programmatically.</span></span>

<span data-ttu-id="01082-184">下列程式碼範例示範如何建立具有標籤的 COM 安全描述項，以允許來自所有低 IL 用戶端的啟動/啟用要求。</span><span class="sxs-lookup"><span data-stu-id="01082-184">The following code example shows how to create a COM security descriptor with a label that allows launch/activation requests from all LOW IL clients.</span></span> <span data-ttu-id="01082-185">請注意，標籤對於啟動/啟用和呼叫許可權都有效。</span><span class="sxs-lookup"><span data-stu-id="01082-185">Note that the labels are valid for Launch/Activation and Call permissions.</span></span> <span data-ttu-id="01082-186">因此，您可以撰寫不允許啟動、啟用或從具有特定 IL 之用戶端呼叫的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="01082-186">Thus, it is possible to write a COM server that disallows launch, activation or calls from clients with a certain IL.</span></span> <span data-ttu-id="01082-187">For more information about integrity levels, see the section "Understanding Windows Vista's Integrity Mechanism" in [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="01082-187">For more information about integrity levels, see the section "Understanding Windows Vista's Integrity Mechanism" in [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).</span></span>


```C++
BOOL GetLaunchActPermissionsWithIL (SECURITY_DESCRIPTOR **ppSD)
{
// Allow World Local Launch/Activation permissions. Label the SD for LOW IL Execute UP
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0xb;;;WD)S:(ML;;NX;;;LW)";
    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }
}

BOOL SetLaunchActPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "LaunchPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
};
```



## <a name="cocreateinstance-and-integrity-levels"></a><span data-ttu-id="01082-188">CoCreateInstance 和完整性層級</span><span class="sxs-lookup"><span data-stu-id="01082-188">CoCreateInstance and Integrity Levels</span></span>

<span data-ttu-id="01082-189">在 Windows Vista 中， [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 的行為已變更，以防止較低的 IL 用戶端預設系結至 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="01082-189">The behavior of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) has changed in Windows Vista, to prevent Low IL clients from binding to COM servers by default.</span></span> <span data-ttu-id="01082-190">伺服器必須藉由指定 SACL 來明確地允許這類系結。</span><span class="sxs-lookup"><span data-stu-id="01082-190">The server must explicitly allow such bindings by specifying the SACL.</span></span> <span data-ttu-id="01082-191">**CoCreateInstance** 的變更如下：</span><span class="sxs-lookup"><span data-stu-id="01082-191">The changes to **CoCreateInstance** are as follows:</span></span>

1.  <span data-ttu-id="01082-192">啟動 COM 伺服器進程時，伺服器進程 token 中的 IL 會設定為用戶端或伺服器權杖 IL，以較低者為准。</span><span class="sxs-lookup"><span data-stu-id="01082-192">When launching a COM server process, the IL in the server process token is set to the client or server token IL, whichever is lower.</span></span>
2.  <span data-ttu-id="01082-193">根據預設，COM 會防止低 IL 用戶端系結至任何 COM 伺服器的執行中實例。</span><span class="sxs-lookup"><span data-stu-id="01082-193">By default, COM will prevent Low IL clients from binding to running instances of any COM servers.</span></span> <span data-ttu-id="01082-194">若要允許系結，COM 伺服器的啟動/啟用安全描述項必須包含指定低 IL 標籤的 SACL (請參閱上一節中的範例程式碼，以建立這類安全描述項) 。</span><span class="sxs-lookup"><span data-stu-id="01082-194">To allow the bind, a COM server's Launch/Activation security descriptor must contain a SACL that specifies the Low IL label (see the previous section for the sample code to create such a security descriptor).</span></span>

## <a name="elevated-servers-and-rot-registrations"></a><span data-ttu-id="01082-195">提高許可權的伺服器和 ROT 註冊</span><span class="sxs-lookup"><span data-stu-id="01082-195">Elevated Servers and ROT Registrations</span></span>

<span data-ttu-id="01082-196">如果 COM 伺服器希望在執行中的物件資料表中註冊 (的 ROT) 並允許任何用戶端存取註冊，則必須使用 ROTFLAGS \_ ALLOWANYCLIENT 旗標。</span><span class="sxs-lookup"><span data-stu-id="01082-196">If a COM server wishes to register in the running object table (ROT) and allow any client to access the registration, it must use the ROTFLAGS\_ALLOWANYCLIENT flag.</span></span> <span data-ttu-id="01082-197">"Activate As Activator" COM 伺服器無法指定 ROTFLAGS \_ ALLOWANYCLIENT，因為 DCOM 服務控制管理員 (DCOMSCM) 強制對此旗標進行詐騙檢查。</span><span class="sxs-lookup"><span data-stu-id="01082-197">An "Activate As Activator" COM server cannot specify ROTFLAGS\_ALLOWANYCLIENT because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="01082-198">因此，在 Windows Vista 中，COM 加入了新的登錄專案的支援，讓伺服器能夠規定將它的 ROT 註冊提供給任何用戶端使用：</span><span class="sxs-lookup"><span data-stu-id="01082-198">Therefore, in Windows Vista, COM adds support for a new registry entry that allows the server to stipulate that its ROT registrations be made available to any client:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

<span data-ttu-id="01082-199">此登錄 DWORD 專案唯一有效的值 \_ 為：</span><span class="sxs-lookup"><span data-stu-id="01082-199">The only valid value for this REG\_DWORD entry is:</span></span>

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

<span data-ttu-id="01082-200">專案必須存在於 **HKEY \_ 本機 \_ 電腦** hive 中。</span><span class="sxs-lookup"><span data-stu-id="01082-200">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span>

<span data-ttu-id="01082-201">此專案提供「啟用為啟動程式」伺服器，其功能與 ROTFLAGS \_ ALLOWANYCLIENT 為 RunAs 伺服器提供的功能相同。</span><span class="sxs-lookup"><span data-stu-id="01082-201">This entry provides an "Activate As Activator" server with the same functionality that ROTFLAGS\_ALLOWANYCLIENT provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01082-202">相關主題</span><span class="sxs-lookup"><span data-stu-id="01082-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01082-203">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="01082-203">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="01082-204">了解「受保護模式」Internet Explorer 並在此模式下工作</span><span class="sxs-lookup"><span data-stu-id="01082-204">Understanding and Working in Protected Mode Internet Explorer</span></span>](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 