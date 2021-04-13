---
title: IKE/AuthIP 豁免
description: 網際網路金鑰交換 (IKE) 和已驗證的網際網路通訊協定 (AuthIP) ，為了正常運作，必須從 IPsec 篩選豁免其網路流量。
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58a6d00ddd337d56c3c00a34b6949213be6ee26
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374566"
---
# <a name="ikeauthip-exemptions"></a>IKE/AuthIP 豁免

網際網路通訊協定安全性 (IPsec) 的加密模組、網際網路金鑰交換 (IKE) 和已驗證的網際網路通訊協定 (AuthIP) ，為了能夠運作，必須從 IPsec 篩選豁免網路流量。

在 Windows 篩選平台 (WFP) 基礎篩選引擎 (BFE) 會在新增第一個 IKE 或 AuthIP 主要模式 (MM) 原則篩選器時自動新增 IKE 和 AuthIP 豁免篩選，並在刪除最後一個 IKE 或 AuthIP MM 原則篩選器時將其刪除。 如此一來，原則提供者不需要個別管理 IKE 和 AuthIP 篩選豁免。

IKE MM 原則篩選器是引擎層 [**FWPM \_ 圖層 \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 中的篩選器，可參考 [**FWPM \_ IPSEC \_ IKE \_ MM \_ 內容**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)類型的提供者內容。

AuthIP MM 原則篩選器是引擎層 [**FWPM \_ 圖層 \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 中的篩選器，其參考 [**FWPM \_ IPSEC \_ AuthIP \_ MM \_ 內容**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)類型的提供者內容。

IKE 或 AuthIP 豁免篩選是「引擎層 [**FWPM 圖層內送 \_ \_ \_ 傳輸 \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) 中的篩選準則，或 **FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ v {4 \| 6}** 在 [**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**](filter-weight-identifiers.md) 權數範圍中自動加權。

BFE 所實行的 IKE 和 AuthIP 豁免如下所示。

| IP 版本      | 連接埠                        | 豁免                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPv4<br/> | UDP： 500 UDP：4500<br/> | 允許輸入傳輸層和輸出傳輸層的 IKE 和 AuthIP 流量。 <br/> 在 ALE 接收/接受並連接層級時允許 IKE 和 AuthIP 流量，但會將它限制為本機系統。<br/> |
| IPv6<br/> | UDP：500<br/>          | 允許輸入傳輸層和輸出傳輸層的 IKE 和 AuthIP 流量。 <br/> 在 ALE 接收/接受並連接層級時允許 IKE 和 AuthIP 流量，但會將它限制為本機系統。<br/> |



 

IKE 和 AuthIP 豁免篩選器會開放給所有位址。 若要以更細微的控制來執行防火牆，原則提供者應該在加權範圍中新增比 [**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**](filter-weight-identifiers.md)更高的篩選準則。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IPsec 設定](ipsec-configuration.md)
</dt> <dt>

[篩選器加權指派](filter-weight-assignment.md)
</dt> </dl>

 

 





