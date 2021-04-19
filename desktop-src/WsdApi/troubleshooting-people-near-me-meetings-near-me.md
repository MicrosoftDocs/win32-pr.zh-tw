---
description: 列出針對「近端」近端分享/會議進行疑難排解時，所要使用的診斷程式。
ms.assetid: 36190bc2-59f6-41ff-b443-894abb7f2ed8
title: 疑難排解近端分享/會議近端分享
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee35bf85cb850d690623b2333ff1a36b82e3fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974211"
---
# <a name="troubleshooting-people-near-memeetings-near-me"></a>疑難排解近端分享/會議近端分享

近端分享/會議近端分享：

-   一律使用 UDP WS-Discovery 進行裝置探索
-   不會執行任何中繼資料交換

下列診斷程式應依序 (使用) ，以協助找出「近端」近端分享/會議的問題。

**疑難排解近端分享/會議近端分享**

1.  [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。
2.  [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。
3.  [使用 WSD Debug 用戶端來驗證多播流量](using-wsddebug-client-to-verify-multicast-traffic.md)。
4.  [檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)。

如果無法使用上述診斷程式來識別問題的來源，請遵循 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md) 並聯絡 Microsoft 支援服務的指示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



