---
title: ALE Flow 自訂
description: 在應用層強制執行的網路篩選 (Windows 篩選平台的 ALE) 層 (WFP) 可透過新增具有特定分類選項的篩選準則來自訂。
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe42a6df32bc69ba454226eb113cb43756224daaf752c3925f1f2d3bacd7650
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951367"
---
# <a name="ale-flow-customization"></a>ALE Flow 自訂

在應用層強制執行的網路篩選 (Windows 篩選平台的 ALE) 層 (WFP) 可透過新增具有特定分類選項的篩選準則來自訂。

## <a name="multicastbroadcast-traffic"></a>多播/廣播流量

若要根據輸出多播或廣播狀態來封鎖輸入流量，請新增篩選準則，以授權輸出多播和廣播流量，並將 [ [**.Fwp \_ 分類 \_ 選項] \_ 多播 \_ 狀態**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) 選項設為 [已設定為 [已設定為已設定為 [ **\_ \_ \_ 拒絕 \_ 多播 \_ 狀態**]。

## <a name="remote-peers"></a>遠端對等

若要將來自不同對等的回應封包加入至相同的 ALE 流程，請新增一個篩選準則，此篩選器會將 [ [**.Fwp \_ 分類 \_ 選項 \_ 鬆散 \_ 來源 \_ 對應**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) ] 選項設定為 [ **\_ \_ \_ 啟用 \_ 鬆散 \_ 來源 \_ 對應**]。

請參閱使用程式碼範例的 [分類選項](using-classify-options.md) 。

## <a name="ale-flow-lifetime"></a>ALE Flow 存留期

若要修改 ALE 流程的閒置超時值，請加入具有 [ [**.Fwp \_ 分類 \_ 選項 \_ MCAST \_ BCAST \_ 存留期**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) 選項] 和/或 [已將 [已設定的 **\_ \_ 單播分類選項的 \_ 單播 \_ 存留期** ] 選項設定為所需閒置 timeout 值的篩選準則。

請參閱 [使用分類選項](using-classify-options.md) 來取得程式碼範例。

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

[ALE 重新授權](ale-re-authorization.md)
</dt> <dt>

[使用分類選項](using-classify-options.md)
</dt> </dl>

 

 




