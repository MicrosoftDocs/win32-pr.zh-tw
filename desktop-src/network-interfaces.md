---
description: 本主題說明 Windows 上的高階網路介面概念，包括可在程式碼中識別它們的方式，以及它們的屬性。
ms.assetid: CB01B5ED-C9DB-410B-8C98-E30D9A680847
title: 網路介面
ms.topic: article
ms.date: 06/29/2018
ms.openlocfilehash: d74c875b579a34464190ca039e0176b8c01bef671b0ea6c24581023a49988645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825451"
---
# <a name="network-interfaces"></a>網路介面

本主題說明 Windows 上的高階網路介面概念，包括可在程式碼中識別它們的方式，以及它們的屬性。 

> [!IMPORTANT]
> 本主題適用于開發人員物件，適用于 Windows 桌面網路應用程式和核心模式網路驅動程式。 不過，這裡提供的部分資訊也有助於系統管理員透過 PowerShell Cmdlet 管理網路介面。

## <a name="overview"></a>概觀

*網路介面* 是兩個網路設備或通訊協定層連接的點。 一般來說，這是以實體網路介面卡來代表電腦與私人或公用網路之間的連接 (NIC) 。 不過，它也可以採用僅軟體元件的形式，例如 `127.0.0.1` IPv4 或 IPv6) 的回送介面 (`::1` 。

網路介面是由網際網路工程任務推動小組 (IETF) 在[RFC 2863](https://tools.ietf.org/html/rfc2863)中定義，而不是由 Windows 所定義。 如需有關網路介面識別碼（例如 **ifIndex**）意義的詳細問題，請參閱 IETF 的定義。 本主題的其餘部分將討論 Windows 特定的實作為詳細資料。

## <a name="network-interface-identifiers-and-properties"></a>網路介面識別碼和屬性

在 Windows 上，您可以使用不同的方式來識別網路介面。 其中有些識別碼是用來區別彼此之間的網路介面，但並非所有識別碼都同樣適用于該工作，因為它們有不同的屬性。 一般而言，網路介面會由網路位址識別為外部元件。 例如，這可能是節點識別碼和埠號碼，或只是唯一的節點識別碼。 

在程式碼中，您可以透過許多方式來識別網路介面。 下表詳細說明網路介面的識別方式以及相關聯的屬性。 除非特定 API 需要不同的網路介面識別碼，否則建議使用介面 GUID (**ifGuid**) 進行程式設計。

> [!NOTE]
> 在下表中，以 **粗體** 顯示的儲存格代表網路程式設計人員所需的屬性。

| 識別碼 | 大小 | 在系統上是唯一的 | 在世界上是唯一的 | 為可預測 | 移除 NIC 時將會回收 | 在重新開機時持續保存 | 終端使用者可以隨時修改 | 驅動程式可以隨時修改 | 一般熟悉終端使用者 | 一律存在 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **ifIndex** | **4 個位元組** | **是** | 否 | 否 | 是 | 無<sup>1</sup> | **否** | **否** | **部分**<sup>2</sup> | **是** |
| **NetLuid** | **8 個位元組** | **是** | 否 | 否 | 是 | **是** | **否** | **否** | 否 | **是** |
| **ifGuid** | **16位元組** | **是** | **通常** 為 <sup>3</sup> | No | **否** | **是** | **否** | **否** | 否 | **是** |
| **ifAlias** | 514位元組 | **是適用于 nic**<sup>4</sup> | No | 有時為<sup>5</sup> | 是 | **是** | 是 | **否** | **是** | **通常是**<sup>4</sup> |
| **ifDescr** | 514位元組 | 通常為<sup>6</sup> | 否 | 否 | 是 | **是** | **否** | 是 | **是** | **通常** |
| **ifPhysAddress (MAC 位址)**| 0到32位元組 | 通常是針對 Nic | **通常是針對 Nic** | **是** | **系結至硬體** | **是** | **否** | **否** | **是** | **通常** 為 <sup>7</sup> |
| **PnP 實例識別碼** | 最多400個位元組 | **是** | 否 | 否 | 是 | **是** | **否** | **否** | No | **通常是針對 nic**<sup>8</sup> |
| **(PCI 插槽號碼) 的 PnP 位置** | 最多400個位元組 | **是** | 否 | **是** | 是 | **是** | **否** | **否** | 有時 | 有時是<sup>8、9</sup> |

上表的附注：

1. **IfIndexes** 不保證會在重新開機時穩定穩定，即使它們通常會收到與先前開機相同的值。 因此，不建議驅動程式使用 **ifIndex** ，除非 API 需要的位置。
2. 有些 `netsh` 命令會採用 `ifIndex` 或 `index` 作為輸入。 因此，某些系統管理使用者很熟悉 **ifIndex** 屬性（如果 `netsh` 經常使用命令）。
3. 如果電腦已複製或映射，則某些 Guid 可能會相同。 此外，某些特殊的網路介面（例如內建的 Teredo 介面）在所有機器上可能會有相同的 GUID。
4. NetCfg 強制 **ifAlias** 為非空白字串，且在所有 nic 之間是唯一的。 不過，NDIS 介面提供者不會。 因此，您可以找到具有重複或空白名稱的特殊網路介面。 這是 LBFO 團隊最常看到的。
5. 只有當固件支援一致的裝置命名時。 Typcically，伺服器具有這項功能。
6. NetCfg 會將唯一的 **ifDescrs** 指派給所有網路介面。 不過，驅動程式可以呼叫 API 將 **ifDescr** 變更為任何內容，包括非唯一的內容。 有些協力廠商軟體套件會這樣做。
7. 並非所有媒體類型都有「MAC 位址」。 例如，某些通道沒有這個概念，而且只會通告零長度的位元組陣列作為其網路位址。
8. 只存在於 PnP 裝置所支援的網路介面上。 例如，回送介面、輕量篩選介面、NDIS 介面提供者所提供的介面，以及某些特殊的內建 Nic 都沒有支援的 PnP 裝置。
9. 只有一些 PnP 匯流排支援 PnP 位置識別碼。 內建的 PCI 和 USB 匯流排會進行，而根目錄列舉的裝置則不會。

## <a name="visibility-to-developers"></a>開發人員可見度

在上表中，使用者模式傳統型應用程式和核心模式驅動程式除了隨插即用 (PnP) 屬性以外的所有屬性都可透過共用標頭 (Netioapi) 。 PnP 屬性是透過 Devpkey 標頭可見的，並且由使用者模式桌面應用程式和核心模式驅動程式使用。 例如，請參閱 [DEVPKEY](/windows-hardware/drivers/install/devpkey-device-instanceid) 檔。

[IP Helper](/windows/desktop/IpHlp/ip-helper-start-page) API 也適用于使用者模式傳統型應用程式和核心模式驅動程式。

UWP API 介面只會直接公開 [ifGuid](/uwp/api/windows.networking.connectivity.networkadapter.networkadapterid) 屬性。 不過，UWP 應用程式開發人員可以使用 P/Invoke 匯入 [**GetIfTable2**](/windows/desktop/api/netioapi/nf-netioapi-getiftable2) 函式（如果需要這些函式來存取其他網路介面屬性）。

## <a name="related-topics"></a>相關主題

如需管理資訊基礎 (MIB) 網路介面的定義，請參閱 [RFC 2863](https://tools.ietf.org/html/rfc2863)。

如需網路驅動程式中的 NDIS 網路介面，請參閱 [Ndis 網路介面](/windows-hardware/drivers/network/ndis-network-interfaces2)。

如需 Netioapi 的 API 參考，請參閱 [Netioapi. h 標頭](/windows/desktop/api/netioapi/)。
