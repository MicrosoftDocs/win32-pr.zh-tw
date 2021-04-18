---
description: IPV6 \_ 保護 \_ 等級通訊端選項可讓開發人員在 ipv6 通訊端上放置存取限制。
ms.assetid: bfb934b3-1e86-431f-a21c-880048d32d35
title: IPV6_PROTECTION_LEVEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2a8dd70bb1fb5b21f74f8939f11da0d9e2a3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971397"
---
# <a name="ipv6_protection_level"></a>IPV6 \_ 保護 \_ 層級

IPV6 \_ 保護 \_ 等級通訊端選項可讓開發人員在 ipv6 通訊端上放置存取限制。 這類限制可以讓應用程式在私人 LAN 上執行，簡便又穩當地強化應用程式對外部攻擊的抵禦。 IPV6 \_ 保護 \_ 等級通訊端選項可擴大或縮小接聽通訊端的範圍，並在適當時啟用不受限制的公用和私用使用者存取，或僅視需要限制對相同網站的存取。

IPV6 \_ 保護 \_ 等級目前有三個已定義的保護層級。



| 保護等級                                                                                                                                 | 描述                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>不 \_ 受限制的保護層級 \_<br/>       | 由設計用來在網際網路上運作的應用程式所使用，包括利用 Windows (Teredo 內建的 IPv6 NAT 遍歷功能的應用程式，例如) 。 這些應用程式可能會略過 IPv4 防火牆，因此必須加強應用程式，以抵禦在開啟的通訊埠位置遭受的直接網路攻擊。<br/> |
| <span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>保護 \_ 層級 \_ EDGERESTRICTED<br/> | 由設計來在網際網路上操作的應用程式使用。 此設定不允許使用 Windows Teredo 執行的 NAT 遍歷。 這些應用程式可能會略過 IPv4 防火牆，因此必須加強應用程式，以抵禦在開啟的通訊埠位置遭受的直接網路攻擊。<br/>                                   |
| <span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>\_ \_ 受限制的保護等級<br/>             | 由未執行網際網路案例的內部網路應用程式所使用。 這些應用程式通常不會就網路攻擊測試進行測試或是採取強化。<br/> 這個設定會將接收傳輸限制於僅連結和本機之間。<br/>                                                                             |



 

下列程式碼範例會提供每個的定義值：

``` syntax
#define PROTECTION_LEVEL_UNRESTRICTED   10  /* for peer-to-peer apps */
#define PROTECTION_LEVEL_EDGERESTRICTED 20  /* Same as unrestricted, except for Teredo  */
#define PROTECTION_LEVEL_RESTRICTED     30  /* for Intranet apps     */
```

這些值是互斥的，無法在單一 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式呼叫中結合。 此通訊端選項的其他值是保留的。 這些保護層級只適用于連入連線。 設定這個通訊端選項對輸出封包或連接沒有任何作用。

在 Windows 7 和 Windows Server 2008 R2 上，未指定 IPV6 保護層級的預設值， \_ \_ 且 **保護 \_ 等級 \_ 預設** 值定義為-1，這是 IPV6 \_ 保護層級的不合法值 \_ 。

在 Windows Vista 和 Windows Server 2008 上，IPV6 \_ 保護層級的預設值 \_ 是不 **\_ \_ 受保護的保護層** 級，而 **保護 \_ 等級 \_ 預設** 值定義為-1，這是 IPV6 \_ 保護層級的不合法值 \_ 。

在 Windows Server 2003 和 Windows XP 上，IPV6 \_ 保護層級的預設值 \_ 為 **保護 \_ 層級 \_ EDGERESTRICTED** ，而 **保護 \_ 等級 \_ 預設** 值定義為 **保護 \_ 層級 \_ EDGERESTRICTED**。

> [!Note]  
> 在系 \_ \_ 結器之前，應設定 IPV6 保護等級通訊端選項。 否則，在 [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) 和 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 呼叫之間收到的封包會符合 **保護 \_ 層級 \_ EDGERESTRICTED**，並且可傳遞至應用程式。

 

下表說明將每個保護等級套用至接聽通訊端的效果。

保護等級

允許連入流量

相同網站

外部

 (Teredo) 的 NAT 遍歷

\_ \_ 受限制的保護等級

是

否

否

保護 \_ 層級 \_ EDGERESTRICTED

是

是

否

不 \_ 受限制的保護層級 \_

是

是

是



 

在上表中， **相同的網站** 資料行是下列各項的組合：

-   連結本機位址
-   網站本機位址
-   已知屬於相同網站的全域位址 (符合網站首碼資料表) 

在 Windows 7 和 Windows Server 2008 R2 上，未 \_ 指定 IPV6 保護層級的預設值 \_ 。 如果本機電腦上沒有安裝 edge 遍歷感知防火牆軟體 (Windows 防火牆已停用，或已安裝其他會忽略 Teredo 流量) 的防火牆，則只有在您將 [IPV6 \_ 保護 \_ 等級通訊端] 選項設定為 [不 **\_ \_ 受保護的保護等級**] 時，才會收到 Teredo 流量。 不過，Windows 防火牆或任何邊緣遍歷感知防火牆原則可能會根據防火牆的原則設定來忽略此選項。 藉由將此通訊端選項設定為不 **\_ \_ 受限制的保護層級**，應用程式就會傳達其明確意圖，以接收在本機電腦上安裝的主機防火牆的邊緣流量。 因此，如果已安裝 edge 遍歷感知主機防火牆，它就會有接受封包的最後決定。 依預設，不會設定任何通訊端選項：

-   o 如果已啟用 Windows 防火牆 (或在本機電腦上安裝了另一個邊緣進行感知的主機防火牆) ，則會觀察到它所強制執行的任何內容。 一般邊緣遍歷感知主機防火牆預設會封鎖 Teredo 流量。 因此，應用程式會觀察到預設值，就像是 **保護 \_ 層級 \_ EDGERESTRICTED** 一樣。
-   o 如果未啟用 Windows 防火牆，且本機系統上未安裝任何其他邊緣遍歷感知主機防火牆，則預設值將會是 **保護 \_ 層級 \_ EDGERESTRICTED**。

在 Windows Vista 和 Windows Server 2008 上，IPV6 \_ 保護層級的預設值 \_ 是不 **\_ \_ 受保護的保護層** 級。 但有效的值取決於是否已啟用 Windows 防火牆。 無論為 IPV6 保護層級設定的值為何，Windows 防火牆都可感知邊緣對 (Teredo 感知) \_ ， \_ 而且如果 ipv6 \_ 保護 \_ 層級不 **\_ \_ 受保護**，則會忽略。 因此有效的值取決於防火牆原則。 當停用 Windows 防火牆，且本機電腦上未安裝任何其他邊緣遍歷感知防火牆時，IPV6 \_ 保護層級的預設值 \_ 會是不 **\_ \_ 受限制的保護層級**。

在 Windows Server 2003 和 Windows XP 上，IPV6 \_ 保護層級的預設值 \_ 為 **保護 \_ 層級 \_ EDGERESTRICTED**。 除非您已將 IPV6 \_ 保護 \_ 等級通訊端選項設定為不 **\_ \_ 受限制的保護層級**，否則您不會收到任何 Teredo 流量。

視 IPV6 \_ 保護 \_ 等級而定，需要來自網際網路的未經要求流量的應用程式可能無法接收未經要求的流量。 不過，透過 Windows Teredo 介面接收要求的流量並不需要這些需求。 如需與 Teredo 互動的詳細資訊，請參閱透過 [Teredo 接收請求的流量](../teredo/receiving-solicited-traffic-over-teredo.md)。

當連入封包或連線因為設定保護層級而遭到拒絕時，將會以不是任何應用程式在該通訊端上接聽的方式來處理拒絕。

> [!Note]
>
> IPV6 \_ 保護 \_ 等級通訊端選項不一定會在 ipv6 通訊端上放置存取限制，也不一定會使用 Windows Teredo 以外的某種方法來限制 NAT 的存取，或甚至是其他廠商使用其他的 Teredo 執行。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[透過 Teredo 接收請求的流量](../teredo/receiving-solicited-traffic-over-teredo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
