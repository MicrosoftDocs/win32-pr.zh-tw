---
title: 在 DirectML 中繫結
description: 在 DirectML 中，系結指的是在初始化和執行機器學習運算子期間，要用於 GPU 的管線附加資源。
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: a04bf0bcc63fff810604e3db72fe507cc10040f5
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "104548398"
---
# <a name="binding-in-directml"></a>在 DirectML 中繫結

在 DirectML 中 *，系* 結指的是在初始化和執行機器學習運算子期間，要用於 GPU 的管線附加資源。 例如，這些資源可以是輸入和輸出張量，以及操作員需要的任何暫存或持續性資源。

本主題將討論系結的概念和程式詳細資料。 建議您也完整閱讀您所呼叫之 Api 的檔，包括參數和備註。

## <a name="important-ideas-in-binding"></a>系結中的重要概念

下列步驟清單包含系結相關工作的高階描述。 每次執行[dispatchable](/windows/desktop/api/directml/nn-directml-idmldispatchable)時，您都必須遵循這些步驟， &mdash; dispatchable 是操作員初始化運算式或已編譯的運算子。 這些步驟會介紹 DirectML 系結所涉及的重要概念、結構和方法。

本主題的後續章節會更詳細地深入探討這些系結工作，並提供從 [最基本 DirectML 應用程式程式](dml-min-app.md) 代碼範例取得的說明程式碼片段。

- 在 dispatchable 上呼叫 [**IDMLDispatchable：： GetBindingProperties**](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) ，以判斷它需要多少描述項，以及其暫存/持續性資源需求。
- 為描述項建立夠大的 Direct3D 12 描述元堆積，並將其系結至管線。
- 呼叫 [**IDMLDevice：： CreateBindingTable**](/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable) 來建立 DirectML 系結資料表，以代表系結至管線的資源。 使用 [**DML_BINDING_TABLE_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc) 結構來描述您的系結資料表，包括它在描述元堆積中指向之描述項的子集。
- 以 Direct3D 12 緩衝區資源的形式建立暫存/持續性資源，使用 [**DML_BUFFER_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_binding) 和 [**DML_BINDING_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_desc) 結構來描述它們，然後將它們加入至系結資料表。
- 如果 dispatchable 是已編譯的運算子，請建立 tensor 專案的緩衝區作為 Direct3D 12 緩衝區資源。 填入/上傳它、使用 **DML_BUFFER_BINDING** 和 **DML_BINDING_DESC** 結構來描述它，然後將它加入至系結資料表。
- 當您呼叫 [**IDMLCommandRecorder：： RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)時，將您的系結資料表當作參數傳遞。

## <a name="retrieve-the-binding-properties-of-a-dispatchable"></a>取出 dispatchable 的系結屬性

[**DML_BINDING_PROPERTIES**](/windows/desktop/api/directml/ns-directml-dml_binding_properties)結構描述 dispatchable (運算子初始化運算式或編譯的運算子) 的系結需求。 這些系結相關屬性包含您應系結至 dispatchable 的描述項數目，以及它所需的任何暫存和/或持續性資源的大小（以位元組為單位）。

> [!NOTE]
> 即使是相同類型的多個運算子，也請勿對具有相同系結需求的運算子進行假設。 查詢您所建立之每個初始化運算式和運算子的系結屬性。

呼叫 [**IDMLDispatchable：： GetBindingProperties**](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) 來取出 **DML_BINDING_PROPERTIES**。

```cppwinrt
winrt::com_ptr<::IDMLCompiledOperator> dmlCompiledOperator;
// Code to create and compile a DirectML operator goes here.

DML_BINDING_PROPERTIES executeDmlBindingProperties{
    dmlCompiledOperator->GetBindingProperties()
};

winrt::com_ptr<::IDMLOperatorInitializer> dmlOperatorInitializer;
// Code to create a DirectML operator initializer goes here.

DML_BINDING_PROPERTIES initializeDmlBindingProperties{
    dmlOperatorInitializer->GetBindingProperties()
};

UINT descriptorCount = ...
```

您在此處抓取的 `descriptorCount` 值會 (決定描述項堆積的大小下限，以及您在接下來的兩個步驟中所建立之系結資料表的) 大小下限。

**DML_BINDING_PROPERTIES** 也包含 `TemporaryResourceSize` 成員，這是暫存資源的大小下限（以位元組為單位），必須系結至這個 dispatchable 物件的系結資料表。 值為零表示不需要暫存資源。

以及 `PersistentResourceSize` 成員，這是持續性資源的最小大小（以位元組為單位），必須系結至這個 dispatchable 物件的系結資料表。 值為零表示不需要持續性資源。 如果需要持續性資源，則必須在初始化編譯運算子期間提供持續性資源， (其系結為運算子初始化運算式的輸出) 和執行期間。 本主題稍後會有更多相關資訊。 只有編譯的運算子具有持續性資源，運算子初始化運算式一律會傳回這個成員的0值。

如果您在呼叫 [**IDMLOperatorInitializer：： Reset**](/windows/desktop/api/directml/nf-directml-idmloperatorinitializer-reset)之前和之後呼叫運算子初始化運算式上的 **IDMLDispatchable：： GetBindingProperties** ，就不保證會將兩組系結屬性視為相同。

## <a name="describe-create-and-bind-a-descriptor-heap"></a>描述、建立和系結描述項堆積

就描述項而言，您的責任會以描述項堆積本身為開頭和結尾。 DirectML 本身會負責建立及管理您所提供之堆積內的描述項。

因此，請使用 [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) 結構來描述已夠大的堆積，以滿足 dispatchable 所需的描述項數目。 然後使用 [**ID3D12Device：： CreateDescriptorHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)來建立它。 最後，呼叫 [**ID3D12GraphicsCommandList：： SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) ，將描述元堆積系結至管線。

```cppwinrt
winrt::com_ptr<::ID3D12DescriptorHeap> d3D12DescriptorHeap;

D3D12_DESCRIPTOR_HEAP_DESC descriptorHeapDescription{};
descriptorHeapDescription.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
descriptorHeapDescription.NumDescriptors = descriptorCount;
descriptorHeapDescription.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;

winrt::check_hresult(
    d3D12Device->CreateDescriptorHeap(
        &descriptorHeapDescription,
        _uuidof(d3D12DescriptorHeap),
        d3D12DescriptorHeap.put_void()
    )
);

std::array<ID3D12DescriptorHeap*, 1> d3D12DescriptorHeaps{ d3D12DescriptorHeap.get() };
d3D12GraphicsCommandList->SetDescriptorHeaps(
    static_cast<UINT>(d3D12DescriptorHeaps.size()),
    d3D12DescriptorHeaps.data()
);
```

## <a name="describe-and-create-a-binding-table"></a>描述並建立系結資料表

DirectML 系結表代表您系結至管線以供 dispatchable 使用的資源。 這些資源可以是輸入和輸出張量 (或針對操作員) 的其他參數，也可以是 dispatchable 可搭配使用的各種持續性和暫存資源。

使用 [**DML_BINDING_TABLE_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc) 結構來描述您的系結資料表，包括系結資料表將代表系結的 dispatchable，以及從您剛才建立的描述元堆積 (的描述項範圍，) 您希望系結資料表參考 (，以及 DirectML 可能寫入描述項) 。 `descriptorCount`值 (我們在第一個步驟中取得的其中一個系結屬性，) 告訴我們 dispatchable 物件所需之系結資料表的最小大小。 在這裡，我們會使用該值來指出從提供的 CPU 和 GPU 描述項控制碼的開頭，DirectML 可寫入至堆積的最大描述項數目上限。

然後呼叫 [**IDMLDevice：： CreateBindingTable**](/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable) 來建立 DirectML 系結資料表。 在稍後的步驟中，我們為 dispatchable 建立了更多資源之後，我們會將這些資源新增至系結資料表。

您可以傳遞，表示空的系結表，而不是將 **DML_BINDING_TABLE_DESC** 傳遞給這個呼叫 `nullptr` 。

```cppwinrt
DML_BINDING_TABLE_DESC dmlBindingTableDesc{};
dmlBindingTableDesc.Dispatchable = dmlOperatorInitializer.get();
dmlBindingTableDesc.CPUDescriptorHandle = d3D12DescriptorHeap->GetCPUDescriptorHandleForHeapStart();
dmlBindingTableDesc.GPUDescriptorHandle = d3D12DescriptorHeap->GetGPUDescriptorHandleForHeapStart();
dmlBindingTableDesc.SizeInDescriptors = descriptorCount;

winrt::com_ptr<::IDMLBindingTable> dmlBindingTable;
winrt::check_hresult(
    dmlDevice->CreateBindingTable(
        &dmlBindingTableDesc,
        __uuidof(dmlBindingTable),
        dmlBindingTable.put_void()
    )
);
```

DirectML 將描述元寫入堆積的順序並未指定，因此您的應用程式必須小心不要覆寫系結資料表所包裝的描述項。 提供的 CPU 和 GPU 描述項控制碼可能來自不同的堆積，不過，您的應用程式會負責確保 CPU 描述項控制碼所參考的整個描述元範圍，在執行之前，會使用此系結表複製到 GPU 描述控制碼所參考的範圍。 提供控制碼的描述元堆積必須具有類型 **D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV**。 此外，所參考的堆積 `GPUDescriptorHandle` 必須是著色器可見的描述元堆積。

您可以重設系結資料表來移除您已新增至其中的任何資源，同時變更您在初始 **DML_BINDING_TABLE_DESC** (設定的任何屬性，以包裝新的描述項範圍，或針對不同的 dispatchable) 重複使用它。 您只需對 description 結構進行變更，然後呼叫 [**IDMLBindingTable：： Reset**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-reset)。

```cppwinrt
dmlBindingTableDesc.Dispatchable = pIDMLCompiledOperator.get();

winrt::check_hresult(
    pIDMLBindingTable->Reset(
        &dmlBindingTableDesc
    )
);
```

## <a name="describe-and-bind-any-temporarypersistent-resources"></a>描述及系結任何暫存/持續性資源

我們在抓取 dispatchable 的系結 [屬性](#retrieve-the-binding-properties-of-a-dispatchable)時，所填入的 **DML_BINDING_PROPERTIES** 結構包含 dispatchable 所需的任何暫存和/或持續性資源的大小（以位元組為單位）。 如果其中一種大小不是零，則請建立 Direct3D 12 緩衝區資源，並將它加入至系結資料表。

在下列程式碼範例中，我們會建立 `temporaryResourceSize` dispatchable 大小) 的暫存資源 (位元組。 我們會說明要如何系結資源，然後再將該系結新增至系結資料表。

因為我們要系結單一緩衝區資源，所以我們會使用 [**DML_BUFFER_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_binding) 結構來描述系結。 在該結構中，我們會指定 Direct3D 12 緩衝區資源 (資源必須有 [**D3D12_RESOURCE_DIMENSION_BUFFER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)) 的維度，以及緩衝區中的位移和大小。 您也可以描述緩衝區陣列的系結 (而不是單一緩衝區) 的系結，而且該用途有 [**DML_BUFFER_ARRAY_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_array_binding) 結構。

為了抽象化緩衝區系結與緩衝區陣列系結之間的差異，我們使用  [**DML_BINDING_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_desc) 結構。 您可以將 `Type` **DML_BINDING_DESC** 的成員設定為 [**DML_BINDING_TYPE_BUFFER**](/windows/desktop/api/directml/ne-directml-dml_binding_type) 或 **DML_BINDING_TYPE_BUFFER_ARRAY**。 然後，您可以設定 `Desc` 成員指向 **DML_BUFFER_BINDING** 或 **DML_BUFFER_ARRAY_BINDING**，取決於 `Type` 。

我們正在處理此範例中的暫存資源，因此我們會呼叫 [**IDMLBindingTable：： BindTemporaryResource**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindtemporaryresource)，將它新增至系結資料表。

```cppwinrt
D3D12_HEAP_PROPERTIES defaultHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT) };
winrt::com_ptr<::ID3D12Resource> temporaryBuffer;

D3D12_RESOURCE_DESC temporaryBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(temporaryResourceSize) };
winrt::check_hresult(
    d3D12Device->CreateCommittedResource(
        &defaultHeapProperties,
        D3D12_HEAP_FLAG_NONE,
        &temporaryBufferDesc,
        D3D12_RESOURCE_STATE_COMMON,
        nullptr,
        __uuidof(temporaryBuffer),
        temporaryBuffer.put_void()
    )
);

DML_BUFFER_BINDING bufferBinding{ temporaryBuffer.get(), 0, temporaryResourceSize };
DML_BINDING_DESC bindingDesc{ DML_BINDING_TYPE_BUFFER, &bufferBinding };
dmlBindingTable->BindTemporaryResource(&bindingDesc);
```

暫存資源 (如果需要的話) 是在執行運算子期間于內部使用的臨時記憶體，因此您不需要擔心其內容。 您也必須在 GPU 上的 [**IDMLCommandRecorder：： RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) 呼叫完成之後，再繼續進行。 這表示您的應用程式可能會在已編譯運算子的分派之間釋放或覆寫暫存資源。 所提供要系結為暫存資源的緩衝區範圍，其起始位移必須與 [**DML_TEMPORARY_BUFFER_ALIGNMENT**](./direct3d-directml-constants.md)一致。 緩衝區基礎的堆積型別必須是 **D3D12_HEAP_TYPE_DEFAULT**。

但是，如果 dispatchable 針對其較長時間持續的資源報告非零的大小，則程式會稍有不同。 您應建立緩衝區，並依照上面所示的相同模式來描述系結。 但是，您可以呼叫 [**IDMLBindingTable：： BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs)，將它加入操作員初始化運算式的系結表，因為這是運算子初始化運算式的作業，可將持續性資源初始化。 然後使用 [**IDMLBindingTable：： BindPersistentResource**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindpersistentresource)的呼叫，將它新增至已編譯運算子的系結資料表。 請參閱 [最基本的 DirectML 應用程式程式](dml-min-app.md) 代碼範例，以查看此工作流程的實際運作情形。 持續性資源的內容和存留期必須保存，只要經過編譯的運算子就能完成。 亦即，如果操作員需要持續性資源，則您的應用程式必須在初始化期間提供它，然後再將其提供給運算子的所有未來執行，而不需要修改其內容。 DirectML 通常會使用持續性資源來儲存查閱資料表或其他長期存留的資料，這些資料會在初始化操作員時計算，並在該運算子的未來執行時重複使用。 要系結的所提供緩衝區範圍必須與 [**DML_PERSISTENT_BUFFER_ALIGNMENT**](./direct3d-directml-constants.md)的起始位移相符。 緩衝區基礎的堆積型別必須是 **D3D12_HEAP_TYPE_DEFAULT**。

## <a name="describe-and-bind-any-tensors"></a>描述及系結任何張量

如果您要處理編譯的運算子 (而不是使用運算子初始化運算式) ，則您需要將輸入和輸出資源 (系結至運算子的系結資料表) 的張量和其他參數。 系結數目必須完全符合運算子的輸入數目，包括選擇性的張量。 運算子所採用的特定輸入和輸出張量和其他參數，會記載于該運算子的主題 (例如 [**DML_ELEMENT_WISE_IDENTITY_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_identity_operator_desc)) 。

Tensor 資源是一個緩衝區，其中包含 tensor 的個別元素值。 您可以使用一般的 Direct3D 12 技巧，在 GPU 上傳和讀回這類緩衝區， ([上傳資源](/windows/desktop/direct3d12/uploading-resources) 並透過 [緩衝區) 讀回資料](/windows/desktop/direct3d12/readback-data-using-heaps) 。 請參閱 [最基本的 DirectML 應用程式程式](dml-min-app.md) 代碼範例，以瞭解這些技術的實際運作方式。

最後，使用 **DML_BUFFER_BINDING** 和 **DML_BINDING_DESC** 結構來描述您的輸入和輸出資源系結，然後使用 [**IDMLBindingTable：： BindInputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindinputs) 和 [**IDMLBindingTable：： BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs)的呼叫，將它們新增至已編譯運算子的系結資料表。 當您呼叫 **IDMLBindingTable：： Bind \** _ 方法時，DirectML 會將一個或多個描述元寫入至 CPU 描述項的範圍。

```cppwinrt
DML_BUFFER_BINDING inputBufferBinding{ inputBuffer.get(), 0, tensorBufferSize };
DML_BINDING_DESC inputBindingDesc{ DML_BINDING_TYPE_BUFFER, &inputBufferBinding };
dmlBindingTable->BindInputs(1, &inputBindingDesc);

DML_BUFFER_BINDING outputBufferBinding{ outputBuffer.get(), 0, tensorBufferSize };
DML_BINDING_DESC outputBindingDesc{ DML_BINDING_TYPE_BUFFER, &outputBufferBinding };
dmlBindingTable->BindOutputs(1, &outputBindingDesc);
```

建立 DirectML 運算子的其中一個步驟 (請參閱 [_ *IDMLDevice：： CreateOperator* *](/windows/desktop/api/directml/nf-directml-idmldevice-createoperator)) 是宣告一或多個 [**DML_BUFFER_TENSOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc)結構，以描述該運算子所採用和傳回的 TENSOR 資料緩衝區。 您也可以選擇性地指定 [**DML_TENSOR_FLAG_OWNED_BY_DML**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags) 旗標，以及 tensor 緩衝區的型別和大小。

**DML_TENSOR_FLAG_OWNED_BY_DML** 表示 TENSOR 資料應該由 DirectML 擁有及管理。 DirectML 會在運算子的初始化期間建立 tensor 資料的複本，並將它儲存在持續性資源中。 這可讓 DirectML 將 tensor 資料的重新格式化為其他、更有效率的表單。 設定此旗標可能會提高效能，但它通常只適用于張量 (運算子存留期不會變更的資料，例如權數張量) 。 而且旗標只可用於輸入張量。 在特定 tensor 描述上設定旗標時，對應的 tensor 必須系結至運算子初始化期間的系結表，而不是在執行期間執行 (這會導致錯誤) 。 這與預設行為相反， (沒有 DML_TENSOR_FLAG_OWNED_BY_DML 旗標) 的行為，其中 TENSOR 預期會在執行期間系結，而不會在初始化期間進行系結。 當您將 tensor 資料提供給運算子初始化運算式時，系結上傳（而非預設堆積）是合法的，因為 DirectML 會建立資料的複本。 在所有其他情況下，系結至 DirectML 的所有資源都必須是預設堆積資源。

如需詳細資訊，請參閱 [**IDMLBindingTable：： BindInputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindinputs) 和 [**IDMLBindingTable：： BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs)。

## <a name="execute-the-dispatchable"></a>執行 dispatchable

當您呼叫 [**IDMLCommandRecorder：： RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)時，將您的系結資料表當作參數傳遞。

當您在呼叫 **IDMLCommandRecorder：： RecordDispatch** 期間使用系結資料表時，DirectML 會將對應的 GPU 描述元系結至管線。 CPU 和 GPU 描述項控制碼不需要指向描述項堆積中的相同專案，不過您的應用程式會負責確保 CPU 描述項控制碼所參考的整個描述元範圍，在執行之前，會使用此系結表複製到 GPU 描述控制碼所參考的範圍。

```cppwinrt
winrt::com_ptr<::ID3D12GraphicsCommandList> d3D12GraphicsCommandList;
// Code to create a Direct3D 12 command list goes here.

winrt::com_ptr<::IDMLCommandRecorder> dmlCommandRecorder;
// Code to create a DirectML command recorder goes here.

dmlCommandRecorder->RecordDispatch(
    d3D12GraphicsCommandList.get(),
    dmlOperatorInitializer.get(),
    dmlBindingTable.get()
);
```

最後，關閉您的 Direct3D 12 命令清單，然後提交以供執行，就像任何其他命令清單一樣。

在 GPU 上執行 **RecordDispatch** 之前，您必須將所有的系結資源轉換為 **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** 狀態，或轉換成可隱含提升為 **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** 的狀態，例如 **D3D12_RESOURCE_STATE_COMMON**。 此呼叫完成後，資源會維持 **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** 狀態。 唯一的例外是在執行運算子初始化運算式時所系結的上傳堆積，以及一或多個張量已設定 **DML_TENSOR_FLAG_OWNED_BY_DML** 旗標。 在這種情況下，任何針對輸入系結的上傳堆積都必須處於 **D3D12_RESOURCE_STATE_GENERIC_READ** 狀態，而且會維持在該狀態中，如所有上傳堆積的要求。 如果在編譯運算子時未設定 **DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE** ，則在呼叫 **RecordDispatch** 之前，必須在系結資料表上設定所有系結，否則行為是未定義的。 否則，如果操作員支援 [晚期繫結](#optionally-specify-late-bound-operator-bindings)，則可能會延遲資源的系結，直到將 Direct3D 12 命令清單提交到命令佇列以供執行為止。

**RecordDispatch** 的作用就像是呼叫 [**ID3D12GraphicsCommandList：:D ispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)。 因此，如果分派之間有資料相依性，則需要 (UAV) 阻礙的未排序存取權，以確保正確的順序。 這個方法不會在輸入或輸出資源上插入 UAV 障礙。 您的應用程式必須確保在任何輸入上都執行正確的 UAV 障礙（如果其內容相依于上游分派），以及在任何輸出上有相依于這些輸出的下游分派時執行。

## <a name="lifetime-and-synchronization-of-descriptors-and-binding-table"></a>描述元和系結資料表的存留期和同步處理

DirectML 中系結的良好觀念是在幕後，DirectML 系結資料表本身是在您提供的描述元堆積內建立和管理未排序的存取權 (UAV 的) 描述項。 因此，所有常用的 Direct3D 12 規則都適用于同步處理該堆積的存取權，以及其描述項。 您的應用程式必須負責在使用系結資料表的 CPU 和 GPU 工作之間執行正確的同步處理。

在先前的框架 (使用描述元時，系結資料表無法覆寫描述項，例如) 。 因此，如果您想要重複使用已系結的描述元堆積 (例如，藉由在指向它的系結表上再次呼叫 Bind *，或是以手動方式覆寫描述元堆積) ，您應該等候目前使用描述元堆積的 dispatchable 完成 GPU 上的執行。 系結資料表不會在其所寫入的描述元堆積上維護強式參考，因此您不得釋放支援著色器可見的描述元堆積，直到使用該系結資料表的所有工作都已在 GPU 上完成執行為止。

另一方面，雖然系結資料表會指定和管理描述元堆積，但資料表本身本身並不 *包含* 任何記憶體。 因此，您可以在呼叫 [**IDMLCommandRecorder：： RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) 之後，隨時釋放或重設系結資料表 (您不需要等待該呼叫在 GPU 上完成，只要基礎描述項仍維持有效的) 。

系結資料表不會在任何系結的資源上保留強式參考 &mdash; ，您的應用程式必須確保在 GPU 仍在使用時，不會刪除資源。 此外，系結資料表不具備安全線程， &mdash; 您的應用程式不能同時從不同的執行緒呼叫系結資料表上的方法，而不需要同步處理。

而且，請考慮在任何情況下，只有當您變更要系結的資源時，才需要重新系結。 如果您不需要變更系結的資源，則可以在啟動時系結一次，並在每次呼叫 **RecordDispatch** 時傳遞相同的系結表。

針對交錯的機器學習和轉譯工作負載，只需確定每個框架的系結資料表都指向未在 GPU 上使用的描述元堆積範圍。

## <a name="optionally-specify-late-bound-operator-bindings"></a>選擇性地指定晚期繫結運算子系結

如果您要處理編譯的運算子 (而不是使用運算子初始化運算式) ，您可以選擇指定運算子的晚期繫結。 如果沒有晚期繫結，您必須先設定系結資料表上的所有系結，再將運算子記錄到命令清單中。 使用晚期繫結時，您可以在已記錄到命令佇列中的運算子上，設定 (或變更) 系結，然後再提交至命令佇列。

若要指定晚期繫結，請使用 DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE 的引數來呼叫 [**IDMLDevice：： CompileOperator**](/windows/win32/api/directml/nf-directml-idmldevice-compileoperator) `flags` 。 [](/windows/desktop/api/directml/ne-directml-dml_execution_flags)