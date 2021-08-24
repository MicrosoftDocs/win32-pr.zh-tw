---
title: ALE 多播/廣播流量
description: 在應用層強制執行 (ALE) 層的所有輸入多播和廣播流量都會對應到一個全域 ALE 流程。
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2849f7277cc9ada580bca22fa5a4fdf618d959d255b442607963047dd2a37bba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315608"
---
# <a name="ale-multicastbroadcast-traffic"></a>ALE 多播/廣播流量

在應用層強制執行 (ALE) 層的所有輸入多播和廣播流量都會對應到一個全域 [ALE 流程](ale-stateful-filtering.md)。 輸入多播和廣播封包的回應流量會分類于 [**FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層，並為每個回應建立個別的 ale 流程。

在 ALE 層級的輸出多播和廣播流量會建立4秒的 ALE 流程。 根據預設，輸出多播或廣播 ALE 封包的授權將允許來自任何遠端位址的輸入流量（無論是單播、多播或廣播），最長可達4秒。 這類的 ALE 流程只能透過符合 ALE 流程的後續輸出流量來重新整理或保持運作。

> [!Note]  
> 4秒的存留期是由內建的 callout [**FWPM \_ callout \_ SET \_ OPTIONS \_ AUTH \_ CONNECT \_ LAYER \_ V {4 \| 6}**](built-in-callout-identifiers.md)所指定。 若要改變4秒的預設存留期，請新增參考 **FWPM \_ CALLOUT \_ SET \_ OPTIONS \_ AUTH \_ CONNECT \_ LAYER \_ V {4 \| 6}** CALLOUT 的篩選。 如需詳細資訊，請參閱[ALE Flow 自訂](ale-flow-customization.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用層強制 (ALE) ](application-layer-enforcement--ale-.md)
</dt> <dt>

[ALE 層](ale-layers.md)
</dt> <dt>

[ALE 具狀態篩選](ale-stateful-filtering.md)
</dt> <dt>

[ALE 重新授權](ale-re-authorization.md)
</dt> <dt>

[ALE Flow 自訂](ale-flow-customization.md)
</dt> </dl>

 

 




