---
description: Windows 通訊端 (Winsock) 通訊端選項的流覽頁面。
ms.assetid: e2831f76-4499-45b6-bc60-2908ec3a246c
title: 通訊端選項
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPPROTO_IP
- IPPROTO_IPV6
- IPPROTO_RM
- IPPROTO_TCP
- IPPROTO_UDP
- NSPROTO_IPX
- SOL_APPLETALK
- SOL_IRLMP
- SOL_SOCKET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 37da2ff25fe51b08c036fe75ac55b9b3fdb508d1d24dcc151ecd87e04e3b63b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383878"
---
# <a name="socket-options"></a>通訊端選項

本節說明各種 Windows 作業系統版本的 Winsock 通訊端選項。 使用 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 和 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數來取得和設定通訊端選項。 若要列舉通訊協定，並針對每個已安裝的通訊協定探索支援的屬性，請使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) 函式。

有些通訊端選項需要比這些資料表可以傳達的更多說明;這類選項包含其他頁面的連結。

<dl> <dt>

<span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**IPPROTO \_ IP**
</dt> <dd> <dl> <dt>



適用于 IPv4 層級的通訊端選項。 如需詳細資訊，請參閱 [**IPPROTO \_ IP 通訊端選項**](ipproto-ip-socket-options.md)。


</dt> </dl> </dd> <dt>

<span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**IPPROTO \_ IPV6**
</dt> <dd> <dl> <dt>



適用于 IPv6 層級的通訊端選項。 如需詳細資訊，請參閱 [**IPPROTO \_ IPV6 通訊端選項**](ipproto-ipv6-socket-options.md)。


</dt> </dl> </dd> <dt>

<span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO \_ RM**
</dt> <dd> <dl> <dt>



適用于可靠多播層級的通訊端選項。 如需詳細資訊，請參閱 [**IPPROTO \_ RM 通訊端選項**](ipproto-rm-socket-options.md)。


</dt> </dl> </dd> <dt>

<span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**IPPROTO \_ TCP**
</dt> <dd> <dl> <dt>



適用于 TCP 層級的通訊端選項。 如需詳細資訊，請參閱 [**IPPROTO \_ TCP 通訊端選項**](ipproto-tcp-socket-options.md)。


</dt> </dl> </dd> <dt>

<span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO \_ UDP**
</dt> <dd> <dl> <dt>



適用于 UDP 層級的通訊端選項。 如需詳細資訊，請參閱 [**IPPROTO \_ UDP 通訊端選項**](ipproto-udp-socket-options.md)。


</dt> </dl> </dd> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO \_ IPX**
</dt> <dd> <dl> <dt>



適用于 IPX 層級的通訊端選項。 如需詳細資訊，請參閱 [**NSPROTO \_ IPX 通訊端選項**](nsproto-ipx-socket-options.md)。


</dt> </dl> </dd> <dt>

<span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL \_ APPLETALK**
</dt> <dd> <dl> <dt>



適用于 AppleTalk 層級的通訊端選項。 如需詳細資訊，請參閱 [**SOL \_ APPLETALK 通訊端選項**](sol-appletalk-socket-options.md)。


</dt> </dl> </dd> <dt>

<span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL \_ IRLMP**
</dt> <dd> <dl> <dt>



適用于紅外線連結管理通訊協定層級的通訊端選項。 For more information, see the [**SOL\_IRLMP Socket Options**](sol-irlmp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_SOCKET"></span><span id="sol_socket"></span>**SOL \_ 通訊端**
</dt> <dd> <dl> <dt>



通訊端選項適用于通訊端層級。 如需詳細資訊，請參閱 [**SOL \_ 通訊端通訊端選項**](sol-socket-socket-options.md)。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

所有 \_ \* 通訊端選項都同樣適用于 IPv4 和 IPv6 (但 \_ 因為廣播不是在 IPv6) 中執行，所以廣播除外。

 

 



