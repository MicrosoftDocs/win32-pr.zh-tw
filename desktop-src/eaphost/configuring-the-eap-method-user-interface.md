---
title: 設定 EAP 方法消費者介面
description: 說明如何將 EAP 方法設定提供給 EAPHost，以設定要求者。
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b82debadc075b1fcc12dad06484c0fd3617874
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106965214"
---
# <a name="configuring-the-eap-method-user-interface"></a><span data-ttu-id="3fff1-103">設定 EAP 方法消費者介面</span><span class="sxs-lookup"><span data-stu-id="3fff1-103">Configuring the EAP Method User Interface</span></span>

<span data-ttu-id="3fff1-104">本主題說明如何將 EAP 方法設定提供給 EAPHost，以設定要求者。</span><span class="sxs-lookup"><span data-stu-id="3fff1-104">This topic explains how to configure the supplicant by supplying an EAP method configuration to EAPHost.</span></span>

<span data-ttu-id="3fff1-105">若要讓要求者使用 EAPHost 執行 EAP 型驗證，要求者必須透過 [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 函式將 eap 方法設定提供給 EAPHost。</span><span class="sxs-lookup"><span data-stu-id="3fff1-105">For a supplicant to perform an EAP-based authentication using EAPHost, a supplicant must supply an EAP method configuration to EAPHost through the [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) function.</span></span>

1.  <span data-ttu-id="3fff1-106">為了取得 EAP 方法設定，要求者通常會使用 [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) 查詢 EAPHost，以瞭解在本機電腦上可用且已安裝的一組完整 EAP 方法。</span><span class="sxs-lookup"><span data-stu-id="3fff1-106">To obtain the EAP method configuration, a supplicant typically queries EAPHost using [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) to learn the complete set of EAP methods that are available and installed on the local machine.</span></span> <span data-ttu-id="3fff1-107">方法清單通常會在下拉式列示方塊或其他 UI 控制項中呈現給使用者，讓使用者選取他們想要的方法。</span><span class="sxs-lookup"><span data-stu-id="3fff1-107">The list of methods is typically presented to the user in a combination box or other UI control that allows the user to select the method they want.</span></span>
    > [!Note]  
    > <span data-ttu-id="3fff1-108">要求者可以根據 **EAP \_ 方法 \_ 資訊 eapProperties** 中指出的方法屬性位，選擇篩選顯示的方法清單。</span><span class="sxs-lookup"><span data-stu-id="3fff1-108">The supplicant may choose to filter the displayed list of methods based on the method property bits indicated in **EAP\_METHOD\_INFO.eapProperties**.</span></span> <span data-ttu-id="3fff1-109">例如，某些方法可能不適合要求者所提供之傳輸的安全性特性。</span><span class="sxs-lookup"><span data-stu-id="3fff1-109">Some methods may not be appropriate for the security characteristics of the transport provided by the supplicant, for example.</span></span>

     

2.  <span data-ttu-id="3fff1-110">當 UI 控制項填入一組可能的 EAP 方法之後，使用者會選取想要設定的方法。</span><span class="sxs-lookup"><span data-stu-id="3fff1-110">Once the UI control is populated with the set of possible EAP methods, the user selects the method they want to configure.</span></span> <span data-ttu-id="3fff1-111">通常，要求者會提供 [設定 **] 或 [** **屬性** ] 按鈕，讓使用者存取所選 EAP 方法的設定屬性。</span><span class="sxs-lookup"><span data-stu-id="3fff1-111">Typically, the supplicant provides a **Configuration** or **Properties** button for the user to access configuration properties of the selected EAP method.</span></span>
    > [!Note]
    > <span data-ttu-id="3fff1-112">要求者知道有使用者可設定的屬性是以 **EAP \_ 方法 \_ 資訊 eapProperties** 中啟用的 **eapPropSupportsConfig** 位為基礎。</span><span class="sxs-lookup"><span data-stu-id="3fff1-112">The supplicant is aware that there are user-configurable properties based on the **eapPropSupportsConfig** bit being enabled in **EAP\_METHOD\_INFO.eapProperties**.</span></span>
    >
    > <span data-ttu-id="3fff1-113">如需詳細資訊，請參閱 [**EAP 方法屬性**](eap-method-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="3fff1-113">For more information, see [**EAP Method Properties**](eap-method-properties.md).</span></span>

     

3.  <span data-ttu-id="3fff1-114">當使用者按一下適當的 UI 控制項時，要求者會呼叫 [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui)，並將要求者本身 UI 的 **HWND** 值、從查詢取得的 [**eap \_ 方法 \_ 類型**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) 結構，以及其他必要的參數 [**傳遞至函式 \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) 。</span><span class="sxs-lookup"><span data-stu-id="3fff1-114">When the user clicks the appropriate UI control, the supplicant calls [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), passing into the function the **HWND** value for the supplicant's own UI, the [**EAP\_METHOD\_TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) structure obtained from the query to [**EAP\_METHOD\_INFO**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) structure and other required parameters.</span></span>
4.  <span data-ttu-id="3fff1-115">呼叫 [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) 會叫用 EAP 方法本身的設定 UI。</span><span class="sxs-lookup"><span data-stu-id="3fff1-115">Calling [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) invokes an EAP method's own configuration UI.</span></span> <span data-ttu-id="3fff1-116">從 **EapHostPeerInvokeConfigUI** 傳回時，函式會傳回 EAP 方法設定 BLOB 做為 out 參數。</span><span class="sxs-lookup"><span data-stu-id="3fff1-116">On return from **EapHostPeerInvokeConfigUI**, the function will return an EAP method configuration BLOB as an out-parameter.</span></span>
5.  <span data-ttu-id="3fff1-117">要求者會儲存設定 BLOB，以及搭配 [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)使用的 [**EAP \_ 方法 \_ 類型**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type)結構。</span><span class="sxs-lookup"><span data-stu-id="3fff1-117">The supplicant stores the configuration BLOB, along with the [**EAP\_METHOD\_TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) structure for use with [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span></span>
6.  <span data-ttu-id="3fff1-118">儲存組態 BLOB 的精確方法完全取決於要求者。</span><span class="sxs-lookup"><span data-stu-id="3fff1-118">The precise method for storing the configuraiton BLOB is entirely up to the supplicant.</span></span> <span data-ttu-id="3fff1-119">不過，要求者應該一律以適當且安全的方式儲存設定，以適合系統和使用者驗證設定資料。</span><span class="sxs-lookup"><span data-stu-id="3fff1-119">However, the supplicant should always store the configuration in a suitable, secure manner appropriate for system and user authentication configuration data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fff1-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="3fff1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fff1-121">啟用群組原則</span><span class="sxs-lookup"><span data-stu-id="3fff1-121">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="3fff1-122">為 EAP 方法執行 In-Band NAP 支援</span><span class="sxs-lookup"><span data-stu-id="3fff1-122">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="3fff1-123">為 EAP 方法執行 NAP 支援</span><span class="sxs-lookup"><span data-stu-id="3fff1-123">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="3fff1-124">在要求者和 EAP 方法之間傳送資料</span><span class="sxs-lookup"><span data-stu-id="3fff1-124">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="3fff1-125">EAPHost 要求者</span><span class="sxs-lookup"><span data-stu-id="3fff1-125">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




