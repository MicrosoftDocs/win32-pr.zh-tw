---
description: 傳送 COPP 命令
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: 傳送 COPP 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044756f8bdfe59e44309c158cb0be1dc983143d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973129"
---
# <a name="sending-copp-commands"></a>傳送 COPP 命令

若要傳送經認證的輸出保護通訊協定 (COPP) 命令，請填入 [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) 結構，如下所示：

-   **guidCommandID**。 識別命令的 GUID。 請參閱 COPP 命令參考。
-   **dwSequence**。 命令的序號。 請在每個命令之後遞增此值。  (在 [起始 COPP 會話](initiating-a-copp-session.md)時，此值會顯示為 **uCommandSeq** 。 ) 
-   **cbSizeData**。 命令所需的任何資料大小（以位元組為單位）。
-   **CommandData**。 命令的資料。

填入此資料之後，請計算命令的 MAC：

1.  針對在 **AMCOPPCommand** 結構的 **macKDI** 成員後面出現的資料區塊，計算 OMAC-1 標記。
2.  將此值複製到結構的 **macKDI** 成員。

現在將結構傳遞至 [**IAMCertifiedOutputProtection：:P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用認證輸出保護通訊協定 (COPP) ](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



