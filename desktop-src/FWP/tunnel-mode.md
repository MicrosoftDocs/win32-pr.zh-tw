---
title: Tunnel模式
description: Tunnel 模式 ipsec 原則案例可用來對兩個通道端點之間的所有相符流量套用 ipsec 通道模式保護。
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbac16de0dc01bc37e0e4f4b997d00d19339de021ffce66a0d3cf6957addbe90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639068"
---
# <a name="tunnel-mode"></a>Tunnel模式

Tunnel 模式 ipsec 原則案例可用來對兩個通道端點之間的所有相符流量套用 ipsec 通道模式保護。

此原則案例通常用來保護多個分公司子網之間的流量，並在網際網路上對應的閘道之間轉送。 它也可以用來保護兩部主機電腦（也稱為點對點通道）之間的端對端通訊。

若要使用 Windows 篩選平台 (WFP) 來實行 Tunnel 模式原則，請呼叫 [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)函式，以代表呼叫端在適當層級具現化適當的通道模式篩選。 呼叫端必須指定主要模式、快速模式提供者內容，以及描述通道內應保護之流量的篩選準則。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[範例程式碼：使用 Tunnel 模式](using-tunnel-mode.md)
</dt> <dt>

[**篩選層識別碼**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




