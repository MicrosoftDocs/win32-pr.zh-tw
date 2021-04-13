---
title: 字串系結
description: 字串系結是由字串組成的不帶正負號字元字串，代表系結物件 UUID、RPC 通訊協定序列、網路位址，以及端點和端點選項。
ms.assetid: 5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d804fe614185b054b8041e13069e900501342a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376280"
---
# <a name="string-binding"></a>字串系結

字串系結是由字串組成的不帶正負號字元字串，代表系結物件 UUID、RPC 通訊協定序列、網路位址，以及端點和端點選項。

*ObjectUUID* @*ProtocolSequence*：*networkaddress.cache.ttl* \[ *端點*，*選項*\]

## <a name="parameters"></a>參數

<dl> <dt>

<span id="ObjectUUID"></span><span id="objectuuid"></span><span id="OBJECTUUID"></span>*ObjectUUID*
</dt> <dd>

遠端程序呼叫所操作之物件的[UUID](/windows/desktop/Midl/uuid) 。 在伺服器上，RPC 執行時間程式庫會將物件類型對應至 () 函式指標陣列來叫用正確管理員常式的管理員進入點向量。 如需如何將物件 Uuid 對應至經理進入點向量的討論，請參閱 [註冊介面](registering-interfaces.md)。

</dd> <dt>

<span id="ProtocolSequence"></span><span id="protocolsequence"></span><span id="PROTOCOLSEQUENCE"></span>*ProtocolSequence*
</dt> <dd>

代表 RPC 通訊協定 (的有效組合的字元字串，例如 ncacn) 、傳輸通訊協定 (例如 TCP) ，以及網路通訊協定 (例如 IP) 。 Microsoft RPC 支援下列 [通訊協定順序常數](protocol-sequence-constants.md)中指定的通訊協定。

</dd> <dt>

<span id="NetworkAddress"></span><span id="networkaddress"></span><span id="NETWORKADDRESS"></span>*Networkaddress.cache.ttl*
</dt> <dd>

接收遠端程序呼叫之系統的網路位址。

> [!Note]  
> Windows XP 不支援下列通訊協定順序：

 

-   [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)
-   [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)
-   [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)
-   [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp)
-   [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)
-   [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)
-   [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)

網路位址的格式和內容取決於指定的通訊協定順序，如下所示。



| 通訊協定順序                       | 網路位址                                                                                                                                  | 範例                                               |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)     | 電腦名稱                                                                                                                                    | myserver                                               |
| [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)     | 電腦名稱                                                                                                                                    | myserver                                               |
| [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)       | 電腦名稱                                                                                                                                    | myserver                                               |
| [ncacn \_ ip \_ tcp](/windows/desktop/Midl/ncacn-ip-tcp)     | 四個八位的網際網路位址或主機名稱。 如果已安裝 IPv6 網路堆疊，則會完全支援 IPv6，而且也會接受 IPv6 位址。 | 128.10.2.30 anynode.microsoft.com                      |
| [ncacn \_ np](/windows/desktop/Midl/ncacn-np)              | 伺服器名稱 (前置雙反斜線是選擇性的)                                                                                             | myserver \\ \\ myotherserver                             |
| [ncacn \_ spx](/windows/desktop/Midl/ncacn-spx)            | IPX 網際網路位址或伺服器名稱                                                                                                             | ~ 0000000108002B30612C myserver                         |
| [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp) | 區域和節點語法                                                                                                                             | 4.120                                                  |
| [\_在 \_ dsp ncacn](/windows/desktop/Midl/ncacn-at-dsp)     | 電腦名稱稱，選擇性地接著 @ 和 AppleTalk 區功能變數名稱稱。 預設為 @ \* 、用戶端的區域（如果未提供任何區域）                     | servername@zonename servername                         |
| [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | 表單的 StreetTalk 伺服器名稱 item@group@organization                                                                                       | printserver@sdkdocs@microsoft                          |
| [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)              | 伺服器名稱                                                                                                                                      | myserver                                               |
| [ncacn \_ HTTP](/windows/desktop/Midl/ncacn-http)          | 網際網路位址 (四個八位或易記名稱，或本機伺服器名稱                                                                       | 128.10.2.30 somesvr@anywhere.com mylocalsvr<br/> |
| [ncadg \_ ip \_ udp](/windows/desktop/Midl/ncadg-ip-udp)     | 四個八位的網際網路位址或主機名稱                                                                                                        | 128.10.2.30 anynode.microsoft.com                      |
| [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)            | IPX 網際網路位址或伺服器名稱                                                                                                             | ~ 0000000108002B30612C myserver                         |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | 電腦名稱                                                                                                                                     | thismachine                                            |



 

[網路位址] 欄位是選擇性的。 當您未指定網路位址時，字串系結會參考您的本機主機。 當您使用 **ncalrpc** 通訊協定順序時，可以指定本機電腦的名稱，不過這樣做完全不需要。

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>*端點*
</dt> <dd>

接收遠端程序呼叫之進程的端點或位址。 端點之前可以有關鍵詞 **端點 =**。 如果伺服器已向端點對應程式註冊其系結，則指定端點是選擇性的。 請參閱 [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)。

端點的格式和內容取決於指定的通訊協定順序，如下列端點/選項表所示。

</dd> <dt>

<span id="Option"></span><span id="option"></span><span id="OPTION"></span>*選項*
</dt> <dd>

通訊協定特定的選項。 選項欄位不是必要的。 每個選項都是由使用語法 *選項名稱* = *選項值* 的 {name，value} 配對所指定。 系統會為每個通訊協定序列定義選項，如下列端點/選項表格所示。



| 通訊協定順序                       | 端點                                                                                           | 範例             | 選項名稱                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------|----------------------|--------------------------------------------------------|
| [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)     | 介於1到254之間的整數。 0和32之間的許多值都是由 Microsoft 所保留。                 | 100                  | 無                                                   |
| [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)     |  (如上所示)                                                                                          |  (如上所示)            | 無                                                   |
| [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)       |  (如上所示)                                                                                          |  (如上所示)            | 無                                                   |
| [ncacn \_ ip \_ tcp](/windows/desktop/Midl/ncacn-ip-tcp)     | 網際網路埠號碼。                                                                              | 1025                 | 無                                                   |
| [ncacn \_ np](/windows/desktop/Midl/ncacn-np)              | 具名管道。 名稱必須以 " \\ \\ pipe" 開頭。                                                       | \\\\管道 \\ \\ pipename | 安全性                                               |
| [ncacn \_ spx](/windows/desktop/Midl/ncacn-spx)            | 介於1到65535之間的整數。                                                                       | 5000                 | 無                                                   |
| [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp) | DECnet 階段 IV 物件編號 (前面必須加 \# 上字元) 或物件名稱。              | mailserver \# 17      | 無                                                   |
| [\_在 \_ dsp ncacn](/windows/desktop/Midl/ncacn-at-dsp)     | 字元字串，長度最多為22個位元組。                                                           | myservicesendpoint   | 無                                                   |
| [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Vines 在250到511之間的 SPP 埠號碼。                                                         | 500                  | 無                                                   |
| [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)              | 介於1到65535之間的整數。                                                                       | 5000                 | 無                                                   |
| [ncacn \_ HTTP](/windows/desktop/Midl/ncacn-http)          | 網際網路埠號碼。                                                                              | 2215                 | HTTP 和 RPC proxy 伺服器名稱，HttpConnection 選項 |
| [ncadg \_ ip \_ udp](/windows/desktop/Midl/ncadg-ip-udp)     | 網際網路埠號碼。                                                                              | 1025                 | 無                                                   |
| [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)            | 介於1到65535之間的整數。                                                                       | 5000                 | 無                                                   |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | 指定應用程式或服務名稱的字串。 字串不能包含任何反斜線字元。 | 我的 \_ 印表機          | 安全性                                               |



 

Ncacn HTTP 通訊協定序列支援的 **HttpConnectionOption** 選項名稱 \_ 會採用下列值。



| 選項名稱       | 值            |
|-------------------|------------------|
| HttpConnectOption | **UseHttpProxy** |



 

**HttpConnectionOption** 可讓您在進行 HTTP 連線時，指示 RPC s 的行為。 **UseHttpProxy** 值會指示 RPC 隨時透過 Http proxy 路由傳送流量，包括當用戶端的網際網路選項設定在 Internet Explorer 中，以略過本機位址的 proxy 伺服器。  此選項會指示用戶端透過 Http proxy 強制連接至 RPC proxy。 這可加速建立連接的時間，因為它會略過在使用 HTTP proxy 之前，直接搜尋 RPC 伺服器的任何延遲。

如果使用此 **HttpConnectionOption** 選項，且用戶端上的 Internet Explorer 未設定為使用該 Http proxy，則連線可能會失敗，並出現 **RPC \_ S 不正確 \_ \_ 網路 \_ 選項**。

``` syntax
HttpConnectOption=UseHttpProxy
```

如需 **HttpConnectionOption** 的詳細資訊，請參閱 [使用 HTTP 做為 RPC 傳輸](using-http-as-an-rpc-transport.md)。

Ncalrpc  、ncacn \_ np、ncadg \_ ip \_ udp 和 ncadg ipx 通訊協定序列支援的安全性選項名稱 \_ 會採用下列選項值。



| 選項名稱  | 選項值                                                                               |
|--------------|--------------------------------------------------------------------------------------------|
| **安全性** | {識別 \| 匿名模擬 \| } {動態 \| 靜態} {**true** \| **false**} |



 

如果指定了安全性選項名稱，也必須提供每個安全性選項值集合中的一個專案。 選項值必須以單一空白字元分隔。 例如，下列 *選項* 欄位有效：

``` syntax
Security=identification dynamic true
Security=impersonation static true
```

安全性選項值具有下列意義。



| 安全性選項值 | Description                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 匿名             | 用戶端對伺服器而言是匿名。                                                                                                                                                                                                                                                                                                                   |
| 動態               | 當伺服器使用傳輸安全性時，伺服器會看到用戶端安全性識別中的變更。 這是 LRPC (ncalrpc) 傳輸層級安全性，以及區域具名管道 (ncacn \_ np) 傳輸層級安全性的預設模式。                                                                                                             |
| **False**             | 有效 = **FALSE**;所有的權杖許可權設定（包括設定為 OFF 的設定）都會包含在伺服器上的權杖中，而且可由伺服器啟用。 許可權僅與相同電腦 RPC 呼叫相關。                                                                                                                                     |
| **識別**    | 伺服器具有用戶端的相關資訊，但無法模擬。                                                                                                                                                                                                                                                                                      |
| **模擬**     | 伺服器可在本機系統內代表用戶端執行動作 (傳輸層級安全性不支援委派) 。                                                                                                                                                                                                                               |
| **靜態**            | 當伺服器使用傳輸安全性時，伺服器不會看到用戶端安全性識別中的變更。 這是遠端具名管道唯一可用的模式 (ncacn \_ np) 傳輸層級安全性。 呼叫端的身分識別會在該系結控制碼上的第一個遠端程序呼叫期間儲存，而不是在建立系結控制碼時儲存。 |
| **True**              | 有效 = **TRUE**;只有設定為 ON 的權杖許可權設定才會包含在伺服器的權杖中。 如果使用此選項，伺服器便無法開啟設定為 OFF 的許可權。 許可權僅與相同電腦 RPC 呼叫相關。                                                                                                         |



 

如需安全性選項的詳細資訊，請閱讀 [安全性](security.md)。

</dd> </dl>

## <a name="remarks"></a>備註

除了 *Option* 語法所要求的位置之外，字串系結中不允許空白字元。 [ *Networkaddress.cache.ttl*]、[ *端點*] 和 [ *選項* ] 欄位的預設設定會根據 *ProtocolSequence* 成員的值而不同。

針對所有字串系結欄位，會將單一反斜線字元 (\) 解釋為一個 escape 字元。 若要指定單一常值反斜線字元，您必須 (提供兩個反斜線字元 \\ \) 。

字串系結包含系結控制碼的字元標記法，以及有時候系結控制碼的部分。 字串系結很方便表示系結控制碼的部分，但無法用於進行遠端程序呼叫。 您必須先呼叫 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)，將它們轉換成系結控制碼。

此外，字串系結不包含系結控制碼的所有資訊。 例如，與系結控制碼相關聯的驗證資訊（如果有的話）不會轉譯成呼叫 [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)所傳回的字串系結。

在分散式應用程式的開發過程中，伺服器可以使用字串系結將其系結資訊傳達給用戶端，以建立用戶端伺服器關聯性，而不需要使用端點對應資料庫或名稱服務資料庫。 若要建立這類關聯性，請使用函數 [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) ，將一個或多個系結控制碼向量的系結控制碼轉換成字串系結，並提供字串系結給用戶端。

## <a name="examples"></a>範例

以下是有效字串系結的範例。 在這些範例中，會使用 *obj uuid* 以方便表示字串格式的有效 uuid。 這些範例不會顯示 UUID 308FB580-1EB2-11CA-923B-08002B1075A7，而是顯示 *obj uuid*。

``` syntax
obj-uuid@ncadg_mq:mymqserver
obj-uuid@ncacn_http:major7.microsoft.com[2225]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80,HttpConnectOption=UseHttpProxy]
obj-uuid@ncacn_ip_tcp:16.20.16.27[2001]
obj-uuid@ncacn_ip_tcp:16.20.16.27[endpoint=2001]
obj-uuid@ncacn_nb_nb:
obj-uuid@ncacn_nb_nb:[100]
obj-uuid@ncacn_np:
obj-uuid@ncacn_np:[\\pipe\\p3,Security=impersonation static true]
obj-uuid@ncacn_np:\\\\marketing[\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\marketing[endpoint=\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\sales
obj-uuid@ncacn_np:\\\\sales[\\pipe\\p1,Security=identification dynamic true]
obj-uuid@ncalrpc:
obj-uuid@ncalrpc:[object1_name_demonstrating_that_these_can_be_lengthy]
obj-uuid@ncalrpc:[object2_name,Security=anonymous static true]
obj-uuid@ncacn_vns_spp:server@group@org[500]
obj-uuid@ncacn_dnet_nsp:took[elf_server]
obj-uuid@ncacn_dnet_nsp:took[endpoint=elf_server]
obj-uuid@ncadg_ip_udp:128.10.2.30
obj-uuid@ncadg_ip_udp:maryos.microsoft.com[1025]
obj-uuid@ncadg_ipx: ~0000000108002B30612C[5000]
obj-uuid@ncadg_ipx:printserver
obj-uuid@ncacn_spx:annaw[4390]
obj-uuid@ncacn_spx:~0000000108002B30612C
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)
</dt> <dt>

[**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)
</dt> <dt>

[使用 HTTP 做為 RPC 傳輸](using-http-as-an-rpc-transport.md)
</dt> </dl>

 

