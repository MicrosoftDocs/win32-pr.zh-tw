---
description: 使用 DMO 類別範本
ms.assetid: 5193ad08-aaee-47e3-93eb-a126a66d8f23
title: 使用 DMO 類別範本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 205ee51953aff35ef5b05790b45fcd0bdf3bcd753239a521e40ca796c21b0a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130898"
---
# <a name="using-the-dmo-class-template"></a>使用 DMO 類別範本

DirectShow 包含用於執行 DMOs 的類別樣板 [**IMediaObjectImpl**](imediaobjectimpl-class-template.md)。 此範本會處理許多「簿記」工作，例如驗證輸入參數。 藉由使用範本，您可以將焦點放在 DMO 特有的功能。 此外，此範本有助於確保您能夠建立強大的實作為。 範本會定義在標頭檔 Dmoimpl 中，該檔案位於 SDK 的 Include 目錄中。

**IMediaObjectImpl** 範本會繼承 [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject)介面。 若要使用範本建立 DMO，請定義衍生自 **IMediaObjectImpl** 的新類別。 範本會實 **IMediaObject** 方法。 在大部分情況下，範本會在衍生類別上呼叫對應的私用方法。 範本提供下列功能：

-   基本參數檢查。 範本方法會驗證必要的參數不是 **Null**、資料流程索引在範圍內，且旗標有效。
-   鎖定。 範本方法會呼叫兩個內部方法（**鎖定** 和 **解除鎖定**）來序列化 DMO 上的作業。 這項功能可確保 DMO 具備執行緒安全。
-   媒體類型。 此範本會儲存用戶端所設定的媒體類型，並提供媒體類型的存取子方法。
-   流。 此範本會防止串流處理，直到用戶端已設定所有非選用資料流程的媒體類型。 它也可確保在串流開始之前呼叫 [**IMediaObject：： AllocateStreamingResources**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) 方法，以確保配置資源。

衍生的類別必須執行 **IUnknown** 介面;範本未提供這個介面。 您可以使用 Active Template Library (ATL) 來執行 **IUnknown**，也可以提供一些其他實作為。 此範本也不會執行鎖定機制。 衍生的類別必須執行 **鎖定** 和 **解除** 鎖定方法。 如果您使用 ATL 建立類別，您可以使用預設的 ATL 執行。

**宣告衍生類別**

**IMediaObjectImpl** 類別範本的宣告方式如下：


```C++
template <class _DERIVED_, int NUMBEROFINPUTS, int NUMBEROFOUTPUTS>
class IMediaObjectImpl : public ImediaObject
```



這三個範本參數是 \_ 衍生的 \_ 、NUMBEROFINPUTS 和 NUMBEROFOUTPUTS。 Set \_ 衍生 \_ 等於您類別的名稱。 另外兩個參數會定義 DMO 上輸入資料流程和輸出資料流程的數目。 例如，若要建立一個名為 CMyDmo 的 DMO 類別，以支援一個輸入資料流程和兩個輸出資料流程，請使用下列宣告：


```C++
class CMyDmo : public IMediaObjectImpl<CMyDmo, 1, 2>
```



本節的其餘部分將說明範本如何在 **IMediaObject** 中執行各種方法。

**設定媒體類型的方法**

下列方法會設定或取出 DMO 上的媒體類型：

-   **GetInputType**、 **GetOutputType**。 這些方法會傳回慣用的媒體類型，依串流號碼和類型索引。 此範本會在衍生類別上呼叫 **InternalGetInputType** 或 **InternalGetOutputType** 。
-   **SetInputType**、 **SetOutputType**。 這些方法會設定資料流程的媒體類型、測試媒體類型或清除媒體類型。 若要驗證媒體類型，範本會呼叫衍生類別上的 **InternalCheckInputType** 或 **InternalCheckOutputType** 。 衍生的類別會傳回 S \_ OK，以接受類型或 DMO \_ E \_ INVALIDTYPE 來拒絕型別。 範本會處理設定或清除媒體類型。
-   **GetInputCurrentType**、 **GetOutputCurrentType**。 這些方法會傳回資料流程的目前媒體類型， \_ \_ \_ \_ 如果未設定任何類型，則會傳回未設定的 DMO E 類型。 此範本會完全實作為這些方法。

**參考方法**

下列方法提供 DMO 的相關資訊。

-   **GetInputMaxLatency**、 **SetInputMaxLatency**。 這些方法會取得或設定最大延遲。 此範本會在衍生類別上呼叫 **InternalGetInputMaxLatency** 或 **InternalSetInputMaxLatency** 。
-   **GetInputSizeInfo**、 **GetOutputSizeInfo**。 這些方法會為指定的資料流程傳回 DMO 的緩衝區需求。 如果未在該資料流程上設定任何媒體類型，範本 \_ \_ 會傳回未設定 DMO E 類型 \_ \_ 。 否則，它會在衍生類別上呼叫 **InternalGetInputSizeInfo** 或 **InternalGetOutputSizeInfo** 。
-   **GetInputStreamInfo**、 **GetOutputStreamInfo**。 這些方法會傳回各種旗標，以指出用戶端應該如何格式化資料。 此範本會在衍生類別上呼叫 **InternalGetInputStreamInfo** 或 **InternalGetOutputStreamInfo** 。
-   **GetStreamCount**。 這個方法會傳回輸入和輸出資料流程的數目。 此範本會使用範本參數來執行此方法。

**資源配置的方法**

-   **AllocateStreamingResources** 方法會在串流處理開始之前，先配置 DMO 需要的任何資源。 **FreeStreamingResources** 方法會釋放相同的資源。 範本會分別呼叫 **InternalAllocateStreamingResources** 和 **InternalFreeStreamingResources**。

DMO 的用戶端不需要呼叫這些方法，但範本會在串流處理開始之前自動呼叫 **AllocateStreamingResources** 。 因此，DMO 可以假設在呼叫 **ProcessInput** 時，已正確配置資源。 DMO 應該在其函式中呼叫 **FreeStreamingResources** 。

此外，當範本呼叫 **InternalAllocateStreamingResources** 時，它會設定內部旗標，如此一來，它就不會再次呼叫該方法，直到呼叫 **InternalFreeStreamingResources** 為止。 這可確保不會意外地重新配置資源，可能會造成記憶體流失。

**串流處理方法**

下列方法可用來串流資料：

-   **GetInputStatus**。 這個方法會指出 DMO 目前是否可以接受輸入。 範本會在衍生類別上呼叫 **InternalAcceptingInput** 。 如果 DMO 可以接受輸入，則衍生類別會傳回 \_ [確定]，而範本會 \_ \_ \_ \_ 在 *dwFlags* 參數中設定 DMO 輸入 STATUSF 接受資料位。 否則，衍生類別會傳回 \_ FALSE，而範本會將 *dwFlags* 設定為零。
-   **ProcessInput**。 這個方法會處理輸入緩衝區。 此範本會呼叫先前所述的 **AllocateStreamingResources**。 然後，它會在衍生的類別上呼叫 **InternalAcceptingInput** 。 如果 DMO 可以接受新的輸入，範本就會呼叫 **InternalProcessInput**。
-   **ProcessOutput**。 這個方法會處理一組輸出緩衝區，每個輸出資料流程都有一個緩衝區。 此範本會呼叫 **AllocateStreamingResources** ，然後 **InternalProcessOutput**。
-   不 **中斷。** 這個方法會通知輸入資料流程中的不連續。 範本會在衍生類別上呼叫 **InternalAcceptingInput** 。 如果該方法傳回 S \_ OK，則範本會在衍生類別上呼叫 **InternalDiscontinuity** 。
-   **Flush**： 這個方法會清除 DMO。 範本會在衍生類別上呼叫 **InternalFlush** 。 DMO 應捨棄其仍保留要處理的任何輸入緩衝區。

此範本不會提供 [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) 介面的任何直接支援。

**鎖定的方法**

鎖定是用來保護多執行緒環境中 DMO 的狀態。 在 ATL 專案中， [**IMediaObject：： Lock**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-lock) 方法會導致名稱與 ATL **鎖定** 方法發生衝突。 若要解決此衝突，此範本會將 **IMediaObject** 方法重新命名為 **DMOLock**。 當您編譯衍生類別時，請先定義修正 \_ 鎖定 \_ 名稱，再將標頭檔包含在前面：


```C++
#define FIX_LOCK_NAME
#include <dmo.h>
```



這個指示詞會讓預處理器以 **DMOLock** 取代 **IMediaObject** 介面宣告中的 **鎖定**。 應用程式仍然可以使用名稱 **鎖定** 來叫用方法，因為 vtable 順序不會變更。 **DMOLock** 方法會呼叫衍生類別的 **鎖定** 或 **解除鎖定**。 如果您使用 ATL 來執行衍生類別，則這些方法已由 ATL 定義，因此不需要額外的程式碼。 如果您不是使用 ATL，則必須在衍生類別中提供 **鎖定** 和 **解除** 鎖定方法。

此範本會自動鎖定每個 **IMediaObject** 方法中的 DMO。 衍生類別可能需要鎖定其所執行 (之其他公用方法內的 DMO （例如，如果它支援 **IMediaObjectInPlace**) ）。 類別樣板也會提供內部 helper 類別 [**IMediaObjectImpl：： LockIt**](imediaobjectimpl-lockit.md)，這適用于鎖定和解除鎖定 DMO。

**總結**

針對下列 **IMediaObject** 方法，範本會在衍生類別上使用相同的簽章來呼叫對應的方法。 衍生的類別必須執行第二個數據行中顯示的每個方法。



| IMediaObject 方法            | 衍生類別方法                   |
|--------------------------------|----------------------------------------|
| **AllocateStreamingResources** | **InternalAllocateStreamingResources** |
| **間斷**              | **InternalDiscontinuity**              |
| **清除**                      | **InternalFlush**                      |
| **FreeStreamingResources**     | **InternalFreeStreamingResources**     |
| **GetInputMaxLatency**         | **InternalGetInputMaxLatency**         |
| **GetInputSizeInfo**           | **InternalGetInputSizeInfo**           |
| **GetInputStreamInfo**         | **InternalGetInputStreamInfo**         |
| **GetInputType**               | **InternalGetInputType**               |
| **GetOutputSizeInfo**          | **InternalGetOutputSizeInfo**          |
| **GetOutputStreamInfo**        | **InternalGetOutputStreamInfo**        |
| **GetOutputType**              | **InternalGetOutputType**              |
| **ProcessInput**               | **InternalProcessInput**               |
| **ProcessOutput**              | **InternalProcessOutput**              |
| **SetInputMaxLatency**         | **InternalSetInputMaxLatency**         |



 

針對其餘的 **IMediaObject** 方法，範本方法與衍生類別方法之間不會有一對一的對應關係。 下表摘要說明範本完全執行的方法，以及在衍生類別上呼叫其他方法的方法。



| IMediaObject 方法                   | 衍生類別方法                                                             |
|---------------------------------------|----------------------------------------------------------------------------------|
| **GetInputCurrentType**               | 完全實作為                                                                |
| **GetOutputCurrentType**              | 完全實作為                                                                |
| **GetStreamCount**                    | 完全實作為                                                                |
| **GetInputStatus**                    | [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))        |
| **鎖定** (實作為 **DMOLock**)  | [**鎖定**](/previous-versions/ms809100(v=msdn.10))， [**解除** 鎖定](/previous-versions/ms809101(v=msdn.10)) |
| **SetInputType**                      | [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))        |
| **SetOutputType**                     | [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMediaObjectImpl 類別範本**](imediaobjectimpl-class-template.md)
</dt> <dt>

[撰寫 DMO](writing-a-dmo.md)
</dt> </dl>

 

 
