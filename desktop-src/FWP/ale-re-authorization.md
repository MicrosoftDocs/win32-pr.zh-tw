---
title: ALE 重新授權
description: 在應用層強制執行的網路流量 (Windows 篩選平台的 ale) 層 (以 ale 流程篩選 WFP) 。
ms.assetid: 3cc7f78e-3f9d-4a91-8ea0-9b64c299068a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 850cd7f789c1fb1222a0d6820e84a42cf41763dac4e57b96667e7feda364374c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582688"
---
# <a name="ale-reauthorization"></a>ALE 重新授權

在應用層強制執行的網路流量 (Windows 篩選平台的 ale) 層 (以[ale 流程](ale-stateful-filtering.md)篩選 WFP) 。 一旦允許 ALE 流程，就會允許屬於 ALE 流程的所有流量。 重新授權是驗證 ALE 流程許可權的要求，通常是因為網路原則有變更。

ALE 流程會根據觸發流程建立和授權的第一個封包方向，指派一個方向（輸入或輸出）。 輸入 ALE 流程是在 [**FWPM \_ 層的 \_ ale \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層建立和授權的。 **FWPM \_ LAYER \_ ale \_ AUTH \_ CONNECT \_ V {4 \| 6}** 層會建立和授權輸出 ALE 流程。 ALE 流程的方向不會限制屬於流程的封包方向。 ALE 流程包含輸入和輸出封包，而不考慮 ALE 流程本身的方向。

系統會觸發 ALE 流程的重新授權，如下所示：

-   在最初授權或建立 ALE 流程的層級變更原則。
-   抵達介面不同于原本授權或建立 ALE 流程的介面。
-   暫止的連接。

重新授權可與初始授權區別，因為出現的 [**\_ \_ \_ 是已 \_ 重新授權旗標的 .fwp 條件旗**](filtering-condition-flags-.md) 標。

重新授權只能在 [**FWPM \_ 層的 \_ ale \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 和 **FWPM \_ LAYER \_ ale \_ auth \_ CONNECT \_ v {4 \| 6}** 層進行。

### <a name="policy-change-reauthorization"></a>原則-變更重新授權

原則變更會實作為在 ALE 層的新增或移除篩選。 一旦偵測到原則變更，系統將會指定第一個流經受影響層級所建立之 ALE 流程的封包，以重新授權至圖層。 因此，在重新授權中，輸出封包完全有可能分類于 [**FWPM \_ 層 \_ ale \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層，並將輸入封包分類于 **FWPM \_ LAYER \_ ale \_ auth \_ CONNECT \_ V {4 \| 6}** 層。

這種混合方向分類的原因之一是，可能沒有來自原始方向的進一步網路流量 (例如，輸入的 ALE 流量) 的輸入封包。 其中一個範例是在初始雙向交握之後的單向 UDP 串流。 在此情況下，較好的做法是盡可能儘快卸載串流。

### <a name="arrival-interface-reauthorization"></a>抵達介面重新授權

從 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 開始，可以使用抵達介面重新授權。

屬於相同 ALE 流程的封包可以從多個介面抵達。 第一個要在與 ALE 流程的原始介面不同的介面上進入的封包是重新授權。

在強式主機模型中（TCP/IP 堆疊的預設安全性模型），網路介面上的連線只接受在相同介面上的封包。 因此，不會在強式主機電腦上使用抵達介面重新授權。

在弱式主機模型中，網路介面上的連線允許傳入任何其他網路介面上的封包。 抵達介面重新授權用於弱式主機電腦上，以執行介面特定的原則。 如需詳細資訊，請參閱「 [纜線專家：強式和弱式主機模型」。](/previous-versions/technet-magazine/cc137807(v=msdn.10))

某些 [資料欄位](filtering-conditions.md) 在重新授權期間可能未知。 例如，如果在 [**FWPM \_ 層的 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層重新授權輸出封包，則與抵達介面相關的所有欄位都是未知的。 在此情況下，未知欄位的值會表示為 [**.Fwp \_ 空白**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)。

類型 [**\_ 為 .fwp 空白**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) 的欄位，可以比 [**對 \_ \_ 相等的 .fwp 相符**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type)。 因此，您可以設定原則來封鎖 reauthorizations，並在重新授權要求的 ALE 流量抵達時清除 ALE 流程。

## <a name="pending-connection-reauthorization"></a>暫止連接重新授權

注標驅動程式可以延後 ALE 層級的分類作業，並在稍後安全地進行篩選決策時完成。 ALE 延遲/完成功能是透過核心模式函式 [FwpsPendOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpspendoperation0) 和 [FwpsCompleteOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscompleteoperation0)支援。

重新授權會在 FwpsCompleteOperation0 呼叫之後立即觸發，並允許標注驅動程式允許或封鎖流程。

只有初始授權可以延後。 如果已設定 [ [**\_ 已設定 \_ \_ \_ 重新授權**](filtering-condition-flags-.md) 旗標] 旗標，呼叫 FwpsPendOperation0 將會失敗。

如需詳細資訊，請參閱[Windows 驅動程式套件](/windows-hardware/drivers/ddi/_netvista/)檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用層強制 (ALE) ](application-layer-enforcement--ale-.md)
</dt> <dt>

[ALE 層](ale-layers.md)
</dt> <dt>

[ALE 具狀態篩選](ale-stateful-filtering.md)
</dt> <dt>

[ALE 多播/廣播流量](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[ALE Flow 自訂](ale-flow-customization.md)
</dt> </dl>

 

 