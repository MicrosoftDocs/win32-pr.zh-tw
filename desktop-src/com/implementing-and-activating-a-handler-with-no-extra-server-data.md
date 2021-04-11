---
title: 不使用額外的伺服器資料來執行和啟用處理常式
description: 不使用額外的伺服器資料來執行和啟用處理常式
ms.assetid: 9d91260a-4cec-4a10-bb57-d02999efae47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6866b40e1257a865aa5068ffd46611c411498877
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "103945539"
---
# <a name="implementing-and-activating-a-handler-with-no-extra-server-data"></a>不使用額外的伺服器資料來執行和啟用處理常式

若要建立處理常式的實例（如果它是未取得額外伺服器資料的實例），伺服器必須執行 [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) ，但不是 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)。 **IStdMarshalInfo** 有一個方法 [**GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler)，它會抓取要用於目的地進程的物件處理常式 CLSID。 當 COM 呼叫 [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) 並在用戶端上啟動處理常式時，會呼叫此函數。

接下來，伺服器和處理常式的執行都必須呼叫 [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) 函數。 此函式會在每一端建立標準封送處理器， (在用戶端上呼叫 proxy 管理員和伺服器端上的存根管理員) 。

伺服器會呼叫 [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)，並在旗標 SMEXF \_ 伺服器中傳遞。 這會建立伺服器端標準封送處理器 (存根管理員) 。 下圖顯示伺服器端結構：

![顯示伺服器端結構的圖表。](images/b47b3bc0-3e7d-4be4-9767-7ae436bd1b21.png)

## <a name="server-side-structure"></a>Server-Side 結構

處理常式會呼叫 [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)，並傳入旗標 SMEXF \_ 處理常式。 這會建立用戶端標準封送處理器 (proxy 管理員) ，並使用用戶端上的處理常式進行匯總。 兩者的存留期都是由控制身分識別物件所管理， (在處理常式呼叫 **CoGetStdMarshalEx** 時，執行系統所執行的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)) 。 下圖顯示用戶端結構。

![顯示用戶端結構的圖表。](images/24ae70ef-dfa8-4784-90ac-dc6cfb043ee5.png)

## <a name="client-side-structure"></a>Client-Side 結構

如上圖所示，此處理程式實際上是在 proxy 管理員和身分識別/控制未知之間 sandwiched。 這可讓系統控制物件的存留期，同時讓處理常式控制公開的介面。 身分識別和 Proxy 管理員之間的虛線表示這兩個共用會透過內部私用介面緊密整合。

當 COM 呼叫用戶端的 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) 時，它會建立處理常式實例，並使用身分識別進行匯總。 此處理程式將會透過呼叫 [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)來建立標準封送處理器 (，並在) 建立時傳入控制未知的 it 接收。 處理常式不會執行 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) ，而只會從標準封送處理器傳回 **IMarshal** 。 即使處理常式確實執行 **IMarshal**，在 unmarshal 期間也不會呼叫它。

如果兩個執行緒在第一次同時 unmarshal 相同的物件，則可能會暫時建立兩個處理常式。 接著會發行一個。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[輕量 Client-Side 處理常式](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 