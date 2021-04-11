---
description: 所有 IPv6 設定都是使用 Ipv6.exe 工具來完成。
ms.assetid: cb701070-cb7f-472a-97c7-1de9c0ddec0f
title: Ipv6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e6fb0266609d22116cc72151e0db26006c415a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191334"
---
# <a name="ipv6exe"></a>Ipv6.exe

所有 IPv6 設定都是使用 Ipv6.exe 工具來完成。 此工具主要用於查詢和設定 IPv6 介面、位址、快取和路由。 以下是 IPv6 子命令：

<dl> <dt>

<span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**ipv6 if** \[如果\#\]
</dt> <dd>

顯示介面的相關資訊。 如果指定了介面編號，則只會顯示該介面的相關資訊。 否則，就會顯示所有介面的相關資訊。 輸出會包含介面的連結層位址和指派給介面的 IPv6 地址清單，包括介面目前的 MTU，以及介面可支援的 (true) MTU 的最大值。

介面 \# 1 是用於回送的虛擬介面。 介面 \# 2 是用於設定通道、自動通道和6to4 通道的虛擬介面。 其他介面會依照建立的順序依序編號。 此順序會因一部電腦而異。

*Aa* - *bb* - *cc* - *dd* - *ee* - *ff* 格式的連結層位址是乙太網路位址。 中 *的* 連結層位址。*b.**c.**d* 形式為6個以上的介面。 如需 6-4 以上的詳細資訊，請參閱 RFC 2529。

這兩個虛擬介面不會使用 IPv6 鄰居探索。

</dd> <dt>

<span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**ipv6 ifc** 如果 \# \[ 轉送轉送 \] \[ \] \[ -轉送 \] \[ 的 \] \[ mtu \# 位元組 \] \[ 網站識別碼\]
</dt> <dd>

控制介面屬性。 介面可以轉送，在這種情況下，它們會轉送具有未指派給介面之目的地位址的封包。 介面可以是廣告，在這種情況下，它們會傳送路由器通告。 這些屬性可以獨立控制。 介面會傳送路由器請求並接收路由器通告，或接收路由器請求並傳送路由器通告。

因為這兩個虛擬介面不使用鄰近探索，所以無法將其設定為傳送路由器通告。

轉寄可以縮寫為 forw，並公告為進階。

介面的 MTU 也可以設定。 如果) 和大於或等於最小的 IPv6 MTU (1280 個位元組) ，則新的 MTU 必須小於或等於連結的最大 (true) MTU (（依 ipv6 回報）。

您也可以變更介面的網站識別碼。 網站識別碼會用於 sin6 \_ 範圍 \_ 識別碼欄位中，並具有網站本機位址。

</dd> <dt>

<span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**ipv6 ifd** if\#
</dt> <dd>

刪除介面。 無法刪除回送和通道虛擬介面。

</dd> <dt>

<span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**ipv6 nc** \[如果 \# \[ 位址\]\]
</dt> <dd>

顯示鄰近快取的內容。 如果指定了介面編號，則只會顯示該介面的相鄰快取內容。 否則，會顯示所有介面的相鄰快取內容。 如果指定了介面，則可以指定 IPv6 位址，只顯示該鄰近快取專案。

針對每個鄰近的快取專案，會顯示介面、IPv6 位址、連結層位址和觸達狀態。

</dd> <dt>

<span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**ipv6 ncf** \[如果 \# \[ 位址\]\]
</dt> <dd>

清除指定的鄰近快取專案。 只會清除沒有參考的鄰近快取專案。 由於路由快取專案會保留鄰近快取專案的參考，因此應該先清除路由快取。 路由表專案也可以保留鄰近快取專案的參考。

</dd> <dt>

<span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**ipv6 rc** \[如果 \# 位址\]
</dt> <dd>

顯示路由快取的內容。 路由快取是目的地快取的 Microsoft IPv6 實作為名稱。 如果指定了介面和位址，則會顯示透過介面到達位址的路由快取專案。 否則，會顯示所有的路由快取專案。

針對每個路由快取專案，會顯示 IPv6 位址和目前的下一個躍點介面和鄰近位址。 與此目的地搭配使用的慣用來源位址、透過介面到達此目的地的目前路徑 MTU，以及判斷這是否為特定介面–路由快取專案也會顯示。 任何針對目的地位址的行動性) 的轉交位址 (也會一併顯示。

目的地位址可以有多個路由快取專案，最多可有一個用於每個輸出介面。 不過，目的地位址最多可有一個不是介面特定的路由快取專案。 只有在應用程式明確指定該連出介面時，才會使用特定的介面-路由快取專案。

</dd> <dt>

<span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**ipv6 rcf** \[如果 \# \[ 位址\]\]
</dt> <dd>

清除指定的路由快取專案。

</dd> <dt>

<span id="ipv6_bc"></span><span id="IPV6_BC"></span>**ipv6 bc**
</dt> <dd>

顯示系結快取的內容，其保存家用位址與行動 IPv6 的轉交位址之間的系結。

針對每個系結，會顯示首頁位址、轉交位址、系結序號和存留期。

</dd> <dt>

<span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**ipv6 adu** if \# /address \[ 存留期 VL \[ /PL \] \] \[ 任意傳播 \] \[ 單播\]
</dt> <dd>

在介面上新增或移除單播或任意傳播位址指派。 除非指定了任意傳播，否則會對單播位址採取動作。

如果未指定，則存留期為無限。 如果只指定有效的存留期，則慣用的存留期等於有效的存留期。 您可以指定無限期的存留期，或以秒為單位的有限值。 慣用的存留期必須小於或等於有效的存留期。 指定零的存留期會導致移除位址。

您可以縮寫存留期的存留期。

針對任意傳播位址，唯一有效的存留期值為零和無限。

</dd> <dt>

<span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**ipv6 spt**
</dt> <dd>

顯示網站首碼表的目前內容。

針對每個網站首碼，此命令會顯示首碼、網站首碼套用的介面，以及首碼存留期（以秒為單位）。

網站首碼通常是從路由器公告自動設定的。 在 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函式中，會使用它們來篩選不當的網站-本機位址。

</dd> <dt>

<span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>**ipv6 spu** 首碼（如果 \# \[ 存留期為 L）\]
</dt> <dd>

新增、移除或更新網站首碼資料表中的前置詞。

前置詞和介面編號是必要的。 如果未指定，網站首碼存留期（以秒為單位指定）預設為無限。 指定零的存留期會刪除網站首碼。

主機或路由器的一般設定不需要此命令。

</dd> <dt>

<span id="ipv6_rt"></span><span id="IPV6_RT"></span>**ipv6 rt**
</dt> <dd>

顯示路由表的目前內容。

針對每個路由表專案，此命令會顯示路由前置詞、內部連結介面或介面上的下個躍點相鄰、偏好值 (較小的) 和存留期（以秒為單位）。

路由表專案也可以有 **發行** 和 **過時** 屬性。 根據預設，他們會存留存留期 (存留期，而不是剩餘的常數) ，也不會發佈 (用來建立) 的路由器公告。

在主機上，路由表專案通常會從路由器公告自動設定。

</dd> <dt>

<span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>**ipv6 rtu** 首碼 \# \[ （如果/nexthop \] \[ 存留期 L \] \[ 喜好設定 P \] \[ 發佈 \] \[ age） \] \[ spl 網站-首碼-長度\]
</dt> <dd>

新增或移除路由表中的路由。 需要路由前置詞。 前置詞可以連結至指定的介面（或下一個躍點），並以介面上的鄰近位址指定。 路由可以有以秒為單位的存留期（預設為無限）和喜好設定，預設值為零或最慣用。 指定零的存留期會刪除路由。

如果路由是指定為已發佈的，表示它將用於建立路由器公告，則不會存在。 路由的存留期不會進行計數，因此實際上是無限的，但此值是在路由器公告中使用。 您可以選擇性地將路由指定為已發佈的路由，也就是年齡。 依預設，nonpublished 路由一律為年齡。

選擇性的 spl 子選項可以用來指定與路由相關聯的網站前置長度。 只有在傳送路由器公告時，才會使用網站前置長度。

存留期可以縮寫為 life、喜好設定為 pref，然後發佈為 pub。

</dd> </dl>

 

 



