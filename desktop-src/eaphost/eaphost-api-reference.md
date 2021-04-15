---
title: EAPHost API 參考
description: 瞭解 EAPHost Api 及其元件。 請參閱各種 API 主題的參考資訊，例如 EAPHost XML 架構。
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c4d80c402f963a05bbcfb79ca451541603489e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382829"
---
# <a name="eaphost-api-reference"></a><span data-ttu-id="cc16f-104">EAPHost API 參考</span><span class="sxs-lookup"><span data-stu-id="cc16f-104">EAPHost API Reference</span></span>

<span data-ttu-id="cc16f-105">EAPHost Api 分為三個元件：要求者 Api，可從已啟用 EAP 的應用程式直接呼叫;EAP 對等方法 Api，可管理特定 EAP 驗證類型的要求者要求，並在用戶端上引發互動式元素;和 EAP 驗證器 API，可執行要求者的伺服器端驗證。</span><span class="sxs-lookup"><span data-stu-id="cc16f-105">The EAPHost APIs are divided into three components: the supplicant APIs, which are directly callable from an EAP-enabled application; the EAP peer method APIs, which manage supplicant requests for a specific EAP authentication type and raise interactive elements on the client; and the EAP authenticator APIS, which perform the server-side authentication of a supplicant.</span></span>

<span data-ttu-id="cc16f-106">後兩個 API 元件--EAP 對等方法和 EAP 驗證器方法 Api--在將它們公開給 EAPHost 服務的 Dll 中，需要有自訂且一致的執行。</span><span class="sxs-lookup"><span data-stu-id="cc16f-106">The latter two API components -- the EAP Peer Method and EAP Authenticator Method APIs -- require custom and conformant implementation in DLLs that expose them to the EAPHost service.</span></span> <span data-ttu-id="cc16f-107">您無法直接從應用程式程式碼呼叫它們;相反地，它們是由用戶端上的 EAPHost (的 EAP 對等方法，以及 EAP 驗證器方法的伺服器端所呼叫) 如果執行是否符合對應檔中指定的 API 簽章。</span><span class="sxs-lookup"><span data-stu-id="cc16f-107">They cannot be called directly from application code; instead, they are called by EAPHost (on client side for EAP peer methods, and on the server side for EAP authenticator methods) if the implementation matches the API signatures specified in the corresponding documentation.</span></span> <span data-ttu-id="cc16f-108">每個函式參考頁面上都會提供 API 實行的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="cc16f-108">API implementation specific information is provided on each function reference page.</span></span>

## <a name="eaphost-registry-settings"></a><span data-ttu-id="cc16f-109">EAPHost 登錄設定</span><span class="sxs-lookup"><span data-stu-id="cc16f-109">EAPHost Registry Settings</span></span>



| <span data-ttu-id="cc16f-110">主題</span><span class="sxs-lookup"><span data-stu-id="cc16f-110">Topic</span></span>                                                      | <span data-ttu-id="cc16f-111">描述</span><span class="sxs-lookup"><span data-stu-id="cc16f-111">Description</span></span>                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="cc16f-112">EAPHost 登錄設定</span><span class="sxs-lookup"><span data-stu-id="cc16f-112">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md) | <span data-ttu-id="cc16f-113">描述 EAPHost 所使用的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="cc16f-113">Describes the registry keys consumed by EAPHost.</span></span> |



 

## <a name="eaphost-xml-schema"></a><span data-ttu-id="cc16f-114">EAPHost XML 架構</span><span class="sxs-lookup"><span data-stu-id="cc16f-114">EAPHost XML Schema</span></span>



| <span data-ttu-id="cc16f-115">主題</span><span class="sxs-lookup"><span data-stu-id="cc16f-115">Topic</span></span>                                            | <span data-ttu-id="cc16f-116">描述</span><span class="sxs-lookup"><span data-stu-id="cc16f-116">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc16f-117">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="cc16f-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md) | <span data-ttu-id="cc16f-118">描述用於建立設定 XML 和認證 XML 的 EAPHost 架構和舊版架構。</span><span class="sxs-lookup"><span data-stu-id="cc16f-118">Describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span> |



 

## <a name="common-eaphost-api-reference"></a><span data-ttu-id="cc16f-119">Common EAPHost API 參考</span><span class="sxs-lookup"><span data-stu-id="cc16f-119">Common EAPHost API Reference</span></span>



| <span data-ttu-id="cc16f-120">主題</span><span class="sxs-lookup"><span data-stu-id="cc16f-120">Topic</span></span>                                                                   | <span data-ttu-id="cc16f-121">描述</span><span class="sxs-lookup"><span data-stu-id="cc16f-121">Description</span></span>                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="cc16f-122">常見的 EAPHost API 列舉</span><span class="sxs-lookup"><span data-stu-id="cc16f-122">Common EAPHost API Enumerations</span></span>](common-eap-host-api-enumerations.md) | <span data-ttu-id="cc16f-123">列出所有 EAPHost Api 通用的常數。</span><span class="sxs-lookup"><span data-stu-id="cc16f-123">Lists constants common to all EAPHost APIs.</span></span>  |
| [<span data-ttu-id="cc16f-124">常見的 EAPHost API 結構</span><span class="sxs-lookup"><span data-stu-id="cc16f-124">Common EAPHost API Structures</span></span>](common-eap-host-api-structures.md)     | <span data-ttu-id="cc16f-125">列出所有 EAPHost Api 通用的結構。</span><span class="sxs-lookup"><span data-stu-id="cc16f-125">Lists structures common to all EAPHost APIs.</span></span> |
| [<span data-ttu-id="cc16f-126">常見的 EAPHost API 常數</span><span class="sxs-lookup"><span data-stu-id="cc16f-126">Common EAPHost API Constants</span></span>](common-eap-host-error-constants.md)     | <span data-ttu-id="cc16f-127">列出所有 EAPHost Api 通用的常數。</span><span class="sxs-lookup"><span data-stu-id="cc16f-127">Lists constants common to all EAPHost APIs.</span></span>  |



 

## <a name="eaphost-api-reference"></a><span data-ttu-id="cc16f-128">EAPHost API 參考</span><span class="sxs-lookup"><span data-stu-id="cc16f-128">EAPHost API Reference</span></span>



| <span data-ttu-id="cc16f-129">主題</span><span class="sxs-lookup"><span data-stu-id="cc16f-129">Topic</span></span>                                                                       | <span data-ttu-id="cc16f-130">描述</span><span class="sxs-lookup"><span data-stu-id="cc16f-130">Description</span></span>                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc16f-131">EAPHost 要求者 API 參考</span><span class="sxs-lookup"><span data-stu-id="cc16f-131">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)   | <span data-ttu-id="cc16f-132">描述可讓要求者呼叫 EAPHost 的 API 元素。</span><span class="sxs-lookup"><span data-stu-id="cc16f-132">Describes the API elements available to enable supplicant calls to EAPHost.</span></span>                                                                      |
| [<span data-ttu-id="cc16f-133">EAPHost 對等方法 API 參考</span><span class="sxs-lookup"><span data-stu-id="cc16f-133">EAPHost Peer Method API Reference</span></span>](eap-host-peer-method-api-reference.md) | <span data-ttu-id="cc16f-134">描述必須實作為的 API 元素，以建立可由用戶端 EAPHost 載入和呼叫的 EAP 對等方法 DLL。</span><span class="sxs-lookup"><span data-stu-id="cc16f-134">Describes the API elements that must be implemented to create an EAP peer method DLL that can be loaded and called by a client EAPHost.</span></span>          |
| [<span data-ttu-id="cc16f-135">EAPHost 驗證器方法 Api</span><span class="sxs-lookup"><span data-stu-id="cc16f-135">EAPHost Authenticator Method APIs</span></span>](eaphost-authenticator-method-apis.md)  | <span data-ttu-id="cc16f-136">描述必須執行的 API 專案，以建立可由伺服器 EAPHost 載入和呼叫的 EAP 驗證器方法 DLL。</span><span class="sxs-lookup"><span data-stu-id="cc16f-136">Describes the API elements that must be implemented to create an EAP authenticator method DLL that can be loaded and called by a server EAPHost.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cc16f-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="cc16f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc16f-138">關於 EAPHost</span><span class="sxs-lookup"><span data-stu-id="cc16f-138">About EAPHost</span></span>](about-eap-host.md)
</dt> <dt>

[<span data-ttu-id="cc16f-139">使用 EAPHost</span><span class="sxs-lookup"><span data-stu-id="cc16f-139">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 




