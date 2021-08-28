---
description: WinHTTP 支援的網際網路架構。
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: 'INTERNET_SCHEME (WinHTTP. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0429d07ef366acdc881a82373194e153ad3c8f367172b7e64221ecf479e7bf3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644018"
---
# <a name="internet_scheme"></a>網際網路 \_ 配置

WinHTTP 支援的網際網路架構。

<dl> <dt>

<span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**網際網路 \_ 配置 \_ HTTP**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



HTTP 網際網路配置。


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**網際網路 \_ 配置 \_ HTTPS**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



HTTPS (SSL) 網際網路配置。


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**網際網路 \_ 配置 \_ FTP**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



FTP 網際網路配置。 此配置僅支援在 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 和 [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)中使用。


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**網際網路 \_ 配置 \_ SOCKS**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



SOCKS 網際網路配置。 此配置僅支援在 [**WINHTTP \_ PROXY \_ 結果 \_ 專案**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)中使用。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP、Windows 2000 Professional 搭配 SP3 \[ desktop 應用程式\]<br/>      |
| 最低支援的伺服器<br/> | Windows伺服器2003、Windows 2000 伺服器（僅含 SP3 \[ desktop 應用程式）\]<br/>   |
| 標頭<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WINHTTP \_ PROXY \_ 結果 \_ 專案**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 




