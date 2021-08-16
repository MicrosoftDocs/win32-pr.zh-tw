---
description: 本指南提供您所需的資訊，讓您的 Microsoft Windows 應用程式使用新一代的網際網路通訊協定第6版 (IPv6) 。
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: Windows 通訊端應用程式的 IPv6 指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c52d86dfcdfa06df80dc71a3f3313de19f9201c7421a3f27f094589a6656dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741112"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a>Windows 通訊端應用程式的 IPv6 指南

本指南提供您所需的資訊，讓您的 Microsoft Windows 應用程式使用新一代的網際網路通訊協定第6版 (IPv6) 。 將 IPv6 功能新增至您的應用程式不一定是移植進程。 若要移植應用程式，建議將程式碼修改為在不同平臺上運作，這表示離開先前的平臺。 本指南的結構是專門用來協助將 IPv6 功能新增至應用程式，同時保留 IPv4 功能。

本指南將討論新增 IPv6 功能的相關問題，然後以最受轉換影響的開發領域為目標。 每個區域都可以完整說明要注意的陷阱、建議用來避免的策略，以及如何充分利用新的[Windows 通訊端 2](what-s-new-for-windows-sockets-2.md)程式設計項目 (函式和結構) 的秘訣。 如需 IPv6 的詳細資訊，請參閱 [Ipv6 支援](ipv6-support-2.md)。

本指南也提供程式碼範例，以提供您在修改應用程式時可能遇到之問題的實際操作體驗和視覺標記法。 這些範例來自完整的工作範例，簡單 Windows 通訊端應用程式已修改為支援 IPv4 和 IPv6。 這些工作範例的原始程式碼包含在本檔結尾的兩個附錄中： [附錄 A：「僅 IPv4](appendix-a-ipv4-only-source-code-2.md) 」的原始程式碼會包含應用程式的原始程式碼，然後才會將其修改為支援 IPv6; [附錄 B：](appendix-b-ip-version-agnostic-source-code-2.md) 在應用程式已啟用 IPv6 的情況下，IP 版本中立的原始程式碼會提供原始程式碼。

Microsoft 提供一個稱為 Checkv4.exe 的公用程式，可協助您在應用程式程式碼中找出可能移植的程式碼，也會提出修正的建議。 本檔會示範 Checkv4.exe 公用程式，並使用附錄中包含的範例應用程式，以及顯示 Checkv4.exe 公用程式所產生之輸出的螢幕擷取畫面。 如需詳細資訊，請參閱 [使用 Checkv4.exe 公用程式](using-the-checkv4-exe-utility-2.md)。

本指南所討論的程式設計區域包括：

-   [變更 IPv6 Winsock Html5 應用程式的資料結構](changing-data-structures-2.md)
-   [IPv6 Winsock 應用程式的函式呼叫](function-calls-2.md)
-   [使用硬式編碼的 IPv4 位址](use-of-hardcoded-ipv4-addresses-2.md)
-   [IPv6 Winsock 應用程式的消費者介面問題](user-interface-issues-2.md)
-   [IPv6 Winsock 應用程式的基礎通訊協定](underlying-protocols-2.md)
-   [IPv6 Winsock 應用程式的雙重堆疊通訊端](dual-stack-sockets.md)

因為沒有任何統一的事件順序，所以解決 IPv6 啟用問題的區段不會依序排列，因此您隨時都可以參考任何區段。 強烈建議您在將 IPv6 功能新增至應用程式時，仔細檢查每個區段。 也建議您閱讀 Checkv4.exe 公用程式的相關資訊，因為它包含瞭解決 IPv6 啟用問題之順序的秘訣。

若要查看 Checkv4.exe 公用程式，並檢查您在應用程式中處理移植程式的順序，請參閱 [使用 Checkv4.exe 公用程式](using-the-checkv4-exe-utility-2.md)。 本節包含編譯時間旗標的相關資訊，該旗標會嚴格檢查與 IPv6 不相容的程式設計項目。

若要直接移至範例應用程式，請參閱 [附錄 A：僅限 IPv4 的原始程式碼](appendix-a-ipv4-only-source-code-2.md) 和 [附錄 B： IP 版本中立的原始程式碼](appendix-b-ip-version-agnostic-source-code-2.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網際網路通訊協定第6版 (IPv6) ](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[IPv6 支援](ipv6-support-2.md)
</dt> <dt>

[適用于 Windows 2000 的 IPv6 技術預覽](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[使用 Checkv4.exe 公用程式](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[附錄 A：僅限 IPv4 的來源程式碼](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[附錄 B： IP 版本中立的原始程式碼](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



