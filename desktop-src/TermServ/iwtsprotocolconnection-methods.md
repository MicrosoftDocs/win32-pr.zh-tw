---
title: IWTSProtocolConnection 方法
description: IWTSProtocolConnection 介面會公開下列方法。
ms.assetid: DBB96D6B-F5A5-4CAF-974F-44D76B9CBFB6
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb89f63aea6b1904eb4319dcce541aeb4d15d34f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372680"
---
# <a name="iwtsprotocolconnection-methods"></a><span data-ttu-id="32675-103">IWTSProtocolConnection 方法</span><span class="sxs-lookup"><span data-stu-id="32675-103">IWTSProtocolConnection Methods</span></span>

<span data-ttu-id="32675-104">\[IWTSProtocolConnection 不再適用于 Windows Server 2012。\]</span><span class="sxs-lookup"><span data-stu-id="32675-104">\[IWTSProtocolConnection is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="32675-105">[**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="32675-105">The [**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="32675-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="32675-106">In this section</span></span>

-   [<span data-ttu-id="32675-107">**AcceptConnection 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-107">**AcceptConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-acceptconnection)
-   [<span data-ttu-id="32675-108">**AuthenticateClientToSession 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-108">**AuthenticateClientToSession method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-authenticateclienttosession)
-   [<span data-ttu-id="32675-109">**Close 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-109">**Close method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-close)
-   [<span data-ttu-id="32675-110">**ConnectNotify 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-110">**ConnectNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-connectnotify)
-   [<span data-ttu-id="32675-111">**CreateVirtualChannel 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-111">**CreateVirtualChannel method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-createvirtualchannel)
-   [<span data-ttu-id="32675-112">**DisconnectNotify 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-112">**DisconnectNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-disconnectnotify)
-   [<span data-ttu-id="32675-113">**GetClientData 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-113">**GetClientData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getclientdata)
-   [<span data-ttu-id="32675-114">**GetLastInputTime 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-114">**GetLastInputTime method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlastinputtime)
-   [<span data-ttu-id="32675-115">**GetLicenseConnection 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-115">**GetLicenseConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlicenseconnection)
-   [<span data-ttu-id="32675-116">**GetLogonErrorRedirector 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-116">**GetLogonErrorRedirector method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlogonerrorredirector)
-   [<span data-ttu-id="32675-117">**GetProtocolHandles 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-117">**GetProtocolHandles method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolhandles)
-   [<span data-ttu-id="32675-118">**GetProtocolStatus 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-118">**GetProtocolStatus method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolstatus)
-   [<span data-ttu-id="32675-119">**GetShadowConnection 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-119">**GetShadowConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getshadowconnection)
-   [<span data-ttu-id="32675-120">**GetUserCredentials 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-120">**GetUserCredentials method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getusercredentials)
-   [<span data-ttu-id="32675-121">**GetUserData 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-121">**GetUserData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getuserdata)
-   [<span data-ttu-id="32675-122">**IsUserAllowedToLogon 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-122">**IsUserAllowedToLogon method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-isuserallowedtologon)
-   [<span data-ttu-id="32675-123">**LogonNotify 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-123">**LogonNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-logonnotify)
-   [<span data-ttu-id="32675-124">**NotifySessionId 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-124">**NotifySessionId method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-notifysessionid)
-   [<span data-ttu-id="32675-125">**QueryProperty 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-125">**QueryProperty method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty)
-   [<span data-ttu-id="32675-126">**SendBeep 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-126">**SendBeep method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendbeep)
-   [<span data-ttu-id="32675-127">**SendPolicyData 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-127">**SendPolicyData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendpolicydata)
-   [<span data-ttu-id="32675-128">**SessionArbitrationEnumeration 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-128">**SessionArbitrationEnumeration method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sessionarbitrationenumeration)
-   [<span data-ttu-id="32675-129">**SetErrorInfo 方法**</span><span class="sxs-lookup"><span data-stu-id="32675-129">**SetErrorInfo method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-seterrorinfo)

 

 




