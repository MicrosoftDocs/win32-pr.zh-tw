---
description: DVD 區域資訊的來源
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: DVD 區域資訊的來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729dc02d07b927dd2bb7938ba87c6435df04459ad3ebd1976ede808bd292552e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904091"
---
# <a name="sources-of-dvd-region-information"></a>DVD 區域資訊的來源

dvd 區域資訊有三個來源可一起運作，以判斷在 Windows 電腦上播放 DVD 的區域。

-   DVD 標題。 大部分的 DVD 標題會標示為特定區域。 有些標題只能在一個區域中播放，有些可在多個區域中播放，其他則可在所有區域中播放。 區域1到6是在原始的 DVD-Video 規格中定義。 區域7目前未定義。 已在1999中新增區域8以進行特殊場地，例如飛機。 沒有視頻區域的 DVD-ROM 光碟 (，) 不應包含任何區域編碼。
-   DVD-ROM 磁片磁碟機。 DVD-ROM 磁片磁碟機有兩種類型： RPC 階段 1 (RPC1) 磁片磁碟機和 RPC 第2階段 (RPC2) 磁片磁碟機。 RPC1 磁片磁碟機沒有內建的區域管理硬體支援。 對於這些磁片磁碟機，Windows 會維護區域變更計數資訊，而且區域只能變更一次。 RPC2 磁片磁碟機會維護硬體中的區域變更計數資訊，而一般而言，這類磁片磁碟機的區域最多可以變更5次。
-   DVD 解碼器。 某些 DVD 解碼器、硬體或軟體是針對特定區域而設定。 一般情況下，使用者無法變更此解碼器的區域。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 中的 DVD 區域變更支援](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



