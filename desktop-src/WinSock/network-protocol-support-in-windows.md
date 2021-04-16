---
description: 網際網路通訊協定套件是商業網路和網際網路上所使用的主要網路通訊協定。
ms.assetid: 8c123e09-b11a-4c92-b41e-49cc01be53d3
title: Windows 中的 Winsock 網路通訊協定支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36da53101dda06426a04e5f910b4548273e8ab47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469049"
---
# <a name="winsock-network-protocol-support-in-windows"></a>Windows 中的 Winsock 網路通訊協定支援

網際網路通訊協定套件是商業網路和網際網路上所使用的主要網路通訊協定。 網際網路通訊協定套件代表大型的分層網路通訊協定集合。 網際網路通訊協定套件通常是以套件中包含的兩個最重要的通訊協定為基礎，稱為 TCP/IP：網際網路通訊協定 (IP) 和傳輸控制通訊協定 (TCP) 。

IPv6 和 IPv4 代表網際網路通訊協定的兩個可用版本。 TCP 是數個重要網路服務的其中一種，通常稱為 IP 通訊協定，可透過 IPv6 和 IPv4 網路運作。 使用者資料包協定 (UDP) 和網際網路控制訊息通訊協定 (ICMP) 是其他透過 IPv6 和 IPv4 網路使用的重要 IP 通訊協定。 有一些其他 IP 通訊協定可用於 IPv6 和 IPv4 網路。

Windows 通訊端會將每個網路通訊協定套件視為唯一的位址系列。 因此，IPv6 通訊協定被視為 **af \_ INET6** 位址家族，而 IPv4 通訊協定則視為 **af \_ INET** 位址系列。 IPv6 和 IPv4 通訊協定支援使用各種分層式 IP 通訊協定，例如 TCP、UDP 和 ICMP。

Windows 通訊端一開始是設計來將 IPv4 的支援新增至 Windows。 不過，Windows 通訊端程式設計介面是設計自驗證，而且能夠支援其他網路通訊協定套件。 經過一段時間之後，Windows 的版本和相關聯的 Windows 通訊端已包含其他網路通訊協定套件的原生支援 (IPX/SPX 和 AppleTalk，例如) 。 其他網路通訊協定的支援也適用于 Windows 版本，作為廠商提供的協力廠商軟體。

在網際網路的成長和熱門程度之前，會在網路環境中使用各種其他網路通訊協定套件，特別是針對本機內部網路。 網路通訊協定套件的選擇通常是根據網路大小或 IT 網路人員的專業知識。 由於現今的全球網際網路連線能力，即使是最小的網路，也能連結到全球各地的網路專業人員。 如此一來，其他先前重要的網路通訊協定套件現在會以非常有限的方式使用，並已成為排除。 這些排除網路通訊協定套件的原生支援（通常稱為傳統網路通訊協定）已從最新版本的 Microsoft Windows 中卸載。 其中某些舊版通訊協定的支援，可能會以廠商的協力廠商軟體的形式提供， (具有 ATM 網路硬體的 ATM，例如) 。

下表識別一般網路通訊協定套件的原生 Windows 支援。 

| 網路通訊協定                 | Windows 7                | Windows Server 2008      | Windows Vista            | Windows Server 2003                  | Windows XP                           | Windows 2000                         |
|----------------------------------|--------------------------|--------------------------|--------------------------|--------------------------------------|--------------------------------------|--------------------------------------|
| IPv6<br/>                  | 支援<br/>     | 支援<br/>     | 支援<br/>     | 支援<br/>                 | 支援<br/>                 | 不支援 (請參閱附注) <br/> |
| IPv4<br/>                  | 支援<br/>     | 支援<br/>     | 支援<br/>     | 支援<br/>                 | 支援<br/>                 | 支援<br/>                 |
| NetBIOS (查看附注)  <br/>  | 支援<br/>     | 支援<br/>     | 支援<br/>     | 支援<br/>                 | 支援<br/>                 | 支援<br/>                 |
| IrDA (查看附注) <br/>      | 支援<br/>     | 支援<br/>     | 支援<br/>     | 支援<br/>                 | 支援<br/>                 | 支援<br/>                 |
| 藍牙 (查看附注) <br/> | 支援<br/>     | 支援<br/>     | 支援<br/>     | 支援<br/>                 | 支援<br/>                 | 不支援<br/>             |
| IPX/SPX<br/>               | 不支援<br/> | 不支援<br/> | 不支援<br/> | 支援<br/>                 | 支援<br/>                 | 支援<br/>                 |
| AppleTalk<br/>             | 不支援<br/> | 不支援<br/> | 不支援<br/> | 支援<br/>                 | 支援<br/>                 | 支援<br/>                 |
| Dlc<br/>                   | 不支援<br/> | 不支援<br/> | 不支援<br/> | 不支援 (請參閱附注) <br/> | 不支援 (請參閱附注) <br/> | 支援<br/>                 |
| ATM<br/>                   | 不支援<br/> | 不支援<br/> | 不支援<br/> | 支援的 (請參閱附注) <br/>     | 支援的 (請參閱附注) <br/>     | 支援的 (請參閱附注) <br/>     |
| NetBEUI<br/>               | 不支援<br/> | 不支援<br/> | 不支援<br/> | 不支援<br/>             | 不支援<br/>             | 支援的 (請參閱附注) <br/>     |



 

**Windows 2000 上的 IPv6：** Windows 2000 （含 Service Pack 1） (SP1) 和更新版本支援 IPv6 通訊協定（含 Windows 2000 的 Microsoft IPv6 技術預覽版）。

**NetBIOS：** NetBIOS 通訊協定通常是由 Windows 上的命名服務所使用。 NetBIOS 可以使用多個網路通訊協定套件，包括 IP (NetBIOS over TCP/IP) 、IPX/SPX 和 NetBEUI。 Winsock 支援 NetBIOS over TCP/IP (通常只會在32位版本的 Windows 7、Windows Server 2008 和 Windows Vista 上呼叫 NetBT) 。 Winsock 支援在 Windows Server 2003 和 Windows XP 上使用 IPX 的 NetBIOS over TCP/IP 和 NetBIOS。 Winsock 支援使用 IPX 的 NetBIOS over TCP/IP、NetBIOS，以及在 Windows 2000 上使用 NetBEUI 的 NetBIOS。

**IrDA：** 如果電腦已安裝紅外線埠和驅動程式，則支援紅外線資料關聯 (IrDA) 通訊協定。

**藍牙：** 針對 Bluetooth 作為網路通訊協定套件的 Winsock 支援包括藍牙個人區域網路 (的行動電話) 和撥號網路 (DUN) 設定檔。 Windows 中的藍牙支援也包括使用藍牙人體介面裝置 (HID) 和其他設定檔，以連接至鍵盤、指向裝置，以及其他與網路通訊協定無關的輸入裝置。

**Windows 2003 和 WINDOWS XP 上的 DLC：** 當安裝 Microsoft Host Integration Server 2006、Host Integration Server 2004 或 Host Integration Server 2000 所含的 DLC 驅動程式時，Windows Server 2003 和 Windows XP 支援 (DLC) 通訊協定的資料連結控制項。

**Windows 2003、WINDOWS XP 及 windows 2000 上的 ATM：** 當安裝 ATM 網路介面卡時，Windows Server 2003、Windows XP 及 Windows 2000 上支援 (ATM) 通訊協定的非同步傳輸模式。 傳統 IP over (ATM 的通訊協定，有時會縮寫為剪輯/ATM) 是在 [RFC 2225](https://tools.ietf.org/html/rfc2225) 中定義，而在 IETF 發行的相關檔中定義。 Windows Server 2003、Windows XP 及 Windows 2000 提供此標準的完整實作為。

**Windows 2000 上的 NetBEUI：** Windows sockets 不直接支援 NetBEUI 通訊協定。 但可使用多個網路通訊協定的 NetBIOS 通訊協定支援在 Windows 2000 上使用 NetBEUI 通訊協定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ATM 技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc759707(v=ws.10))
</dt> <dt>

[Bluetooth](../bluetooth/bluetooth-start-page.md)
</dt> <dt>

[適用于 Windows 2000 的 IPv6 技術預覽](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Irda](/previous-versions/windows/desktop/irda/irda-start-page)
</dt> <dt>

[Windows 中的 NDIS 5.0 和 ATM 支援](/windows-hardware/drivers/network/ndis-version-guide)
</dt> </dl>

 

 
