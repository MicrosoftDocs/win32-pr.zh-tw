---
title: 成分
description: 組合是暫時的輸入狀態，可讓文字服務指定應用程式和使用者的輸入文字仍處於變更狀態。
ms.assetid: 3d9da4f2-ceb9-4abc-8979-d3756d948a57
keywords:
- 文字服務架構 (TSF) 、撰寫
- TSF (文字服務架構) ，組合
- 文字服務，組合
- 啟用 TSF 的應用程式，組合
- compositions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b03f3e991f76ee7c6dca3830267796576c7b842
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376264"
---
# <a name="compositions"></a>成分

組合是暫時的輸入狀態，可讓文字服務指定應用程式和使用者的輸入文字仍處於變更狀態。 應用程式可以和應該取得組合的顯示內容資訊，並使用此資訊向使用者顯示組合狀態。

在語音輸入期間使用組合的其中一個範例。 當使用者說話時，語音文字服務會建立組合。 這項組合將保持不變，直到整個語音輸入完成為止。 當會話結束時，語音文字服務會終止組合。

應用程式會使用組合的存在和不存在，來決定如何顯示文字，以及應對文字執行哪些作業（如果有的話）。 例如，如果使用者使用語音引擎來輸入文字，則應用程式不應對任何組合文字執行任何拼寫或文法檢查。 在結束組合之前，會將文字視為未完成。

## <a name="text-services"></a>文字服務

文字服務會藉由呼叫 [ITfCoNtextComposition：： StartComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-startcomposition)來建立組合。 文字服務可以選擇性地執行接收撰寫事件通知的 [ITfCompositionSink](/windows/desktop/api/msctf/nn-msctf-itfcompositionsink) 物件。 StartComposition 會傳回 [ITfComposition](/windows/desktop/api/msctf/nn-msctf-itfcomposition) 物件，此物件可讓文字服務保存參考，並使用來修改和終止組合。 文字服務會藉由呼叫 [ITfComposition：： EndComposition](/windows/desktop/api/msctf/nf-msctf-itfcomposition-endcomposition)來終止組合。

如果文字服務將建立組合，也應該支援顯示內容，讓應用程式顯示與標準文字不同的組合文字。 如需詳細資訊，請參閱 [提供顯示內容](providing-display-attributes.md)。

## <a name="applications"></a>應用程式

應用程式可以藉由安裝 [ITfCoNtextOwnerCompositionSink](/windows/desktop/api/msctf/nn-msctf-itfcontextownercompositionsink) 接收，來監視組合的建立、變更和終止。 當組合開始時，會呼叫 [ITfCoNtextOwnerCompositionSink：： OnStartComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onstartcomposition) 。 同樣地，當組合變更或終止時，會分別呼叫 [ITfCoNtextOwnerCompositionSink：： OnUpdateComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onupdatecomposition) 和 [ITfCoNtextOwnerCompositionSink：： OnEndComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onendcomposition) 。

以下是使用組合來更新檔的一般程式。

1.  [ITextStoreACP：： InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection) 或 [ITextStoreAnchor：： InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection) 通常用來將初始文字插入組合中。
2.  組合是使用 [ITfCoNtextComposition：： StartComposition](/windows/desktop/api/Msctf/nf-msctf-itfcontextcomposition-startcomposition)的呼叫來啟動，並使用 **InsertTextAtSelection** 所傳回的文字範圍。
3.  當它收到新的輸入（例如語音或鍵盤輸入）時，應用程式會使用 [ITextStoreACP：： SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext) 或 [ITextStoreAnchor：： SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)來更新組合。
4.  當應用程式判斷是否要結束組合時，它會呼叫 [ITfComposition：： EndComposition](/windows/desktop/api/Msctf/nf-msctf-itfcomposition-endcomposition)。

應用程式應該使用文字服務所提供的顯示內容，隨時修改文字的顯示，而不只是在組合為使用中時。 如需詳細資訊，請參閱 [使用顯示內容](using-display-attributes.md)。

如有必要，應用程式可以藉由呼叫 [ITfCoNtextOwnerCompositionServices：： TerminateComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionservices-terminatecomposition)來終止組合。

 

 