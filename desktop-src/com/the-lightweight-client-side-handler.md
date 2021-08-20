---
title: 輕量 Client-Side 處理常式
description: 輕量用戶端處理常式可讓您建立任何大小的一般用戶端處理常式，以協助您進行任何種類的標準工作。
ms.assetid: b712237c-55d7-4f52-9cf6-19c6e5fb3182
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a868b6152a13b79bc4475dca14810821065ddfe5c3590ed4e20687bc6d3614b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118103665"
---
# <a name="the-lightweight-client-side-handler"></a>輕量 Client-Side 處理常式

輕量用戶端處理常式可讓您建立任何大小的一般用戶端處理常式，以協助您進行任何種類的標準工作。 做為處理常式，這些都可供多個用戶端使用。 它們與 OLE 處理常式不同之處在于，它們無法在啟動伺服器之前建立，而且其存留期會系結至 proxy 管理員的存留期，以防止可能發生競爭情況的情況下，處理常式可能會在其他情況下釋放。

Proxy 管理員是系統建立的物件，它會執行 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) 介面。 如果您使用標準封送處理，當您呼叫 [**CoGetStandardMarshal**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstandardmarshal) (或 [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)時，系統會為您建立它，以針對輕量處理常式建立匯總的封送處理器) 也會在物件上執行 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) 和 [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi) 介面。 在伺服器端，有一個對應的系統物件也會執行 **IMarshal**。 這些物件會以透明的方式處理封送處理。

這些處理常式有兩種您可能想要執行的一般類型：

-   執行服務的處理常式，此服務不需要伺服器的額外資料
-   使用來自伺服器之額外資料的處理常式

伺服器所提供之資料流程中的額外資料可能會用到，如下所示：

-   來自伺服器的靜態資料。 無論正在封送處理的特定介面為何，伺服器都會將相同的資料寫入資料流程中。
-   來自伺服器的每個介面資料。 根據正在封送處理的特定介面，伺服器可能會將不同的資料寫入資料流程。
-   每個介面的協助程式。 匯總至用戶端處理常式並委派給標準 proxy 的每個介面 COM 元件。 例如，若要改善網路效能， [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 的 COM 元件可以執行資料的用戶端快取、預先讀取、寫入後端、op 鎖定等等。
-   介面的網路版本。 介面的網路版本與用戶端和伺服器應用程式程式碼所公開的介面不同。 例如，您可以透過相同的網路介面 INetAB，以內嵌伺服器處理常式的方式，將公開的介面 IA 和 IB 多工處理。 例如，您可以將資料傳輸介面轉換成使用管道的網路介面，以有效率地傳輸資料。

下層用戶端可能無法進行封送處理具有自訂處理常式的介面，原因有兩種：首先，它們可能不會在匯總伺服器處理常式且物件需要處理常式時，瞭解自訂封送封包中使用的 CLSID。 其次，如果處理常式程式碼需要 COM 的新功能來建立匯總標準封送處理器，並執行遠端 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 呼叫，甚至可能不會在用戶端上執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[OLE 處理常式](the-ole-handler.md)
</dt> </dl>

 

 