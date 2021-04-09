---
title: WinRM 常數和列舉
description: Windows 遠端管理具有用來建立會話和列舉的位旗標，以及對 proxy 伺服器的存取類型和驗證。
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0789d440ff0f88cc037e0dc9e544ca559c1af5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021751"
---
# <a name="winrm-constants-and-enumerations"></a><span data-ttu-id="a25eb-103">WinRM 常數和列舉</span><span class="sxs-lookup"><span data-stu-id="a25eb-103">WinRM Constants and Enumerations</span></span>

<span data-ttu-id="a25eb-104">Windows 遠端管理具有用來建立會話和列舉的位旗標，以及對 proxy 伺服器的存取類型和驗證。</span><span class="sxs-lookup"><span data-stu-id="a25eb-104">Windows Remote Management has bit flags used in creating sessions and enumerations, and for access types and authentication to a proxy server.</span></span> <span data-ttu-id="a25eb-105">下列清單列出不同的位旗標。</span><span class="sxs-lookup"><span data-stu-id="a25eb-105">The following list lists the different bit flags.</span></span>

<dl> <dt>

<span data-ttu-id="a25eb-106"><span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[會話常數](session-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a25eb-106"><span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Session Constants](session-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="a25eb-107">[**CreateSession**](wsman-createsession.md)或 [**IWSMan：： CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)方法的 *flags* 參數中所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="a25eb-107">Flags used in *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) or [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) methods.</span></span>

</dd> <dt>

<span data-ttu-id="a25eb-108"><span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**列舉常數**](enumeration-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a25eb-108"><span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Enumeration Constants**](enumeration-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="a25eb-109">旗標，用於呼叫 Session 的 *旗標* 參數 [**。列舉**](session-enumerate.md) 或 [**iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)。</span><span class="sxs-lookup"><span data-stu-id="a25eb-109">Flags used in *flags* parameter of call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

</dd> <dt>

<span data-ttu-id="a25eb-110"><span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)</span><span class="sxs-lookup"><span data-stu-id="a25eb-110"><span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)</span></span>
</dt> <dd>

<span data-ttu-id="a25eb-111">*AuthenticationMechanism* 參數中用來呼叫 [**IWSManConnectionOptionsEx2：： SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)的旗標。</span><span class="sxs-lookup"><span data-stu-id="a25eb-111">Flags used in *authenticationMechanism* parameter of call to [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span></span>

</dd> <dt>

<span data-ttu-id="a25eb-112"><span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)</span><span class="sxs-lookup"><span data-stu-id="a25eb-112"><span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)</span></span>
</dt> <dd>

<span data-ttu-id="a25eb-113">*AccessType* 參數中用來呼叫 [**IWSManConnectionOptionsEx2：： SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)的旗標。</span><span class="sxs-lookup"><span data-stu-id="a25eb-113">Flags used in *accessType* parameter of call to [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a25eb-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="a25eb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a25eb-115">Windows 遠端管理參考</span><span class="sxs-lookup"><span data-stu-id="a25eb-115">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dt>

[<span data-ttu-id="a25eb-116">**WSMan. CreateSession**</span><span class="sxs-lookup"><span data-stu-id="a25eb-116">**WSMan.CreateSession**</span></span>](wsman-createsession.md)
</dt> <dt>

[<span data-ttu-id="a25eb-117">**IWSMan：： CreateSession**</span><span class="sxs-lookup"><span data-stu-id="a25eb-117">**IWSMan::CreateSession**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[<span data-ttu-id="a25eb-118">**IWSManConnectionOptionsEx2：： SetProxy**</span><span class="sxs-lookup"><span data-stu-id="a25eb-118">**IWSManConnectionOptionsEx2::SetProxy**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




