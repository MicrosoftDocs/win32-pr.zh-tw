---
title: 內容編碼
description: 從 Windows Server 2008 和 Windows Vista 開始，應用程式可以導向 WinINet 來執行 gzip 和 deflate 內容編碼配置的內容解碼。
ms.assetid: 136f22a6-e5ca-41c5-8651-6e132655d268
keywords:
- 內容編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b089ae2aa4cbacdfc9b6ebefe5cbdfc1bfc10e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023960"
---
# <a name="content-encoding"></a>內容編碼

如同 HTTP 通訊協定中所指定 (RFC 2616) 應用程式可以要求伺服器以編碼格式傳回 HTTP 回應。 在 Windows Server 2008 和 Windows Vista 之前，會將內容編碼的要求傳送至應用程式，以在其層級進行處理。 從 Windows Server 2008 和 Windows Vista 開始，應用程式可以導向 WinINet 來執行 gzip 和 deflate 內容編碼配置的內容解碼。

若要啟用內容解碼，應用程式會設定解碼選項，要求 WinINet 代表他們執行解碼。 不過，啟用解碼並不保證 WinINet 會執行內容解碼，而應用程式應該準備好處理解碼。 當成功執行內容解碼時，WinINet 會從回應中去除內容編碼標頭。 當回應中出現內容編碼標頭時，無論是否啟用或停用解碼選項，應用程式都應該處理內容解碼。

啟用解碼時，應用程式必須在要求的 Accept-Encoding 標頭中指定支援的編碼清單。 不過，Accept-Encoding 標頭不會商都必須伺服器來傳送編碼的回應。 WinINet 會將不符合可接受之編碼清單的回應傳送回應用程式。

下列清單描述當啟用選項時，WinINet 將執行內容解碼的條件：

-   要求中必須有 Accept-Encoding 標頭，而且必須指定 gzip、deflate 或 gzip 和 deflate 編碼配置。
-   在內容編碼標頭中指定的編碼配置必須符合 Accept-Encoding 標頭中指定的其中一個編碼配置。
-   回應中的內容編碼標頭只會指定一種編碼配置。
-   回應必須只包含一個內容編碼標頭。 WinINet 只會將以一種編碼配置編碼的內容解碼。
-   Cache-Control 標頭不能包含無轉換指示詞。
-   內容約制標頭不能出現在回應中。

## <a name="setting-the-decompression-option"></a>設定解壓縮選項

您可以在會話控制碼、要求控制碼或連接控制碼上設定解碼選項。 設定解碼選項的控制碼，會定義解碼選項的範圍。 例如，在會話上設定解碼將可解碼在該控制碼下建立的所有連接和要求。

若要設定解碼選項，應用程式會使用從 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)、 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)傳回的控制碼來呼叫 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 。 [ **網際網路 \_ 選項 \_ HTTP \_ 解碼** ] 選項是在 *DwOption* 參數中指定，而 *lpBuffer* 參數則指向設定為 true 的布林值變數。 若要停用解碼，應用程式會使用 **網際網路 \_ 選項 \_ HTTP \_ 解碼** 選項來呼叫 **InternetSetOption** ，並將布林值變數設定為 false。

當設定解碼選項時，WinINet 會在應用程式呼叫 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)時，對要求執行解碼。 如果 WinINet 在執行內容解碼時發生錯誤，對 **InternetReadFile** 的呼叫會失敗，並出現 **錯誤 \_ 網際網路 \_ 解碼 \_ 失敗**。 解碼失敗時，應用程式有兩個選項：可以移除 Accept-Encoding 標頭並重新傳送要求，也可以將要求上的 **網際網路 \_ 選項 \_ HTTP \_ 解碼** 選項設定為 false，然後再重新傳送要求。 如果解碼選項設定為 false，則應用程式必須檢查內容編碼標頭，並在應用層級執行任何解碼。

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 