---
description: 6to4 是一種方法，可透過現有的 IPv4 網際網路基礎結構連接 IPv6 主機或網站。
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: '設定2： IPv4 網路上不同子網的節點之間的 IPv6 流量 (6to4) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1abd5477005e6a1e71c13aaf19a734e9191097d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469061"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a>設定2： IPv4 網路上不同子網的節點之間的 IPv6 流量 (6to4) 

6to4 是一種方法，可透過現有的 IPv4 網際網路基礎結構連接 IPv6 主機或網站。 它會使用唯一的位址前置詞，為隔離的 IPv6 網站提供自己的 IPv6 位址空間。 6to4 就像是提供 IPv6 連線的「虛擬 ISP」。 您可以使用6to4 直接與其他6to4 網站進行通訊。 6to4 不需要使用 IPv6 路由器，其 IPv6 流量會以 IPv4 標頭封裝。

下圖顯示使用6to4 在 IPv4 路由器之間進行通訊的不同子網上，兩個節點的設定。

![使用6to4 在 ipv4 路由器之間通訊的節點。](images/v6mig-2.png)

使用6to4 的主要需求是您網站的一個可全域路由的 IPv4 位址。 假設您的網站是由一組您管理的 IPv6 電腦所組成， (某些執行的 Microsoft IPv6 通訊協定，以及一些執行中的其他 IPv6 執行) 。 也假設所有 IPv6 電腦都是使用乙太網路或6到4來直接連接。 您必須將可全域路由的 IPv4 位址指派給執行 Microsoft IPv6 通訊協定的其中一部電腦。 這部電腦將是您的6to4 閘道。

如果您的 IPv4 位址是私人位址空間的一部分 (10.0.0.0/8、172.16.0.0/12 或 192.168.0.0/16) 或自動私人 IP 位址 (APIPA) 位址空間（由 Windows 2000 使用），則無法全域路由傳送。 否則，它可能是公用 IP 位址，而且可全域路由傳送。 See the [Debugging 6to4 Configuration](#debugging-6to4-configuration) topic in this document for more help in determining whether your ISP connection supports 6to4.

## <a name="the-6to4cfgexe-tool"></a>6to4cfg.exe 工具

6to4cfg.exe 工具會將6to4 設定自動化，自動探索您全域可路由傳送的 IPv4 位址，以及建立6to4 首碼。 它會直接執行設定，也可以撰寫您稍後可以檢查和執行的設定腳本。

基本 6to4cfg.exe 命令語法如下所示。

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span id="_filename_"></span><span id="_FILENAME_"></span>\[*檔案名*\]
</dt> <dd>

如果您指定檔案名，則將設定腳本寫入檔案。 設定腳本會使用 Ipv6.exe。

您可以指定檔案名的 con 將設定腳本寫入主控台輸出，這對於查看測試案例中的 6to4cfg.exe 會有説明。

如果您沒有指定檔案名，6to4cfg.exe 直接更新您電腦上的 IPv6 設定。

</dd> <dt>

<span id="-r"></span><span id="-R"></span>-r
</dt> <dd>

成為區域網路的6to4 閘道路由器，可在您的所有介面和指派的子網首碼上啟用路由。

</dd> <dt>

<span id="-s"></span><span id="-S"></span>-s
</dt> <dd>

在您的6to4 網站中啟用網站本機定址。 此命令只有在搭配-r 使用時才有用。

</dd> <dt>

<span id="-u"></span><span id="-U"></span>-u
</dt> <dd>

指定反轉6to4 設定。 因此，6to4cfg-u 會反轉6to4cfg 和6to4cfg 的效果-r-u 會反轉 6to4cfg-r 的效果，依此類推。

</dd> <dt>

<span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *轉送*
</dt> <dd>

指定6to4 轉送路由器的名稱或 IPv4 位址。 預設名稱是6to4.ipv6.microsoft.com，也就是網際網路上的6to4 轉送路由器。

</dd> <dt>

<span id="-b"></span><span id="-B"></span>-b
</dt> <dd>

指定 6to4cfg.exe 挑選「最佳」轉送位址，而不是第一個位址。

</dd> <dt>

<span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *位址*
</dt> <dd>

指定6to4 首碼的本機 IPv4 位址。

</dd> </dl>

## <a name="manual-6to4-configuration"></a>手動設定6to4

在此範例中，會 172.31.42.239 6to4 閘道的位址。 您需要您專屬可全域路由的 IPv4 位址，才能使用6to4。

> [!Note]  
> IP 位址172.31.42.239 僅供範例之用。 這是私人位址，無法在網際網路上以全球方式路由傳送。

 

32位可全域路由的 IPv4 位址會與16位首碼2002::/16 結合，以形成您網站的48位 IPv6 位址首碼。 在此範例中，6to4 網站首碼是2002： ac1f：2aef：：/48。 請注意，ac1f：2aef 是 172.31.42.239 (的十六進位編碼方式，您將使用不同的前置詞，並根據您專屬可全域路由的 IPv4 位址) 。 您可以使用6to4 網站首碼來指派網站內的位址和子網首碼。

此範例假設您使用子網0手動設定6to4 閘道電腦上的6to4 位址，並使用子網1自動設定 Ethernet 網路區段上的位址。 不過，也可以選擇其他選項。

1.  使用 Ipv6.exe 在您的6to4 閘道電腦上啟用6to4：

    **ipv6 rtu 2002::/16 2**

    **Ipv6 rtu** 命令會執行路由表更新。 可以用來新增、移除或更新路由。 在此情況下，它會啟用6to4。

    2002::/16 引數是路由的前置詞，指定唯一的6to4 前置詞。

    2個引數會指定這個前置詞的內部連結介面。 介面 \# 2 是用於設定通道、自動通道和6to4 的「虛擬介面」。 當 IPv6 目的地位址符合2002::/16 首碼時，會解壓縮目的地位址前置詞後面的32位以形成 IPv4 目的地位址。 封包會以 IPv4 標頭封裝，並傳送至 IPv4 目的地位址。

2.  在您的6to4 閘道電腦上設定6to4 位址：

    **ipv6 adu 2/2002： ac1f：2aef：： ac1f：2aef**

    **Ipv6 adu** 命令會執行位址更新。 可以用來新增、移除或更新介面上的位址。 在此情況下，它會設定電腦的6to4 位址。

    2/2002： ac1f：2aef：： ac1f：2aef 引數同時指定介面和位址。 它需要在介面2上設定 address 2002： ac1f：2aef：： ac1f： 2aef \# 。 位址會使用網站首碼2002： ac1f：2aef：：/48、子網0來提供子網首碼2002： ac1f：2aef：：/64 和64位介面識別碼。 此慣例針對指派給介面2的位址，使用電腦的 IPv4 位址作為介面識別碼 \# 。 針對您的使用，ac1f：2aef 應該由您專屬可全域路由的 IPv4 位址的十六進位編碼來取代。

上述兩個命令足以允許與其他6to4 網站進行通訊。 例如，您可以嘗試 ping Microsoft 6to4 網站：

**ping6 2002：836b：9820：：836b：9820**

若要啟用與6bone 的通訊，您必須建立通往6to4 轉送的預設設定通道。 您可以使用 Microsoft 6to4 轉送路由器131.107.152.32：

**ipv6 rtu：：/0 2/：： 131.107.152.32 pub life 1800**

**Ipv6 rtu** 命令會執行路由表更新，在此實例中建立通往6to4 轉送的預設路由。

：：/0 引數是路由前置詞。 長度為零的前置詞表示它是預設路由。

2/：：131.107.152.32 引數會指定這個前置詞的下一個躍點相鄰。 它需要使用介面2將符合前置詞的封包轉送至位址：： 131.107.152.32 \# 。 在介面2上將封包轉送至：： 131.107.152.32 \# 會導致它以 v4 標頭封裝並傳送至131.107.152.32。

Pub 引數使其成為已發佈的路由。 因為這只與路由器有關，所以在啟用路由之前，它沒有任何作用。 同樣地，30分鐘的存留期僅適用于啟用路由。

您應該能夠存取6bone 網站和6to4 網站。 您可以使用下列命令來測試此項：

**ping6 3ffe：1cff：0： f5：：1**

最後一個步驟是在您的6to4 閘道上啟用路由。 此範例假設 \# 您閘道電腦上的介面3是乙太網路介面，而介面 \# 4 是6到4。 您的電腦可能會以不同的方式來為其介面編號。 下列兩個命令會將子網首碼指派給這兩個連結。 子網首碼衍生自網站的6to4 首碼2002： ac1f：2aef：：/48：

**ipv6 rtu 2002： ac1f：2aef：1：：/64 3 pub life 1800**

**ipv6 rtu 2002： ac1f：2aef：2：：/64 4 pub life 1800**

**Ipv6 rtu** 命令指定首碼2002： ac1f：2aef：1：：/64 是在介面3的連結上 \# 。 它會設定 Ethernet 介面上的第一個子網前置詞。 此路由會在存留期30分鐘內發佈。

同樣地，2002： ac1f：2aef：2：：/64 首碼是在6個以上的介面上進行設定。

接下來的三個命令可讓6to4 閘道電腦以路由器的形式運作：

**ipv6 ifc 2 forw**

**ipv6 ifc 3 forw 進階**

**ipv6 ifc 4 forw 進階**

**Ipv6 ifc** 命令可控制介面的屬性。 路由器會轉送封包並傳送路由器通告。 在 Microsoft IPv6 的執行中，這些每個介面屬性會分開控制。

\#不需要介面2來進行廣告，因為它是虛擬介面。

如果您的電腦有其他介面，也應該將它們設定為轉送和廣告。

執行這些命令之後，Microsoft IPv6 通訊協定會 \# 使用各自的子網首碼在介面3和4上自動設定位址， \# 而這兩個介面會開始傳送路由器公告大約3到10分鐘。

接收這些路由器公告的主機會自動設定預設路由，以及衍生自其連結子網首碼的6to4 位址。 他們會透過閘道電腦與其他6to4 網站和6bone 進行通訊。

## <a name="debugging-6to4-configuration"></a>進行6to4 設定的調試

**若要偵測您的6to4 設定**

1.  檢查 IPv4 與6to4 轉送路由器之間的連線能力：

    **ping 6to4.ipv6.microsoft.com**

    如果失敗，您就不會有全球網際網路連線能力。

2.  使用自動通道檢查 IPv6 封裝：

    **ping6：：131.107.152.32**

    如果失敗，則您的電腦與網際網路之間可能會有防火牆或網路位址轉譯器 (NAT) 。 如果成功，則您的網際網路連接可以支援6to4。

3.  檢查 ipv6 rt 命令的顯示。 您應該會看到 2002::/16-> 2 路由。 檢查 ipv6 的顯示是否為2個命令。 您應該會看到含有2002::/16 前置詞的慣用位址。

> [!Note]  
> 131.107.152.32 的 Microsoft 6to4 轉送路由器的 IPv4 位址可能會變更。 如果上述步驟2無法運作，請在步驟1中檢查 ping 命令的輸出，以確認 Microsoft 6to4 轉送路由器的 IPv4 位址。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IPv6 的建議設定](recommended-configurations-2.md)
</dt> <dt>

[具有連結-本機位址的單一子網](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[在兩個本機連結主機之間使用 IPsec](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



