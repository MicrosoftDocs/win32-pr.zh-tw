---
title: 編輯內容
description: 編輯內容
ms.assetid: cf8bbe66-d2ad-49b3-9e7c-246e4ca50149
keywords:
- 文字服務架構 (TSF) 編輯內容
- TSF (文字服務架構) 、編輯內容
- 文字服務，編輯內容
- 啟用 TSF 的應用程式，編輯內容
- 編輯內容
- 文字服務架構 (TSF) 、編輯 cookie
- TSF (文字服務架構) 、編輯 cookie
- 文字服務，編輯 cookie
- 啟用 TSF 的應用程式，編輯 cookie
- 編輯 cookie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26e99b1fe3f167f4cc76e9496a2071f017abd0bea2f5196de3e3041e53e2259e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118879575"
---
# <a name="edit-contexts"></a>編輯內容

## <a name="applications"></a>應用程式

若要建立編輯內容，應用程式會呼叫 [ITfDocumentMgr：： CreateCoNtext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)。

## <a name="text-services"></a>文字服務

文字服務通常會使用目前現用的編輯內容。 目前作用中的編輯內容是活動文件管理員堆疊頂端的編輯內容。 為了取得目前使用中的內容，文字服務會呼叫 [ITfThreadMgr：： GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) 來取得使用中的檔管理員，然後呼叫 [ITfDocumentMgr：： vemap.gettop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) ，以取得堆疊頂端的編輯內容。

在某些情況下，文字服務需要自己的編輯內容。 若要建立編輯內容，文字服務會呼叫 **ITfDocumentMgr：： CreateCoNtext**。

## <a name="edit-cookies"></a>編輯 Cookie

許多方法（例如 [ITfRange：： SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)）都需要一種方法來識別具有唯讀或讀取/寫入 [檔鎖定](document-locks.md)的編輯內容。 您可以透過 TSF 管理員和應用程式之間的協商來取得檔鎖定。 文字服務無法直接執行此協商。 文字服務只能藉由要求具有特定內容和唯讀或讀取/寫入存取權的 [編輯會話](edit-sessions.md) 來取得鎖定。 當授與編輯會話時，系統會提供文字服務與 *編輯 cookie* ，以使用所要求的存取權來識別編輯內容。 此 cookie 接著會傳遞至方法，以適當的存取權識別編輯內容。

**ITfDocumentMgr：： CreateCoNtext** 也會提供編輯 cookie 給內容建立者。 此 cookie 具有唯讀存取權，且沒有任何方法可修改存取層級。 老實說，TSF manager 不會協調此編輯 cookie 的檔鎖定。 Cookie 會在內部標示為唯讀，但檔並未實際鎖定。 例如，如果內容建立者使用 **ITfDocumentMgr：： CreateCoNtext** 傳回的編輯 cookie 來呼叫 [ITfCoNtext：： GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) ，這會導致呼叫應用程式的 [ITextStoreACP：： GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)或 [ITextStoreAnchor：： GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) 。 取得選取專案之前，應用程式會判斷檔鎖定是否存在。 因為沒有鎖定存在，應用程式將會失敗，並出現 TS \_ E \_ NOLOCK。 也就是，如果應用程式使用這個 cookie 來呼叫方法，而此 cookie 會導致呼叫其中一個應用程式的文字存放區方法，它就必須在內部處理此案例，因為應用程式實際上並不會有檔鎖定。

如果內容建立者需要具有讀取/寫入存取權的編輯 cookie，它必須建立自己的編輯會話。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ITfCoNtext](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[ITfDocumentMgr：： CreateCoNtext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[ITfThreadMgr：： GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[ITfDocumentMgr：： Vemap.gettop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[ITfRange：： SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[檔鎖定](document-locks.md)
</dt> <dt>

[編輯工作階段](edit-sessions.md)
</dt> <dt>

[ITfCoNtext：： GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP：： GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




