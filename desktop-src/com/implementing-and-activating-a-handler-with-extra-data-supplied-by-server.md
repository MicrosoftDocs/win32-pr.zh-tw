---
title: 使用伺服器提供的額外資料來執行和啟用處理常式
description: 使用伺服器提供的額外資料來執行和啟用處理常式
ms.assetid: 5bbf81bd-430d-4008-b1cc-9ea91bb3b1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78a3e39c85c37c52dfa3f09ef41f0a71b5f431
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "104321323"
---
# <a name="implementing-and-activating-a-handler-with-extra-data-supplied-by-server"></a>使用伺服器提供的額外資料來執行和啟用處理常式

如果伺服器要在封包中包含一些額外的資料以供處理常式使用，則伺服器必須同時執行 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) 和 [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) 介面。 伺服器必須匯總標準封送處理器，而且必須將封送處理的第一個部分委派給匯總的標準封送處理器（包括 [**IMarshal：： GetUnmarshalClass**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getunmarshalclass)），而且必須將它自己的資料大小加入標準封送處理器的 [**IMarshal：： GetMarshalSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getmarshalsizemax)傳回的大小。 標準封送處理器會呼叫 [**IStdMarshalInfo：： GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler) 來取得要建立之處理常式的 CLSID。 標準封送處理器完成封送處理之後，伺服器會將自己的額外資料寫入資料流程中。 下圖顯示產生的結構以及資料流程中的額外資料，如下圖所示：

![顯示資料流程中有額外資料之結構的圖表。](images/4cff306b-bb82-4c05-8e64-7ca73731f265.png)

## <a name="server-side-structures-with-extra-data-in-stream"></a>資料流程中具有額外資料的 Server-Side 結構

如此一來，如果無法建立處理常式，則在用戶端上呼叫 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) 時，可以略過任何未讀取的資料，並將資料流程保留在適當的位置。

## <a name="client-side-structures-with-extra-data-in-stream"></a>資料流程中具有額外資料的 Client-Side 結構

在資料流程中沒有額外的伺服器資料的情況下，用戶端對 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) 的 COM 呼叫將會建立身分識別和處理常式。 處理常式必須執行 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) ，而且必須先將 **IMarshal** 呼叫委派給匯總的標準封送處理器，然後封送處理或 unmarshal 伺服器提供的任何額外資料。 將會針對每個 unmarshal 呼叫處理常式的 [**UnmarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-unmarshalinterface) ，不論它是否已將介面取消封送處理。 在此情況下，伺服器不會呼叫 [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) ，但處理常式必須是。 產生的用戶端結構如下圖所示。

![顯示用戶端結構的圖表。](images/053411c7-9d54-4ae5-bcb6-778454b1d86f.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[輕量 Client-Side 處理常式](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 