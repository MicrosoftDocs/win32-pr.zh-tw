---
title: WinRM 常數和列舉
description: Windows遠端系統管理具有用來建立會話和列舉的位旗標，以及對 proxy 伺服器的存取類型和驗證。
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73de8f418d5b0fb0bd7adebb8439ccbce67f0bcb6aacf72ed2665683c00e0076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742934"
---
# <a name="winrm-constants-and-enumerations"></a>WinRM 常數和列舉

Windows遠端系統管理具有用來建立會話和列舉的位旗標，以及對 proxy 伺服器的存取類型和驗證。 下列清單列出不同的位旗標。

<dl> <dt>

<span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[會話常數](session-constants.md)
</dt> <dd>

[**CreateSession**](wsman-createsession.md)或 [**IWSMan：： CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)方法的 *flags* 參數中所使用的旗標。

</dd> <dt>

<span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**列舉常數**](enumeration-constants.md)
</dt> <dd>

旗標，用於呼叫 Session 的 *旗標* 參數 [**。列舉**](session-enumerate.md) 或 [**iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)。

</dd> <dt>

<span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)
</dt> <dd>

*AuthenticationMechanism* 參數中用來呼叫 [**IWSManConnectionOptionsEx2：： SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)的旗標。

</dd> <dt>

<span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)
</dt> <dd>

*AccessType* 參數中用來呼叫 [**IWSManConnectionOptionsEx2：： SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)的旗標。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows遠端系統管理參考](windows-remote-management-reference.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[**IWSMan：： CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[**IWSManConnectionOptionsEx2：： SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




