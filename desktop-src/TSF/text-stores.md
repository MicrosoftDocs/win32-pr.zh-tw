---
title: 文字存放區
description: 文字存放區
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- 文字服務架構 (TSF) 、文字存放區
- TSF (文字服務架構) 、文字存放區
- 啟用 TSF 的應用程式，文字存放區
- 文字存放區
- '文字服務架構 (TSF) ，應用程式字元位置 (ACP) '
- 'TSF (文字服務架構) ，應用程式字元位置 (ACP) '
- '啟用 TSF 的應用程式，應用程式字元位置 (ACP) '
- '應用程式字元位置 (ACP) '
- 'ACP (應用程式字元位置) '
- 文字服務架構 (TSF) 、錨點
- TSF (文字服務架構) 、錨點
- 啟用 TSF 的應用程式，錨點
- 錨點
- 文字服務架構 (TSF) 、檔鎖定
- TSF (文字服務架構) ，檔鎖定
- 啟用 TSF 的應用程式，檔鎖定
- 檔鎖定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af01edd439dbac23e4dee4b5289101a9bd92ca8180b66b460096b797d32b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950918"
---
# <a name="text-stores"></a>文字存放區

## <a name="application-character-position-acp"></a>應用程式字元位置 (ACP) 

ACP 是文字資料流程中字元（或字元）的位置，以文字資料流程開頭的字元數表示。 由於 ACP 模型是以零為基底，因此文字資料流程中的第一個字元具有零的 ACP。 例如：


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



文字存放區會執行支援 [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) 介面的物件，此介面可讓文字資料流程以 ACP 表示。 **ITextStoreACP** 介面方法會使用文字資料流程的 ACP 範圍來修改文字。

## <a name="anchor-based-applications"></a>Anchor-Based 應用程式

管理員會以原生方式使用以 ACP 為基礎的方法來操作文字。 不過，錨點型方法適用于支援[錨點](ranges.md) [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md)用戶端，因此管理員會使用[ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)和[ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)方法來包裝[ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)和[ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)方法。

## <a name="document-access-control"></a>檔存取控制

文字存放區會使用 [檔鎖定](document-locks.md)來控制文字資料流程的存取。 若要讀取或修改文字存放區，管理員必須先安裝支援 [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) 介面的建議接收，方法是呼叫 [ITextStoreACP：： AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) 方法，並將指標傳遞給建議接收器。 「建議接收」可讓管理員取得文字存放區的檔鎖定，並在文字存放區由管理員以外的其他內容（例如透過應用程式的使用者輸入）修改時接收通知。 本主題稍後會討論建議接收器。

## <a name="how-to-initialize-the-text-store"></a>如何初始化文字存放區

應用程式會藉由完成下列步驟來初始化文字存放區：

1.  藉由呼叫[CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)函式和執行緒管理員物件的指標，以根據[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)介面建立執行緒管理員物件。 以下是執行執行緒管理員物件的程式碼範例。
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  藉由呼叫 [ITfThreadMgr：： activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) 方法來啟動執行緒管理員物件。 這個方法會提供用來建立內容物件的 [用戶端識別碼](tfclientid.md) 指標。 執行緒管理員是用來執行檔管理員物件。
3.  藉由呼叫[ITfThreadMgr：： CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)方法以及檔管理員物件的指標，以建立以[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)介面為基礎的檔管理員物件。 檔案管理員物件是用來執行做為文字存放區的內容物件。
4.  藉由呼叫 [ITfDocumentMgr：： CreateCoNtext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) 方法並搭配文字存放區物件的指標和用戶端識別碼的指標，從啟用執行緒管理員，以從檔管理員建立內容物件。 以下是建立內容物件的範例：
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  使用 [ITfDocumentMgr：:P ush](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) 方法，將內容物件推送至堆疊。 以下是將內容物件推送至堆疊的範例：
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a>如何修改文字存放區

**ITfDocumentMgr：:P ush** 方法會使用建議接收介面的指標來呼叫 **ITextStoreACP：： AdviseSink** ，以安裝新的建議接收或修改現有的建議接收器。 當文字存放區由管理員以外的其他內容（例如應用程式的使用者輸入）進行修改時，「建議接收」會收到通知。 當輸入方法取得焦點時，應用程式必須呼叫 [ITfThreadMgrEventSink：： OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) 方法。 呼叫適當的 **ITextStoreACPSink** 介面方法，即可提供執行緒管理員的其他通知。

不過，應用程式不應該呼叫 **ITextStoreACPSink** 介面方法來回應 **ITextStoreACP** 介面方法。 應用程式應該只在管理員以外的其他內容修改文字存放區時，才呼叫 **ITextStoreACPSink** 介面方法。

您可以使用稱為 [組合](compositions.md)的暫存輸入狀態來修改文字存放區的內容。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錨點](ranges.md)
</dt> <dt>

[成分](compositions.md)
</dt> <dt>

[檔鎖定](document-locks.md)
</dt> <dt>

[ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 