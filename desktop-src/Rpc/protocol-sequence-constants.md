---
title: 通訊協定順序常數
description: Microsoft RPC 支援下列通訊協定順序。
ms.assetid: 51284532-b0ac-4bf2-b322-91393b2b9dc6
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
- ncacn_nb_ipx
- ncacn_nb_nb
- ncacn_ip_tcp
- ncacn_np
- ncacn_spx
- ncacn_dnet_nsp
- ncacn_at_dsp
- ncacn_vns_spp
- ncadg_ip_udp
- ncadg_ipx
- ncadg_mq
- ncacn_http
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72c28486bfa3981870ac331ae83f0cbb532bba4d27c44062ce902823e4e3c259
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927128"
---
# <a name="protocol-sequence-constants"></a>通訊協定順序常數

Microsoft RPC 支援下列通訊協定順序。



| 常數/值                                                                                                                                                                                                                                                                                 | 描述                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ncacn_nb_tcp"></span><span id="NCACN_NB_TCP"></span><dl> ncacn 在傳輸控制通訊協定上 <dt>**\_ nb \_ tcp**</dt> <dt>連接導向的 NetBIOS (tcp)</dt> </dl>          | 僅限用戶端： MS-DOS，Windows 3。*x* 用戶端和伺服器： Windows Server 2003、Windows XP、Windows 2000、Windows NT<br/>                                                          |
| <span id="ncacn_nb_ipx"></span><span id="NCACN_NB_IPX"></span><dl> 透過網際網路封包 Exchange <dt>**\_ nb \_ ipx**</dt> <dt>連接導向的 NetBIOS (ipx)</dt> </dl>               | 僅限用戶端： MS-DOS，Windows 3。*x* 用戶端和伺服器： Windows Server 2003、Windows XP、Windows 2000、Windows NT<br/>                                                          |
| <span id="ncacn_nb_nb"></span><span id="NCACN_NB_NB"></span><dl> <dt>**ncacn \_ nb \_**</dt> <dt>的連線導向 NetBIOS 增強消費者介面 (NetBEUI)</dt> </dl>                    | 僅限用戶端： MS-DOS，Windows 3。*x* 用戶端和伺服器： Windows Server 2003、Windows XP、Windows 2000、Windows NT、Windows Me、Windows 98、Windows 95<br/>                      |
| <span id="ncacn_ip_tcp"></span><span id="NCACN_IP_TCP"></span><dl> <dt>**ncacn \_ ip \_ tcp**</dt> <dt>連接導向的傳輸控制通訊協定/網際網路通訊協定 (tcp/ip)</dt> </dl>  | 僅限用戶端： MS-DOS，Windows 3。*x* 和 Apple Macintosh 用戶端和伺服器： Windows Server 2003、Windows XP、Windows 2000、Windows NT、Windows Me、Windows 98、Windows 95<br/> |
| <span id="ncacn_np"></span><span id="NCACN_NP"></span><dl> <dt>**ncacn \_ np**</dt> <dt>連接導向具名管道</dt> </dl>                                                            | 僅限用戶端： MS-DOS，Windows 3。*x*、Windows 95 用戶端和伺服器： Windows Server 2003、Windows XP、Windows 2000、Windows NT<br/>                                              |
| <span id="ncacn_spx"></span><span id="NCACN_SPX"></span><dl> <dt>**ncacn \_ spx**</dt> <dt>連接導向的排序封包 Exchange (spx)</dt> </dl>                                     | 僅限用戶端： MS-DOS，Windows 3。*x* 用戶端和伺服器： Windows Server 2003、Windows XP、Windows 2000、Windows NT、Windows Me、Windows 98、Windows 95<br/>                      |
| <span id="ncacn_dnet_nsp"></span><span id="NCACN_DNET_NSP"></span><dl> <dt>**ncacn \_ dnet \_ Nsp**</dt> <dt>連接導向 DECnet 傳輸</dt> </dl>                                    | 僅限用戶端： MS-DOS，Windows 3。*x*<br/>                                                                                                                                       |
| <span id="ncacn_at_dsp"></span><span id="NCACN_AT_DSP"></span><dl> <dt>**ncacn \_ 于 \_ dsp**</dt> <dt>連接導向的 AppleTalk dsp</dt> </dl>                                             | 用戶端： Apple Macintosh 伺服器： Windows Server 2003、Windows XP、Windows 2000、Windows NT<br/>                                                                                |
| <span id="ncacn_vns_spp"></span><span id="NCACN_VNS_SPP"></span><dl> <dt>**ncacn \_ vns \_ Spp**</dt> <dt>連接導向 Vines 可調整的平行處理 (spp) 傳輸</dt> </dl>     | 僅限用戶端： MS-DOS，Windows 3。*x* 用戶端和伺服器： Windows Server 2003、Windows XP、Windows 2000、Windows NT<br/>                                                          |
| <span id="ncadg_ip_udp"></span><span id="NCADG_IP_UDP"></span><dl> <dt>**ncadg \_ ip \_ udp**</dt> <dt>資料包 (無連接) 使用者資料包協定/網際網路通訊協定 (udp/ip)</dt> </dl>   | 僅限用戶端： MS-DOS，Windows 3。*x* 用戶端和伺服器： Windows Server 2003、Windows XP、Windows 2000、Windows NT<br/>                                                          |
| <span id="ncadg_ipx"></span><span id="NCADG_IPX"></span><dl> <dt>**ncadg \_ ipx**</dt> <dt>資料包 (無連接) ipx</dt> </dl>                                                           | 僅限用戶端： MS-DOS，Windows 3。*x* 用戶端和伺服器： Windows Server 2003、Windows XP、Windows 2000、Windows NT<br/>                                                          |
| <span id="ncadg_mq"></span><span id="NCADG_MQ"></span><dl> <dt>**ncadg \_ mq**</dt> <dt>資料包 (沒有連接) 透過 Microsoft 訊息佇列伺服器 (MSMQ)</dt> </dl>                   | 僅限用戶端： Windows Me/98/95 用戶端和伺服器： Windows server 2003、Windows XP、Windows 2000、Windows NT server 4.0 SP3 和更新版本<br/>                                 |
| <span id="ncacn_http"></span><span id="NCACN_HTTP"></span><dl> <dt>使用 Microsoft Internet Information Server 作為 HTTP proxy 的</dt> <dt>**ncacn \_ HTTP**</dt>連線導向 tcp/ip </dl> | 僅限用戶端： Windows Me/98/95 用戶端和伺服器： Windows Server 2003、Windows XP、Windows 2000<br/>                                                                           |
| <span id="ncalrpc"></span><span id="NCALRPC"></span><dl> <dt>**ncalrpc**</dt> <dt>本機程序呼叫</dt> </dl>                                                                           | 用戶端和伺服器： Windows Server 2003、Windows XP、Windows 2000、Windows NT、Windows Me、Windows 98、Windows 95<br/>                                                         |



## <a name="remarks"></a>備註

[**Ncalrpc**](/windows/desktop/Midl/ncalrpc)傳輸僅支援 RPC \_ C \_ 驗證 \_ WINNT 驗證。 如需詳細資訊，請參閱 [安全性](security.md) 和 [驗證-服務常數](authentication-service-constants.md)。

Microsoft RPC 只支援在用戶端應用程式中 [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy) ，不支援在伺服器應用程式中。

 

