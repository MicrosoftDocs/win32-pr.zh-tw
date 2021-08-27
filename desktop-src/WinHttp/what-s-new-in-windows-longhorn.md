---
description: 從 Windows Server 2008 和 Windows Vista 開始，WinHTTP API 已經過增強，可包含下列功能。
ms.assetid: b47a2e38-67bd-4d43-936c-8781641cb7f6
title: Windows Server 2008 與 Windows Vista 有哪些新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e474bbfa32d8f82737df4be6f537ca0a6f1bc870e2028d7dcdb1f418adb7120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071698"
---
# <a name="whats-new-in-windows-server-2008-and-windows-vista"></a>Windows Server 2008 和 Windows Vista 的新功能

從 Windows Server 2008 和 Windows Vista 開始，WinHTTP API 已經過增強，可包含下列功能。

## <a name="greater-than-4-gb-upload"></a>Upload 大於 4 GB。

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 只能傳送 4 GB 的資料，因為 DWORD 總長度參數的大小有所限制。 若要讓應用程式傳送超過 4 GB 的資料，則會將內容長度標頭新增至要求，並將資料指定為大型 \_ 整數 (2 ^ 64 位元組) 。 如需詳細資訊，請參閱 **WinHttpSendRequest**。 [**IWinHttpRequest**](iwinhttprequest-interface.md) COM 物件不支援這項功能。

## <a name="transfer-encoding-header"></a>Transfer-Encoding 標頭

Transfer-Encoding 標頭可讓應用程式將區塊資料傳送至伺服器。 當要求中有 Transfer-Encoding 標頭時，應用程式會在呼叫 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)時，將長度為零的實體主體傳送給要求。 實體主體會在後續的 [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)呼叫中傳送。 [**IWinHttpRequest**](iwinhttprequest-interface.md) COM 物件不支援這項功能。

## <a name="ssl-client-certificate-issuer-list-retrieval"></a>SSL 用戶端憑證簽發者清單抓取

應用程式可以在 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 失敗時取得 SSL 用戶端憑證簽發者清單，且 **需要錯誤的 \_ WINHTTP \_ 用戶端 \_ 驗證 \_ \_** 憑證。 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單** 是新的選項，可讓應用程式取出憑證簽發者清單，並篩選清單以取得最佳憑證。 如需詳細資訊，請參閱「 [SSL 用戶端驗證](ssl-in-winhttp.md)的 [**選項旗標**](option-flags.md)和簽發者清單抓取」主題。 [**IWinHttpRequest**](iwinhttprequest-interface.md) COM 物件不支援這項功能。

## <a name="optional-client-certificates"></a>選用用戶端憑證

當 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 失敗並出現 **錯誤， \_ WINHTTP \_ 用戶端 \_ 驗證憑證 \_ \_ 需要** 時，伺服器可能不需要 SSL 用戶端憑證。 伺服器可以還原成另一種形式的驗證，或允許用戶端繼續進行匿名存取。 應用程式會設定 **winHTTP \_ 選項 [ \_ 用戶端憑證 \_ \_ 內容** ] 選項，並指定 winHTTP 用來判斷是否需要用戶端憑證的宏。 如需詳細資訊，請參閱 [**選項旗標**](option-flags.md)。 [**IWinHttpRequest**](iwinhttprequest-interface.md) COM 物件不支援這項功能。

## <a name="source-and-destination-ip-addresses"></a>來源和目的地 IP 位址

當 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 完成時，應用程式可以取出產生回應之要求的來源和目的地 IP 位址和埠。 當設定 **WINHTTP \_ 選項 \_ 連接 \_ 資訊** 選項時，會提供新的結構來接收來源和目的地位址。 如需詳細資訊，請參閱 [**選項旗標**](option-flags.md)。 [**IWinHttpRequest**](iwinhttprequest-interface.md) COM 物件不支援這項功能。

## <a name="additional-ssl-client-authentication-errors"></a>其他 SSL 用戶端驗證錯誤

額外的 SSL 用戶端驗證錯誤會提供 SSL 用戶端憑證的詳細資訊。 **錯誤 \_winHTTP \_ 用戶端憑證 \_ \_ 沒有 \_ 私密金鑰 \_** 和 **錯誤 \_ WINHTTP \_ 憑證 \_ 無 \_ 需 \_ 存取 \_ 私密金鑰** 用戶端憑證錯誤是 Windows Server 2008 和 Windows Vista 的新問題。 [**IWinHttpRequest**](iwinhttprequest-interface.md) COM 物件會以 HRESULT 傳回這些錯誤。

 

 



