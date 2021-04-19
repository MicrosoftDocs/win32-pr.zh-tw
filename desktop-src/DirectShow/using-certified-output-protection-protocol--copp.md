---
description: '使用認證輸出保護通訊協定 (COPP) '
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: '使用認證輸出保護通訊協定 (COPP) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76460e335985c2aab7f9047b55d2df05aace0269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990323"
---
# <a name="using-certified-output-protection-protocol-copp"></a>使用認證輸出保護通訊協定 (COPP) 

經認證的輸出保護通訊協定 (COPP) 可讓應用程式在從圖形介面卡移至顯示裝置時，保護影片串流。 應用程式可以使用 COPP 來探索哪些類型的實體連接器連接到顯示裝置，以及可用的輸出保護類型。 保護機制包括下列各項：

-   High-Bandwidth 數位內容保護 (HDCP) 
-   複製世代管理系統—類比 (CGMS-A) 
-   類比禁止複製 (ACP) 

如果圖形介面卡支援其中一種機制，應用程式可以使用 COPP 來設定保護層級。

COPP 會定義用來建立與圖形驅動程式安全通道的通訊協定。 它會使用 (Mac) 的訊息驗證碼，來確認應用程式與顯示驅動程式之間所傳遞 COPP 命令的完整性。 應用程式會使用 COPP，方法是在 DirectShow 視頻混合轉譯器篩選器的 [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) 介面上呼叫方法， (VMR-7 或 VMR-9) 。

COPP 不會定義可能適用于數位媒體內容的數位版權原則任何內容。 此外，COPP 本身不會執行任何輸出保護系統。 COPP 通訊協定只是提供一種方法，可讓您使用介面卡所提供的保護系統，在圖形介面卡上設定和查詢保護層級。

本節假設您已熟悉下列技術：

-   DirectShow
-   Windows Media Format SDK
-   XML
-   公開金鑰密碼編譯和對稱式密碼編譯

本節中的程式碼範例會使用 Microsoft 的 CryptoAPI 來執行密碼編譯作業。 本節包含下列主題：

-   [COPP 總覽](overview-of-copp.md)
-   [取得驅動程式的憑證鏈](obtaining-the-drivers-certificate-chain.md)
-   [驗證憑證鏈](validating-the-certificate-chain.md)
-   [憑證撤銷清單](certificate-revocation-lists.md)
-   [匯入驅動程式的公開金鑰](importing-the-drivers-public-key.md)
-   [起始 COPP 會話](initiating-a-copp-session.md)
-   [傳送 COPP 狀態要求](sending-copp-status-requests.md)
-   [傳送 COPP 命令](sending-copp-commands.md)
-   [測試圖形驅動程式是否支援 COPP](testing-whether-a-graphics-driver-supports-copp.md)
-   [COPP 查詢參考](copp-query-reference.md)
-   [COPP 命令參考](copp-command-reference.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片混合轉譯器](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



