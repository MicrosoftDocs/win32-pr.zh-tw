---
title: 使用安全驗證通道
description: 使用安全驗證通道
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Media 裝置管理員，驗證
- 裝置管理員，驗證
- 桌面應用程式，驗證
- 服務提供者，驗證
- 程式設計指南，驗證
- 驗證 (authentication)
- Windows Media 裝置管理員，安全通訊
- 裝置管理員，安全通訊
- 桌面應用程式，安全通訊
- 服務提供者，安全通訊
- 程式設計指南，安全通訊
- 安全通訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88c271cecc2e9252a3f7af0540beef3dc57d2b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021077"
---
# <a name="using-secure-authenticated-channels"></a><span data-ttu-id="72b02-115">使用安全驗證通道</span><span class="sxs-lookup"><span data-stu-id="72b02-115">Using Secure Authenticated Channels</span></span>

<span data-ttu-id="72b02-116">Windows Media 裝置管理員提供兩個 helper 類別、適用于應用程式的 [CSecureChannelClient](csecurechannelclient-class.md) () 與服務提供者的 [CSecureChannelServer](csecurechannelserver-class.md) (，以及) 的一個介面 [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (，藉以啟用元件之間的驗證和安全通訊。</span><span class="sxs-lookup"><span data-stu-id="72b02-116">Windows Media Device Manager enables authentication and secure communication between components by providing two helper classes, [CSecureChannelClient](csecurechannelclient-class.md) (for applications) and [CSecureChannelServer](csecurechannelserver-class.md) (for service providers), and one interface, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (for both).</span></span> <span data-ttu-id="72b02-117">這些會一起組成 API，以使用安全驗證通道 (SAC) 。</span><span class="sxs-lookup"><span data-stu-id="72b02-117">Together these make up an API for the use of secure authenticated channels (SAC).</span></span> <span data-ttu-id="72b02-118">SAC 針對使用 Windows Media 裝置管理員的服務提供者或應用程式處理下列三項工作：</span><span class="sxs-lookup"><span data-stu-id="72b02-118">SAC handles the following three tasks for service providers or applications using Windows Media Device Manager:</span></span>

-   [<span data-ttu-id="72b02-119">元件驗證</span><span class="sxs-lookup"><span data-stu-id="72b02-119">Component Authentication</span></span>](component-authentication.md)
-   [<span data-ttu-id="72b02-120">加密和解密</span><span class="sxs-lookup"><span data-stu-id="72b02-120">Encryption and Decryption</span></span>](encryption-and-decryption.md)
-   [<span data-ttu-id="72b02-121">訊息驗證</span><span class="sxs-lookup"><span data-stu-id="72b02-121">Message Authentication</span></span>](message-authentication.md)

<span data-ttu-id="72b02-122">應用程式或服務提供者必須處理元件驗證、加密和解密;訊息驗證是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="72b02-122">An application or service provider must handle component authentication, encryption, and decryption; message authentication is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72b02-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="72b02-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72b02-124">**應用程式和服務提供者的一般工作**</span><span class="sxs-lookup"><span data-stu-id="72b02-124">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




