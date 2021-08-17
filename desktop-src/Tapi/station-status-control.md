---
description: 有三個主要站狀態功能需要控制訊息等候燈、轉寄和請勿打擾。
ms.assetid: 4a6dc47f-caff-4f2b-8858-0e9bec32b137
title: 站狀態控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e136450dbda8cec260a460f49ce8d45b65d1b58ec588ccbcc435c5e3a2b1cd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861931"
---
# <a name="station-status-control"></a>站狀態控制

有三個主要站狀態功能需要控制：訊息等待燈、轉寄和請勿打擾。 轉寄和請勿打擾可透過現有的 [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) 函式來控制 (也就是位址專屬的) ，並使用 [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)查詢。 \_ [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)的 **DWDEVSTATUSFLAGS** 成員中的 LINEDEVSTATUSFLAGS MSGWAIT 位指出裝置上等待燈的訊息狀態，並 \_ 傳送 LINEDEVSTATE MSGWAITON 或 LINEDEVSTATE \_ MSGWAITOFF 訊息來指出狀態變更的時間。 [**LineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)函式可讓您控制訊息等待燈，而不需要針對該目的來執行 TAPI 電話裝置。 \_ [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)和 **LINEDEVSTATUS**) 的 **dwLineFeatures** 成員中的 LINEFEATURE SETDEVSTATUS 位 (指出可以呼叫它的時間，而 **dwSettableDevStatus** 的 **LINEDEVCAPS** 成員可讓應用程式偵測哪些裝置狀態設定可以從應用程式控制。 除了允許控制訊息等候功能之外，它也允許設定裝置的連線、Inservice 和鎖定狀態，使其在交換器或其他硬體支援的範圍內。 呼叫此函式會導致適當的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息傳送，以反映新的狀態。

 

 



