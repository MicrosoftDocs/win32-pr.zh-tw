---
description: 第一個設定不需要額外的設定，除了安裝 Microsoft IPv6 技術預覽通訊協定之外。
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 設定1：具有連結-本機位址的單一子網
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a541edd96175dc61ec0aba3b1358c2bbd9464668e6aa1a11aeb6f2097e5b13bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051729"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a>設定1：具有連結-本機位址的單一子網

第一個設定不需要額外的設定，除了安裝 Microsoft IPv6 技術預覽通訊協定之外。 這項設定是由相同的子網上至少包含兩個節點所組成。 在 IPv6 術語中，這兩個節點位於沒有中繼路由器的相同連結上。

下圖顯示使用連結-本機位址在單一子網上設定兩個節點的設定。

![使用連結-本機位址的兩個節點。](images/v6mig-1.png)

根據預設，IPv6 會為每個對應到已安裝 Ethernet 網路介面卡的介面設定連結-本機 IP 位址。 連結-本機位址的前置詞為 fe80：：/64。 IPv6 位址的最後64位稱為介面識別碼，並衍生自網路介面卡的48位 MAC 位址。

若要從48位 (6 位元組) 乙太網路 MAC 位址建立 IPv6 介面識別碼：

-   在 MAC 位址的第三個和第四個位元組之間插入十六進位數位 0xff-fe。
-   全域/本地位（MAC 位址的第一個位元組的第二個低序位位）會進行求一。 如果是1，則會變成0，如果是0，則會變成1。

例如，針對 MAC 位址 00-60-08-52-f9-d8：

-   在 0x08 (第三個位元組) 和 0x52 (MAC 位址的第四個位元組) （形成64位位址 00-60-08-ff-fe-52-f9-d8）之間，會插入十六進位數位 0xff-fe。
-   在 MAC 位址的第一個位元組)  (的通用/本地位，0x00 的第二個低序位位。 第二個低序位位為0x00 的是0，而在求時，會變成1。 結果是，如果第一個位元組，0x00 會成為0x02。

因此，對應至 Ethernet MAC 位址 00-60-08-52-f9-d8 的 IPv6 介面識別碼是 02-60-08-ff-fe-52-f9-d8。

節點的連結-本機位址是首碼 fe80：：/64 以及以 IPv6 冒號-十六進位標記法表示的64位介面識別碼的組合。 因此，此範例節點的連結-本機位址的前置詞 fe80：：/64 和介面識別碼 02-60-08-ff-fe-52-f9-d8 是 fe80：：260：8ff： fe52： f9d8。

如下列範例所示，您可以使用 ipv6 來查看連結本機位址：

**ipv6 if**

``` syntax
Interface 4 (site 1): Local Area Connection
  uses Neighbor Discovery
  link-level address: 00-10-5a-aa-20-a2
    preferred address fe80::210:5aff:feaa:20a2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ffaa:20a2, 1 refs, last reporter
  link MTU 1500 (true link MTU 1500)
  current hop limit 128
  reachable time 43500ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 3 (site 1): 6-over-4 Virtual Interface
  uses Neighbor Discovery
  link-level address: 10.0.0.2
    preferred address fe80::a00:2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ff00:2, 1 refs, last reporter
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 34000ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 2 (site 0): Tunnel Pseudo-Interface
  does not use Neighbor Discovery
  link-level address: 0.0.0.0
    preferred address ::10.0.0.2, infinite/infinite
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
Interface 1 (site 0): Loopback Pseudo-Interface
  does not use Neighbor Discovery
  link-level address:
    preferred address ::1, infinite/infinite
  link MTU 1500 (true link MTU 1500)
  current hop limit 1
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
```

介面4是對應至已安裝乙太網路介面卡的介面，其連結-本機位址為 fe80：：210：5aff： feaa：20a2。

如需 IPv6 位址的詳細資訊和 IPv6 概念的總覽，請參閱 IPv6 簡介白皮書。

## <a name="testing-connectivity-between-two-link-local-hosts"></a>測試兩個連結本機主機之間的連線能力

您可以執行簡單的 ping (在兩個連結本機主機之間使用 IPv6) ICMPv6 Echo 要求和回應回復訊息的交換。

**使用 IPv6 在兩個連結本機主機之間進行 ping**

1.  在兩個 Windows 主機上安裝適用于 Windows 的 Microsoft IPv6 技術預覽 (主機 A 和主機 B) 位於相同連結 (子網) 。
2.  在主機 A 上使用 ipv6，以取得乙太網路介面的連結-本機位址。

    範例：主機 A 的連結-本機位址是 fe80：：210：5aff： feaa：20a2。

3.  在主機 B 上使用 ipv6 來取得乙太網路介面的連結-本機位址。

    範例：主機 B 的連結-本機位址是 fe80：：260：97ff： fe02：6ea5。

4.  從主機 A，使用 Ping6.exe ping 主機 B。

    範例： ping6 fe80：：260：97ff： fe02：6ea5

若要指定傳送 Echo 要求訊息的來源位址，您也可以使用 Ping6.exe s 選項。 例如，若要從 fe80：：210：5aff： feaa：20a2 的 IPv6 位址傳送 Echo 要求至主機 B，請使用下列命令：

**fe80：：210：5aff： feaa： 20a2% 4 fe80：：260：97ff： fe02：6ea5**

在 ping 連結本機或網站本機位址時，建議您指定範圍識別碼以明確地讓目的位址。 指定範圍識別碼的標記法是位址% 範圍識別碼。 若為連結-本機位址，範圍識別碼會等於 ipv6 if 命令中顯示的介面編號。 若為網站本機位址，範圍識別碼會等於 ipv6 if 命令中顯示的網站號碼。 例如，若要使用範圍識別碼4將 Echo 要求訊息傳送至主機 B，請使用下列命令：

**ping6 fe80：：260：97ff： fe02： 6ea5% 4**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IPv6 的建議設定](recommended-configurations-2.md)
</dt> </dl>

 

 



