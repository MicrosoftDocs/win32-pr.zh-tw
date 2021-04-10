---
title: Windows 部署服務結構
description: 下列結構會搭配 Windows 部署服務使用。
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20f5b369a2bbb5d68bd77dce1751e09fed2e6b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021946"
---
# <a name="windows-deployment-services-structures"></a><span data-ttu-id="a5524-103">Windows 部署服務結構</span><span class="sxs-lookup"><span data-stu-id="a5524-103">Windows Deployment Services Structures</span></span>

<span data-ttu-id="a5524-104">下列結構會搭配 Windows 部署服務使用。</span><span class="sxs-lookup"><span data-stu-id="a5524-104">The following structures are used with Windows Deployment Services.</span></span>



| <span data-ttu-id="a5524-105">結構</span><span class="sxs-lookup"><span data-stu-id="a5524-105">Structure</span></span>                                                                         | <span data-ttu-id="a5524-106">Description</span><span class="sxs-lookup"><span data-stu-id="a5524-106">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5524-107">**PXE \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="a5524-107">**PXE\_ADDRESS**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | <span data-ttu-id="a5524-108">指定封包的網路位址。</span><span class="sxs-lookup"><span data-stu-id="a5524-108">Specifies the network address for a packet.</span></span>                                                                        |
| [<span data-ttu-id="a5524-109">**PXE \_ DHCP \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="a5524-109">**PXE\_DHCP\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | <span data-ttu-id="a5524-110">此結構會與 Windows 部署服務 PXE 伺服器 API 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a5524-110">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="a5524-111">**PXE \_ DHCP \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="a5524-111">**PXE\_DHCP\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | <span data-ttu-id="a5524-112">此結構會與 Windows 部署服務 PXE 伺服器 API 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a5524-112">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="a5524-113">**PXE \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="a5524-113">**PXE\_PROVIDER**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | <span data-ttu-id="a5524-114">描述提供者。</span><span class="sxs-lookup"><span data-stu-id="a5524-114">Describes a provider.</span></span>                                                                                              |
| [<span data-ttu-id="a5524-115">**WDS \_ CLI \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="a5524-115">**WDS\_CLI\_CRED**</span></span>](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | <span data-ttu-id="a5524-116">包含用來授權用戶端會話的認證。</span><span class="sxs-lookup"><span data-stu-id="a5524-116">Contains credentials used to authorize a client session.</span></span>                                                           |
| [<span data-ttu-id="a5524-117">**WDS \_ TRANSPORTCLIENT \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="a5524-117">**WDS\_TRANSPORTCLIENT\_REQUEST**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | <span data-ttu-id="a5524-118">由 [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="a5524-118">Used by the [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) function.</span></span>                     |
| [<span data-ttu-id="a5524-119">**TRANSPORTCLIENT \_ 會話 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="a5524-119">**TRANSPORTCLIENT\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | <span data-ttu-id="a5524-120">由 [*PFN \_ WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) 回呼函數使用。</span><span class="sxs-lookup"><span data-stu-id="a5524-120">Used by the [*PFN\_WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) callback function.</span></span> |
| [<span data-ttu-id="a5524-121">**WDS \_ TRANSPORTPROVIDER \_ INIT \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="a5524-121">**WDS\_TRANSPORTPROVIDER\_INIT\_PARAMS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | <span data-ttu-id="a5524-122">由 [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) 回呼函式使用。</span><span class="sxs-lookup"><span data-stu-id="a5524-122">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |
| [<span data-ttu-id="a5524-123">**WDS \_ TRANSPORTPROVIDER \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="a5524-123">**WDS\_TRANSPORTPROVIDER\_SETTINGS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | <span data-ttu-id="a5524-124">由 [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) 回呼函式使用。</span><span class="sxs-lookup"><span data-stu-id="a5524-124">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |



 

<span data-ttu-id="a5524-125">從 Windows 8 和 Windows Server 2012 開始提供下列各項。</span><span class="sxs-lookup"><span data-stu-id="a5524-125">The following is available beginning with Windows 8 and Windows Server 2012.</span></span>

| <span data-ttu-id="a5524-126">結構</span><span class="sxs-lookup"><span data-stu-id="a5524-126">Structure</span></span>                                          | <span data-ttu-id="a5524-127">Description</span><span class="sxs-lookup"><span data-stu-id="a5524-127">Description</span></span>                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="a5524-128">**PXE \_ DHCPV6 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="a5524-128">**PXE\_DHCPV6\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | <span data-ttu-id="a5524-129">與 Windows 部署服務 PXE 伺服器 API 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a5524-129">Used with the Windows Deployment Services PXE Server API.</span></span> |
| [<span data-ttu-id="a5524-130">**PXE \_ DHCPV6 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="a5524-130">**PXE\_DHCPV6\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | <span data-ttu-id="a5524-131">DHCPV6 訊息。</span><span class="sxs-lookup"><span data-stu-id="a5524-131">A DHCPV6 message.</span></span>                                         |



 

 

 




