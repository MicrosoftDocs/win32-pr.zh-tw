---
title: EAP 方法的常見問題
description: 提供關於 EAP 方法撰寫的常見程式設計問題的解答。
ms.assetid: 244e048f-4cc0-4094-a2b9-0f84674a293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2194f5fe68dc660e40331be1b790b73386
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106968121"
---
# <a name="eap-method-frequently-asked-questions"></a><span data-ttu-id="e571f-103">EAP 方法的常見問題</span><span class="sxs-lookup"><span data-stu-id="e571f-103">EAP Method Frequently Asked Questions</span></span>

<span data-ttu-id="e571f-104">本主題提供關於 EAP 方法撰寫的常見程式設計問題的解答。</span><span class="sxs-lookup"><span data-stu-id="e571f-104">This topic provides answers to commonly-asked programming questions about EAP method authoring.</span></span>

## <a name="eap-method-frequently-asked-questions"></a><span data-ttu-id="e571f-105">EAP 方法的常見問題</span><span class="sxs-lookup"><span data-stu-id="e571f-105">EAP Method Frequently Asked Questions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e571f-106">問題</span><span class="sxs-lookup"><span data-stu-id="e571f-106">Question</span></span></th>
<th><span data-ttu-id="e571f-107">Answer</span><span class="sxs-lookup"><span data-stu-id="e571f-107">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e571f-108">什麼是設定 &quot; 資料 &quot; ？</span><span class="sxs-lookup"><span data-stu-id="e571f-108">What is &quot;configuration data&quot;?</span></span></td>
<td><span data-ttu-id="e571f-109">設定 &quot; 資料 &quot; 和 &quot; 連接資料的詞彙 &quot; 為同義。</span><span class="sxs-lookup"><span data-stu-id="e571f-109">The terms &quot;configuration data&quot; and &quot;connection data&quot; are synonymous.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e571f-110">什麼是 &quot; 連接資料 &quot; ？</span><span class="sxs-lookup"><span data-stu-id="e571f-110">What is &quot;connection data&quot;?</span></span></td>
<td><span data-ttu-id="e571f-111">&quot;連接資料 &quot; 是 EAP 方法特定的不透明 BLOB，其中包含方法的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="e571f-111">&quot;Connection data&quot; is an EAP method-specific opaque BLOB that contains configuration information for the method.</span></span> <span data-ttu-id="e571f-112">此連接資料是在一開始設定時由方法所建立，且絕對不會由任何其他元件（而非 EAP 方法本身）進行解讀或修改。</span><span class="sxs-lookup"><span data-stu-id="e571f-112">This connection data is created by the method when it is initially configured and is never interpreted or modified by any other component than the EAP method itself.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e571f-113">什麼是 &quot; 認證 &quot; ？</span><span class="sxs-lookup"><span data-stu-id="e571f-113">What are &quot;credentials&quot;?</span></span></td>
<td><span data-ttu-id="e571f-114">&quot;認證 &quot; 和 &quot; 使用者資料的意義 &quot; 是同義。</span><span class="sxs-lookup"><span data-stu-id="e571f-114">The terms &quot;credentials&quot; and &quot;user data&quot; are synonymous.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e571f-115">什麼是 &quot; 使用者資料 &quot; ？</span><span class="sxs-lookup"><span data-stu-id="e571f-115">What is &quot;user data&quot;?</span></span></td>
<td><span data-ttu-id="e571f-116">&quot;使用者資料 &quot; 是 EAP 方法特定的不透明 BLOB，其中包含使用者認證資料，例如使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="e571f-116">&quot;User data&quot; is an EAP method-specific opaque BLOB that contains user credential data, such as a user name and password.</span></span> <span data-ttu-id="e571f-117">使用者資料絕對不會由任何其他元件解讀或修改，而非 EAP 方法本身。</span><span class="sxs-lookup"><span data-stu-id="e571f-117">The user data is never interpreted or modified by any other component than the EAP method itself.</span></span> <span data-ttu-id="e571f-118">&quot;使用者資料 &quot; 和認證的 &quot; 詞彙 &quot; 是同義的。</span><span class="sxs-lookup"><span data-stu-id="e571f-118">The terms &quot;user data&quot; and &quot;credentials&quot; are synonymous.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e571f-119">什麼是 &quot; EAP 屬性 &quot; ？</span><span class="sxs-lookup"><span data-stu-id="e571f-119">What is an &quot;EAP attribute&quot;?</span></span></td>
<td><span data-ttu-id="e571f-120">&quot;EAP 屬性 &quot; 是一種資料結構，其中包含預先決定的資料類型。</span><span class="sxs-lookup"><span data-stu-id="e571f-120">An &quot;EAP attribute&quot; is a data structure that contains a predetermined type of data.</span></span> <span data-ttu-id="e571f-121">屬性是用來在 EAP 方法和要求者之間，或在 EAP 方法和驗證器之間傳達資訊。</span><span class="sxs-lookup"><span data-stu-id="e571f-121">Attributes are used to communicate information between EAP methods and supplicants, or between EAP methods and authenticators.</span></span> <span data-ttu-id="e571f-122">EAP 方法的對等和驗證器執行可能會透過網路交換這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e571f-122">Peer and authenticator implementations of an EAP method may exchange these attributes over a network.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e571f-123">設定 API 和執行時間 API 是否會出現在相同的方法 DLL 中？</span><span class="sxs-lookup"><span data-stu-id="e571f-123">Can the configuration API and the run-time API appear in the same method DLL?</span></span></td>
<td><span data-ttu-id="e571f-124">是。</span><span class="sxs-lookup"><span data-stu-id="e571f-124">Yes.</span></span> <span data-ttu-id="e571f-125">設定 EAP 方法本身的登錄專案時，請務必指定差異。</span><span class="sxs-lookup"><span data-stu-id="e571f-125">Be sure to specify the distinction when configuring the registry entries for the EAP method itself.</span></span> <span data-ttu-id="e571f-126">設定路徑和對等路徑必須相同。</span><span class="sxs-lookup"><span data-stu-id="e571f-126">The configuration path and peer path must be the same.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e571f-127">設定 API 和執行時間 API 是否會顯示在不同的方法 Dll 中？</span><span class="sxs-lookup"><span data-stu-id="e571f-127">Can the configuration API and the run-time API appear in separate method DLLs?</span></span></td>
<td><span data-ttu-id="e571f-128">是。</span><span class="sxs-lookup"><span data-stu-id="e571f-128">Yes.</span></span> <span data-ttu-id="e571f-129">設定 EAP 方法本身的登錄專案時，請務必指定差異。</span><span class="sxs-lookup"><span data-stu-id="e571f-129">Be sure to specify the distinction when configuring the registry entries for the EAP method itself.</span></span> <span data-ttu-id="e571f-130">設定和對等路徑必須指向正確的 Dll。</span><span class="sxs-lookup"><span data-stu-id="e571f-130">The configuration and peer paths must point to the correct DLLs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e571f-131">如何? 安裝 EAP 方法？</span><span class="sxs-lookup"><span data-stu-id="e571f-131">How do I install an EAP method?</span></span></td>
<td><span data-ttu-id="e571f-132">若要安裝 EAP 方法，您必須先在 EAP 方法 DLL 本身中，執行 [<strong>DllRegisterServer</strong>] (/windows/win32/api/olectl/nf-olectl-dllregisterserver) 和 [<strong>DllUnregisterServer</strong>] (/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 。</span><span class="sxs-lookup"><span data-stu-id="e571f-132">To install an EAP method, you must first implement [<strong>DllRegisterServer</strong>](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [<strong>DllUnregisterServer</strong>](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) in the EAP method DLL itself.</span></span> <span data-ttu-id="e571f-133">之後，請使用 <strong>regsvr32.exe</strong> 來安裝和卸載方法。</span><span class="sxs-lookup"><span data-stu-id="e571f-133">After that, use <strong>regsvr32.exe</strong> to install and uninstall the method.</span></span> <span data-ttu-id="e571f-134">您也必須設定適當的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="e571f-134">The appropriate registry keys must also be set.</span></span> <span data-ttu-id="e571f-135">如需詳細資訊，請參閱 [安裝 EAP 方法](installing-an-eap-method.md)。</span><span class="sxs-lookup"><span data-stu-id="e571f-135">For more information, see [Installing an EAP Method](installing-an-eap-method.md).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e571f-136">什麼是頻內 [網路存取保護](/windows/desktop/NAP/network-access-protection-start-page) (NAP) 支援？</span><span class="sxs-lookup"><span data-stu-id="e571f-136">What is in-band [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) support?</span></span></td>
<td><span data-ttu-id="e571f-137">啟用頻內 NAP 支援時，會在 EAP 方法封包內傳輸 NAP 封包。</span><span class="sxs-lookup"><span data-stu-id="e571f-137">When in-band NAP support is enabled, NAP packets are transported inside EAP method packets.</span></span> <span data-ttu-id="e571f-138">相反地，當啟用頻外 NAP 支援時，健康情況的 NAP [聲明](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) exchange 會透過 eap 方法封包內部以外的方式進行，而 nap 產生的憑證則用於 eap 方法驗證。</span><span class="sxs-lookup"><span data-stu-id="e571f-138">In contrast, when out-of-band NAP support is enabled, the NAP [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) exchange occurs through means other than internal to EAP method packets, and NAP-generated certificates are used in EAP method authentication.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e571f-139">我可以為我的 EAP 方法啟用頻內 NAP 支援嗎？</span><span class="sxs-lookup"><span data-stu-id="e571f-139">Can I enable in-band NAP support for my EAP method?</span></span></td>
<td><span data-ttu-id="e571f-140">是的，您可以啟用 EAP 方法的頻內 NAP 支援。</span><span class="sxs-lookup"><span data-stu-id="e571f-140">Yes, in-band NAP support for your EAP method can be enabled.</span></span> <span data-ttu-id="e571f-141">如需詳細資訊，請參閱 [啟用 EAP 方法的 In-Band NAP 支援](enabling-in-band-nap-support.md)。</span><span class="sxs-lookup"><span data-stu-id="e571f-141">For more information, see [Enabling In-Band NAP Support for EAP Methods](enabling-in-band-nap-support.md).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e571f-142">EAP 如何透過安全通道進行彈性驗證 (EAP-FAST) 運作？</span><span class="sxs-lookup"><span data-stu-id="e571f-142">How does EAP Flexible Authentication via Secure Tunneling (EAP-FAST) work?</span></span></td>
<td><span data-ttu-id="e571f-143">EAP 快速案例的運作方式如下。</span><span class="sxs-lookup"><span data-stu-id="e571f-143">The EAP-FAST scenario works as follows.</span></span> <br/>
<ul>
<li><span data-ttu-id="e571f-144">方法會在採用方法 UI 的單一登入 (SSO) 處理密碼變更。</span><span class="sxs-lookup"><span data-stu-id="e571f-144">The method processes a password change at single-sign-on (SSO) employing the method UI.</span></span></li>
<li><span data-ttu-id="e571f-145">方法會傳回 [<strong>eatCredentialsChanged</strong>] (/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type) 屬性。</span><span class="sxs-lookup"><span data-stu-id="e571f-145">The method returns the [<strong>eatCredentialsChanged</strong>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type) attribute.</span></span></li>
<li><span data-ttu-id="e571f-146">要求者向使用者指出認證已變更，並要求使用者重新輸入認證。</span><span class="sxs-lookup"><span data-stu-id="e571f-146">The supplicant indicates to the user that credentials have changed and requests the user to re-enter their credentials.</span></span></li>
<li><span data-ttu-id="e571f-147">要求者重新輸入使用者認證，然後將這些認證傳送給方法。</span><span class="sxs-lookup"><span data-stu-id="e571f-147">The supplicant re-enters the user credentials, and sends those credentials to the method.</span></span></li>
</ul>
<span data-ttu-id="e571f-148">如需有關 EAP-FAST 的詳細資訊，請參閱透過 [安全通道的 Eap 彈性驗證](https://go.microsoft.com/fwlink/p/?linkid=84010) (eap-fast) 。</span><span class="sxs-lookup"><span data-stu-id="e571f-148">For more information on EAP-FAST, see [EAP Flexible Authentication via Secure Tunneling](https://go.microsoft.com/fwlink/p/?linkid=84010) (EAP-FAST).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e571f-149">什麼是預先共用金鑰 (PSK) ？</span><span class="sxs-lookup"><span data-stu-id="e571f-149">What is Pre-Shared Key(PSK)?</span></span></td>
<td><span data-ttu-id="e571f-150">傳送和接收數位信號的方法，在此方法中，傳輸信號的階段會因傳達資訊而有所不同。</span><span class="sxs-lookup"><span data-stu-id="e571f-150">A method of transmitting and receiving digital signals in which the phase of a transmitted signal is varied to convey information.</span></span> <span data-ttu-id="e571f-151">[<strong>EAPConfigInputPSK</strong>] (/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) 輸入欄位包含使用者的 EAP 快速 PSK。</span><span class="sxs-lookup"><span data-stu-id="e571f-151">The [<strong>EAPConfigInputPSK</strong>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) input field contains the user's EAP-FAST PSK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e571f-152">什麼是 WOW，以及它對 EAPHost 有何影響？</span><span class="sxs-lookup"><span data-stu-id="e571f-152">What is WOW and how does it matter to EAPHost?</span></span></td>
<td><span data-ttu-id="e571f-153">Microsoft Windows-32-位在 Windows-64 位 (WOW) 是支援32位 x86 平臺應用程式之64位 Windows 中的作業系統元件。</span><span class="sxs-lookup"><span data-stu-id="e571f-153">Microsoft Windows-32-bit-On-Windows-64-bit (WOW) is an operating system component in 64-bit Windows that supports 32-bit x86 platform application.</span></span> <span data-ttu-id="e571f-154">通常，EAP 方法作者會定義某種形式的 C/c + + 結構，以封裝設定資料、認證資料和互動式 UI 資料。</span><span class="sxs-lookup"><span data-stu-id="e571f-154">Typically, a EAP method author would define some form of C/C++ structure to encapsulate configuration data, credential data, and interactive UI data.</span></span> <span data-ttu-id="e571f-155">為了避免在 WOW 和其他案例中發生不相容的情況，請務必確保資料結構在不同處理器架構中的對齊方式， (32 位和64位處理器) 。</span><span class="sxs-lookup"><span data-stu-id="e571f-155">To avoid incompatibilities in WOW and other scenarios, it is important to ensure that data structures are aligned similarly in different processor architectures (32-bit and 64-bit processors).</span></span> <span data-ttu-id="e571f-156">通常會使用虛擬填補來對齊欄位，讓32和64位處理器上的設定、認證和互動式 UI 資料都相同。</span><span class="sxs-lookup"><span data-stu-id="e571f-156">Typically dummy padding is used to align the fields so that the configuration, credential and interactive UI data are identical on both 32-and 64-bit processors.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e571f-157">什麼是 &quot; 動作碼 &quot; ？這些動作碼會傳回哪些條件？</span><span class="sxs-lookup"><span data-stu-id="e571f-157">What are &quot;action codes&quot; and under what conditions are these action codes returned?</span></span></td>
<td><span data-ttu-id="e571f-158">&quot;動作程式碼 &quot; 允許方法控制驗證流程，而且是狀態機器的整數。</span><span class="sxs-lookup"><span data-stu-id="e571f-158">&quot;Action codes&quot; allow methods to control the flow of authentication, and are integral to the state machine.</span></span> <span data-ttu-id="e571f-159">它們是 EAP 方法所傳回的值，表示 EAPHost 應採取的下一個動作。</span><span class="sxs-lookup"><span data-stu-id="e571f-159">They are values returned by an EAP method to indicate the next action the EAPHost should take.</span></span> <span data-ttu-id="e571f-160">例如，動作程式碼可能表示 EAPHost EAP 方法有封包可以進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="e571f-160">For example, an action code could indicate to EAPHost that the EAP method has a packet ready for transmission.</span></span> <span data-ttu-id="e571f-161">由 EAP 方法所傳回的所有動作程式碼所遵守的要求者，但永遠不會發出動作碼。如需詳細資訊，請參閱 [EAP 對等要求者動作代碼](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)。</span><span class="sxs-lookup"><span data-stu-id="e571f-161">The supplicant abides by all action codes returned by an EAP method, but never issues action codes.For more information, see [EAP Peer Supplicant Action Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e571f-162">方法何時會傳回 [<strong>EapPeerMethodResponseActionDiscard</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，而此動作程式碼代表 EAPHost 的意義為何？</span><span class="sxs-lookup"><span data-stu-id="e571f-162">When does a method return [<strong>EapPeerMethodResponseActionDiscard</strong>](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction), and what does this action code mean to EAPHost?</span></span></td>
<td><span data-ttu-id="e571f-163">[<strong>EapPeerMethodResponseActionDiscard</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) 由 EAP 方法傳回，表示 EAPHost 必須捨棄提供給方法的封包。</span><span class="sxs-lookup"><span data-stu-id="e571f-163">[<strong>EapPeerMethodResponseActionDiscard</strong>](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) is returned by an EAP method to indicate to the EAPHost that it must discard the packet it supplied to the method.</span></span> <span data-ttu-id="e571f-164">具體而言，方法已判定封包無效。</span><span class="sxs-lookup"><span data-stu-id="e571f-164">Specifically, the method has determined that the packet is invalid.</span></span> <span data-ttu-id="e571f-165">EAPHost 接著會等待下一個套件。</span><span class="sxs-lookup"><span data-stu-id="e571f-165">EAPHost then waits for the next package.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e571f-166">方法何時會傳回 [<strong>EapPeerMethodResponseActionSend</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，而此動作程式碼代表 EAPHost 的意義為何？</span><span class="sxs-lookup"><span data-stu-id="e571f-166">When does a method return [<strong>EapPeerMethodResponseActionSend</strong>](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) and what does this action code mean to EAPHost?</span></span></td>
<td><span data-ttu-id="e571f-167">[<strong>EapPeerMethodResponseActionSend</strong>] EAP 方法會傳回 [] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，表示 EAPHost EAPHost 所接收的下一個封包必須傳送至網路存取伺服器 (NAS) 。</span><span class="sxs-lookup"><span data-stu-id="e571f-167">[<strong>EapPeerMethodResponseActionSend</strong>](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) is returned by an EAP method to indicate to EAPHost that the next packet received by EAPHost must be sent to the network access server (NAS).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e571f-168">方法何時會傳回 [<strong>EapPeerMethodResponseActionResult</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，而此動作程式碼代表 EAPHost 的意義為何？</span><span class="sxs-lookup"><span data-stu-id="e571f-168">When does a method return [<strong>EapPeerMethodResponseActionResult</strong>](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) and what does this action code mean to EAPHost?</span></span></td>
<td><span data-ttu-id="e571f-169">[<strong>EapPeerMethodResponseActionResult</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) 由 EAP 方法傳回，以向 EAPHost 指出驗證會話已結束，且該會話的結果可供使用。</span><span class="sxs-lookup"><span data-stu-id="e571f-169">[<strong>EapPeerMethodResponseActionResult</strong>](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) is returned by an EAP method to indicate to the EAPHost that the authentication session has concluded and that the results of that session are available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e571f-170">方法何時會傳回 [<strong>EapPeerMethodResponseActionInvokeUI</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，而此動作程式碼代表 EAPHost 的意義為何？</span><span class="sxs-lookup"><span data-stu-id="e571f-170">When does a method return [<strong>EapPeerMethodResponseActionInvokeUI</strong>](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) and what does this action code mean to EAPHost?</span></span></td>
<td><span data-ttu-id="e571f-171">[<strong>EapPeerMethodResponseActionInvokeUI</strong>] EAP 方法會傳回 [] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，表示 EAPHost 需要使用者輸入才能繼續進行驗證，而且必須顯示使用者介面對話方塊才能取得該輸入。</span><span class="sxs-lookup"><span data-stu-id="e571f-171">[<strong>EapPeerMethodResponseActionInvokeUI</strong>](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) is returned by an EAP method to indicate to EAPHost that user input is required to continue with authentication, and that a user interface dialog box must be displayed to obtain that input.</span></span> <span data-ttu-id="e571f-172">一旦取得使用者輸入資料之後，EAPHost 就可以使用更新的 UI 內容資料，再次呼叫 EAP 方法。</span><span class="sxs-lookup"><span data-stu-id="e571f-172">Once the user input data has been obtained, EAPHost can call the EAP method again with the updated UI context data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e571f-173">方法何時會傳回 [<strong>EapPeerMethodResponseActionRespond</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，而此動作程式碼代表 EAPHost 的意義為何？</span><span class="sxs-lookup"><span data-stu-id="e571f-173">When does a method return [<strong>EapPeerMethodResponseActionRespond</strong>](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) and what does this action code mean to EAPHost?</span></span></td>
<td><span data-ttu-id="e571f-174">[<strong>EapPeerMethodResponseActionRespond</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) 由 eap 方法傳回，表示 EAPHost eap 方法具有可供 EAPHost 在驗證期間使用的屬性。</span><span class="sxs-lookup"><span data-stu-id="e571f-174">[<strong>EapPeerMethodResponseActionRespond</strong>](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) is returned by an EAP method to indicate to EAPHost that the EAP method has attributes available for EAPHost to use during authentication.</span></span> <span data-ttu-id="e571f-175">EAPHost 藉由呼叫 [<strong>EapPeerGetResponseAttributes</strong>] (/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) 方法取得屬性，然後再呼叫 [<strong>EapPeerSetResponseAttributes</strong>] (/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) 方法。</span><span class="sxs-lookup"><span data-stu-id="e571f-175">EAPHost obtains the attributes by calling the [<strong>EapPeerGetResponseAttributes</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) method followed by a call to the [<strong>EapPeerSetResponseAttributes</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) method.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e571f-176">方法何時會傳回 [<strong>EapPeerMethodResponseActionNone</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，而此動作程式碼代表 EAPHost 的意義為何？</span><span class="sxs-lookup"><span data-stu-id="e571f-176">When does a method return [<strong>EapPeerMethodResponseActionNone</strong>](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) and what does this action code mean to EAPHost?</span></span></td>
<td><span data-ttu-id="e571f-177">[<strong>EapPeerMethodResponseActionNone</strong>] EAP 方法會傳回 [] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，表示 EAPHost 目前不需要採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="e571f-177">[<strong>EapPeerMethodResponseActionNone</strong>](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) is returned by an EAP method to indicate to EAPHost that no action is required at this time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e571f-178">是否可以在驗證器端啟用追蹤？</span><span class="sxs-lookup"><span data-stu-id="e571f-178">Can I enable tracing on the authenticator side?</span></span></td>
<td><span data-ttu-id="e571f-179">是。</span><span class="sxs-lookup"><span data-stu-id="e571f-179">Yes.</span></span> <span data-ttu-id="e571f-180">如需詳細資訊，請參閱 [啟用追蹤](enabling-tracing.md)。</span><span class="sxs-lookup"><span data-stu-id="e571f-180">For more information, see [Enabling Tracing](enabling-tracing.md).</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e571f-181">相關主題</span><span class="sxs-lookup"><span data-stu-id="e571f-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e571f-182">EAPHost 對等方法 API 參考</span><span class="sxs-lookup"><span data-stu-id="e571f-182">EAPHost Peer Method API Reference</span></span>](eap-host-peer-method-api-reference.md)
</dt> <dt>

[<span data-ttu-id="e571f-183">EAPHost 一般常見問題</span><span class="sxs-lookup"><span data-stu-id="e571f-183">EAPHost General FAQs</span></span>](general-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="e571f-184">EAPHost 要求者常見問題</span><span class="sxs-lookup"><span data-stu-id="e571f-184">EAPHost Supplicant FAQs</span></span>](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="e571f-185">EAPHost 開發常見問題</span><span class="sxs-lookup"><span data-stu-id="e571f-185">EAPHost Development FAQs</span></span>](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

 

