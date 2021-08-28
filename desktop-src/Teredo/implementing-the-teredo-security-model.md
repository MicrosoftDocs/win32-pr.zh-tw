---
title: 執行 Teredo 安全性模型
description: Teredo 安全性模型是以 Windows Vista 內建的 Windows 篩選平台 (WFP) 技術為基礎。 因此，建議協力廠商防火牆使用 WFP 來強制執行 Teredo 安全性模型。
ms.assetid: ee81e5f1-e3e0-440e-a53f-2accced476bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43cad78b7c1512e0f1c632ecd27d0bb9580ac3796d6d36001a1cd19fb72c7b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001746"
---
# <a name="implementing-the-teredo-security-model"></a>執行 Teredo 安全性模型

Teredo 安全性模型是以 Windows Vista 內建的[Windows 篩選平台](/windows/desktop/FWP/windows-filtering-platform-start-page) (WFP) 技術為基礎。 因此，建議協力廠商防火牆使用 WFP 來強制執行 [Teredo](about-teredo.md) 安全性模型。

[Teredo 安全性模型](the-teredo-security-model.md)的一般執行需要下列各項：

-   具備 IPv6 功能的主機防火牆必須向電腦上的 Windows 安全性 Center (WSC) 註冊。 如果沒有以主機為基礎的防火牆或 WSC 本身，Teredo 介面將無法供使用。 這是透過 Teredo 介面接收來自網際網路之要求流量的唯一需求。
-   任何透過 Teredo 介面接收來自網際網路之未經要求流量的應用程式，都必須先向具備 IPv6 功能的防火牆註冊，例如[Windows 防火牆](/previous-versions/windows/desktop/ics/windows-firewall-start-page)，才能接收未受要求的流量。

如果未在 Teredo 介面上傳送或接收流量超過一小時，且符合未要求流量所需安全性準則的應用程式未執行或未開啟接聽通訊端，Teredo 位址將會變成休眠狀態。

在機器重新開機之後，或如果 Teredo 位址失去其資格，Windows Vista 會自動限定位址，並在應用程式系結至支援 IPv6 的通訊端時，讓其可供使用。 務必要注意的是，應用程式所設定的 Windows 防火牆「Edge 遍歷」選項，允許透過 Teredo 的未經要求流量在重新開機時持續存在。

## <a name="firewall-requirements-for-teredo"></a>Teredo 的防火牆需求

防火牆廠商可以輕鬆地在其產品中併入 Teredo 支援，並使用 Windows 篩選平台的功能保護其使用者。 這可以藉由向 Windows 安全性中心註冊具備 IPv6 功能的防火牆、將適當的規則新增至 WFP Teredo 子層，然後使用內建 api 在 Windows 列舉可透過 Teredo 接聽未經要求之流量的應用程式來完成。 在應用程式不需要透過 Teredo 接聽要求流量的情況下，防火牆不需要將其他規則新增至 WFP。 不過，具備 Windows 安全性中心的 IPv6 可用防火牆註冊，仍然需要讓 Teredo 位址可供使用。

為了支援此案例，防火牆必須具備 IPv6 功能，並向 Windows 安全性中心註冊。 此外，防火牆不能變更 Windows 安全性 Center 服務 (wscsvc) 的執行中或啟動狀態，因為 Teredo 相依于透過 WSC api 提供的狀態資訊。

用來向 WSC 註冊防火牆的 API 可透過與 Microsoft 聯絡來取得 wscisv@microsoft.com 。 基於安全性考慮，必須有 (NDA) 的保密合約，才能洩漏此 API。

下列檔詳細說明使用的篩選準則和例外狀況，以確保與 Teredo 的最佳相容性：

-   [執行 Teredo 的防火牆篩選器](implementing-firewall-filters-for-teredo.md)
-   [Teredo 的必要防火牆例外](required-firewall-exceptions-for-teredo.md)
-   [需要 Windows 篩選 Teredo 的平臺例外狀況](required-windows-filtering-platform-exceptions-for-teredo.md)

## <a name="firewall-requirements-for-other-ipv6-transition-technologies"></a>其他 IPv6 轉換技術的防火牆需求

為了支援其他 IPv6 轉換技術 (例如6to4 和 ISATAP) ，主機防火牆產品必須能夠處理 IPv6 流量。 IP 通訊協定41表示 IPv6 標頭在 IPv4 標頭之後。 當主機防火牆遇到通訊協定41時，必須辨識封包是 IPv6 封裝的封包，因此必須適當地處理封包，並根據其原則中的 IPv6 規則進行接受/拒絕決策。

 

 