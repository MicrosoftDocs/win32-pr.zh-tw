---
title: 根簽章版本1。1
description: 根簽章版本1.1 的目的是要讓應用程式向驅動程式指出描述項堆積中的描述項不會變更，或資料描述元指向不會變更。
ms.assetid: 8FE42C1C-7F1D-4E70-A7EE-D5EC67237327
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a7a32576efa4d93a8d26aa57282f06e0d5a02f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343663"
---
# <a name="root-signature-version-11"></a>根簽章版本1。1

根簽章版本1.1 的目的是要讓應用程式向驅動程式指出描述項堆積中的描述項不會變更，或資料描述元指向不會變更。 如此一來，驅動程式的選項就能進行優化，以瞭解描述項或所指向的記憶體在一段時間內是靜態的。

-   [概觀](#overview)
-   [靜態和 Volatile 旗標](#static-and-volatile-flags)
    -   [描述項 \_ VOLATILE](#descriptors_volatile)
    -   [資料 \_ VOLATILE](#data_volatile)
    -   [\_ \_ \_ \_ 在執行時設定靜態 \_ 資料](#data_static_while_set_at_execute)
    -   [資料 \_ 靜態](#data_static)
    -   [組合旗標](#combining-flags)
    -   [旗標摘要](#flag-summary)
-   [版本 1.1 API 摘要](#version-11-api-summary)
    -   [列舉](#enums)
    -   [結構](#helper-structures)
    -   [函數](#functions)
    -   [方法](#methods)
    -   [Helper 結構](#helper-structures)
-   [違反靜態性質旗標的後果](#consequences-of-violating-static-ness-flags)
-   [版本管理](#version-management)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

根簽章版本1.0 可讓應用程式的內容堆積的內容，以及它們所指向的記憶體，隨時都可供應用程式在 GPU 上進行參考的命令清單/組合時自由變更。 不過，通常應用程式在記錄參考它們的命令之後，不需要彈性變更描述元或記憶體。

應用程式通常完整能夠：

-   設定描述元 (以及它們在命令清單或組合上系結描述項資料表或根描述元之前所指向) 的記憶體。
-   請確定這些描述項在參考它們的命令清單/bundles 完成最後一次執行之後，才會變更。
-   請確定描述元指向的資料在相同的完整持續時間內不會變更。

或者，應用程式只能接受該資料不會在較短的時間內變更。 在命令清單執行期間，在命令清單執行期間，特定資料可能會是靜態的，因為根參數系結 (描述中繼資料表或根描述元) 目前指向資料。 換句話說，應用程式可能會想要在 GPU 時間軸上執行執行，以在透過根參數設定資料的期間內更新某些資料，並瞭解設定它將是靜態的時候。

如果描述項或資料描述項指向，將不會變更，則特定的優化驅動程式可能會是硬體廠商專屬的，而且重要的是，它們不會變更可能會改善效能的行為。 盡可能保留最多應用程式意圖的知識，並不會對應用程式造成負擔。

其中一個優化是許多驅動程式如果知道應用程式可以對描述項和資料的靜態性質產生的保證，就可以產生更有效率的記憶體存取。 例如，如果特定硬體不區分根引數的大小，則驅動程式可以藉由將堆積中的描述項轉換成根描述項，來移除其存取層級的間接取值層級。

使用1.1 版的開發人員所做的額外工作，是盡可能地針對資料的變動性和靜態性質做出承諾，讓驅動程式能夠進行優化。 開發人員不需要對靜態性質做出任何承諾。

因為重新編譯根簽章的應用程式預設為根簽章1.1，所以現在 (有必要的選項可強制執行 1.0) ，所以根簽章版本1.0 會繼續運作。

## <a name="static-and-volatile-flags"></a>靜態和 Volatile 旗標

下列旗標是根簽章的一部分，可讓驅動程式選擇在設定個別根引數時，如何最好處理這些引數的策略，並同時將相同的假設內嵌至管線狀態物件 (Pso 在原始編譯時) ，因為根簽章是 PSO 的一部分。

下列旗標是由應用程式所設定，並套用至描述項或資料。

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_FLAGS
{
    D3D12_DESCRIPTOR_RANGE_FLAG_NONE    = 0,
    D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE    = 0x1,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_VOLATILE   = 0x2,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE    = 0x4,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC = 0x8
} D3D12_DESCRIPTOR_RANGE_FLAGS;

typedef enum D3D12_ROOT_DESCRIPTOR_FLAGS
{
    D3D12_ROOT_DESCRIPTOR_FLAG_NONE = 0,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE    = 0x2,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE = 0x4,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC  = 0x8
} D3D12_ROOT_DESCRIPTOR_FLAGS;
```

### <a name="descriptors_volatile"></a>描述項 \_ VOLATILE

在設定此旗標之後，應用程式可以隨時變更根描述中繼資料表所指向之描述元堆積中的描述元，但不包括系結描述項資料表的命令清單/組合已提交，而且尚未完成執行。 例如，在提交命令清單以便執行 *之前* ，記錄命令清單以及後續變更描述項堆積中的描述項。 這是根簽章1.0 版唯一支援的行為。

如果 \_ *未* 設定描述項 VOLATILE 旗標，則描述項是靜態的。 此模式沒有旗標。 靜態描述項表示在記錄) 時，根描述中繼資料表所指向之描述元堆積中的描述元已 (初始化，而描述項必須等到命令清單/組合完成最後一次執行之後才能變更。 *針對根簽章版本1.1，靜態描述項是預設假設*，而且應用程式必須 \_ 在必要時指定描述項 VOLATILE 旗標。

針對使用具有靜態描述項之描述項資料表的組合，在記錄套件組合 (時，必須準備好描述項，而不是在套件組合被) 呼叫時進行變更，而不會在套件組合完成最後一次執行之前變更。 指向靜態描述元的描述中繼資料表必須在套件組合記錄期間設定，而不會繼承到組合。 命令清單若要使用描述中繼資料表，以及已在組合中設定並傳回命令清單的靜態描述項，這是有效的。

當描述項為靜態時，需要設定描述項 VOLATILE 旗標的另一個行為變更 \_ 。 除了 Texture1D/2D/3D/Cube 視圖之外，外 (任何緩衝區視圖的界限存取) 無效，並產生未定義的結果（包括可能的裝置重設），而不是傳回讀取或卸載寫入的預設值。 若要移除應用程式相依于硬體超出範圍存取檢查的能力，可讓驅動程式選擇將靜態描述項存取權升階到根描述項存取，如果它們認為較有效率。 根描述項不支援任何超出範圍的檢查。

如果應用程式在存取描述項時相依于不限時的記憶體存取行為，則必須將存取這些描述項的描述項範圍標記為描述項 \_ VOLATILE。

### <a name="data_volatile"></a>資料 \_ VOLATILE

設定此旗標之後，CPU 可以隨時變更由描述元所指向的資料，但不包括系結描述項資料表的命令清單/組合已提交，而且尚未完成執行。 這是根簽章1.0 版唯一支援的行為。

旗標適用于兩個描述項範圍旗標和根描述元旗標。

### <a name="data_static_while_set_at_execute"></a>\_ \_ \_ \_ 在執行時設定靜態 \_ 資料

設定此旗標之後，如果在 GPU 時間軸上執行時，在命令清單/套件組合上設定基礎根目錄描述元或描述中繼資料表，且在後續的繪製/分派將不再參考資料時，就無法從開始變更描述項所指向的資料。

在 GPU 上設定根描述元或描述中繼資料表之前，您甚至 *可以* 透過相同的命令清單/套件組合來變更此資料。 當根描述元或描述中繼資料表指向該資料時，也會在命令清單/套件組合上進行變更，只要繪製/分派參考它已完成。 不過，這樣做需要在下一次參考根描述元或描述中繼資料表之前，再次將描述中繼資料表重新綁定至命令清單。 這可讓驅動程式知道根描述元或描述中繼資料表所指向的資料已經變更。

在「執行」和「資料 volatile」設定時，資料靜態之間的基本差異在於 \_ \_ \_ \_ \_ \_ 資料 \_ volatile 驅動程式無法判斷命令清單中的資料複製是否已變更描述項所指向的資料，而不需要進行額外的狀態追蹤。 比方說，如果驅動程式可以將任何類型的資料預先提取命令插入其命令清單中 (以便讓著色器存取已知資料更有效率，例如) ， \_ \_ \_ 在執行時設定的資料靜態 \_ ， \_ 可讓驅動程式知道它只需要在透過 [**SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable)、 [**SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) 或其中一個方法設定常數緩衝區視圖、著色器資源檢視器或未排序的存取權時，執行預先提取資料。

針對套件組合，在執行設定時，資料為靜態的保證會在每次執行組合時單獨套用。

旗標適用于兩個描述項範圍旗標和根描述元旗標。

### <a name="data_static"></a>資料 \_ 靜態

如果設定此旗標，則由描述項所指向的資料已在錄製期間于命令清單/套件組合上設定了參考記憶體的根描述元或描述中繼資料表，且資料必須等到命令清單/組合最後一次執行之後才能變更。

針對套件組合，靜態持續時間會在記錄套件組合期間從根描述元或描述中繼資料表設定開始，而不是錄製呼叫命令清單。 此外，也必須在組合中設定指向靜態資料的描述中繼資料表，而不是繼承。 命令清單可以使用描述中繼資料表，指向已在組合中設定並傳回至命令清單的靜態資料，這是有效的。

旗標適用于兩個描述項範圍旗標和根描述元旗標。

### <a name="combining-flags"></a>組合旗標

一次最多隻能指定一個資料旗標，但取樣器描述元範圍（不支援資料旗標）除外，因為取樣器不會指向資料。

如果 SRV 和 CBV 描述項範圍沒有任何資料旗標， \_ \_ \_ \_ \_ 則會假設為在執行行為時設定為靜態資料的預設值。 選擇此預設值而非資料靜態的原因 \_ 是， \_ 在執行時設定的靜態資料，在 \_ \_ \_ \_ 大部分的情況下都可能是安全的預設值，但仍會產生比預設為數據 VOLATILE 更好的一些優化商機 \_ 。

缺少 UAV 描述項範圍的資料旗標表示系統會假設使用預設的資料 \_ 變動行為，通常會將 UAVs 寫入。

描述項 \_ VOLATILE *無法* 與資料 \_ 靜態合併，但 *可以* 與其他資料旗標合併。 當您在執行時設定時，變動性描述元 \_ 可以與資料 \_ 靜態合併，因為 \_ \_ \_ \_ volatile 描述項在執行命令清單/套件組合時，仍需要描述項，而且 \_ 在執行時設定的資料靜態 \_ \_ \_ \_ 只會對命令清單/組合執行的子集內的靜態性質做出承諾。

### <a name="flag-summary"></a>旗標摘要

下表摘要說明可能採用的旗標組合。



| 有效的 D3D12 \_ 描述項 \_ 範圍 \_ 旗標設定                                                               | Description                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 未設定旗標                                                   | 描述項是靜態 (預設) 。 資料的預設假設：針對 SRV/CBV： \_ \_ 在執行時設定的資料靜態 \_ \_ \_ ，以及 UAV：資料 \_ VOLATILE。 SRV/CBV 的這些預設值會安全地符合大部分根簽章的使用模式。                                                                                              |
| 資料 \_ 靜態                                                   | 描述元和資料都是靜態的。 這可將驅動程式優化的可能性最大化。                                                                                                                                                                                                                                                          |
| 資料 \_ VOLATILE                                                 | 描述項是靜態的，而且資料是暫時性的。                                                                                                                                                                                                                                                                                                     |
| \_ \_ \_ \_ 在執行時設定靜態 \_ 資料                          | 描述項是靜態的，而且資料是在執行時設定的靜態。                                                                                                                                                                                                                                                                                      |
| 描述項 \_ VOLATILE                                          | 描述項是暫時性的，而且會對資料進行預設假設：針對 SRV/CBV \_ ： \_ 在執行時設定的資料靜態 \_ \_ \_ ，以及 UAV：資料 \_ volatile。                                                                                                                                                                                              |
| 描述項 \_ VOLATILE VOLATILE \| 資料 \_ VOLATILE                        | 描述元和資料都是 volatile 的，相當於根簽章1.0。                                                                                                                                                                                                                                                                            |
| 描述 \_ \| \_ \_ \_ \_ 在執行時設定的 \_ VOLATILE 靜態資料 | 描述項是暫時性的，但請注意，在命令清單執行期間仍不允許變更。 因此，當您在執行期間透過根描述中繼資料表來設定資料為靜態時，可將資料變成靜態，而基礎描述項的有效時間比將資料承諾為靜態的時間更長。 |



 



| 有效的 D3D12 \_ 根目錄 \_ 描述元 \_ 旗標設定                                                  |  Description                                                                                                                                                                                                                 |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 未設定旗標                                      | 資料的預設假設：針對 SRV/CBV： \_ \_ 在執行時設定的資料靜態 \_ \_ \_ ，以及 UAV：資料 \_ VOLATILE。 SRV/CBV 的這些預設值會安全地符合大部分根簽章的使用模式。 |
| 資料 \_ 靜態                                      | 資料是靜態的，這是驅動程式優化的最佳潛力。                                                                                                                                                       |
| \_ \_ \_ \_ 在執行時設定靜態 \_ 資料             | 資料在執行時設定為靜態。                                                                                                                                                                              |
| 資料 \_ VOLATILE                                    | 相當於根簽章1.0。                                                                                                                                                                                 |



 

## <a name="version-11-api-summary"></a>版本 1.1 API 摘要

下列 API 呼叫會啟用1.1 版。

### <a name="enums"></a>列舉

這些列舉包含用來指定描述元和資料變動性的索引鍵旗標。

-   [**D3D \_根簽章 \_ \_ 版本**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version) ：版本識別碼。
-   [**D3D12 \_描述項 \_ 範圍 \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) ：判斷描述元或資料是否為 volatile 或靜態的旗標範圍。
-   [**D3D12 \_根 \_ 描述項 \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) ： [**D3D12 \_ 描述項 \_ 範圍 \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags)的類似旗標範圍，但只有資料旗標適用于根描述元。

### <a name="structures"></a>結構

從1.0 版 (更新的結構，) 包含變動性/靜態旗標的參考。

-   [**D3D12 \_功能 \_ 資料 \_ 根 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature) 簽章：將此結構傳遞給 [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) ，以檢查是否有根簽章版本1.1 支援。
-   [**D3D12 \_已建立版本的根簽章 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) ：可以保留任何版本的根簽章描述，而且是設計來搭配下列序列化/還原序列化函數使用。
-   這些結構相當於1.0 版中所使用的結構，並加入描述項範圍和根描述項的新旗標欄位：

    -   [**D3D12 \_ 根簽章 \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1)
    -   [**D3D12 \_ 描述項 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
    -   [**D3D12 \_ 根目錄 \_ 描述元 \_ TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
    -   [**D3D12 \_ 根 \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
    -   [**D3D12 \_ 根 \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

### <a name="functions"></a>函式

此處所列的方法會取代原始的 [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) 和 [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) 函式，因為它們是設計用來處理任何版本的根簽章。 序列化形式是傳遞至 [**CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API 的表單。 如果著色器是以根簽章撰寫的，則編譯的著色器會在其中包含已序列化的根簽章。

-   [**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) ：如果應用程式 Cti 產生 [**D3D12 \_ 版本的 \_ 根 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) 簽章資料結構，它必須使用這個函式來建立序列化的表單。
-   [**D3D12CreateVersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) ：產生可透過 [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc)傳回還原序列化之資料結構的介面。

### <a name="methods"></a>方法

會建立 [**ID3D12VersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) 介面，將根簽章資料結構還原序列化。

-   [**GetRootSignatureDescAtVersion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getrootsignaturedescatversion) ：將根簽章描述結構轉換為要求的版本。
-   [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc) ：傳回 [**D3D12 版本根簽章 \_ \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) 結構的指標。

### <a name="helper-structures"></a>Helper 結構

已新增協助程式結構，以協助初始化某些版本1.1 結構。

-   CD3DX12 \_ 描述項 \_ RANGE1
-   CD3DX12 \_ 根 \_ PARAMETER1
-   CD3DX12 \_ 靜態 \_ SAMPLER1
-   CD3DX12 已建立版本的根簽章 \_ \_ \_ \_ DESC

請參閱 [Helper 結構和函式以進行 D3D12](helper-structures-and-functions-for-d3d12.md)。

## <a name="consequences-of-violating-static-ness-flags"></a>違反靜態性質旗標的後果

上述的描述元和資料旗標 (以及缺少特定旗標所隱含的預設值) 定義應用程式對驅動程式的承諾，以瞭解其行為。 如果應用程式違反承諾，則這是不正確行為：結果未定義，而且在不同的驅動程式和硬體之間可能不同。

Debug 層有一些選項，可驗證應用程式是否遵守其承諾，包括使用根簽章版本1.1 的預設承諾，而不需要設定任何旗標。

## <a name="version-management"></a>版本管理

當編譯附加至著色器的根簽章時，較新的 HLSL 編譯器會預設為編譯1.1 版的根簽章，而舊的 HLSL 編譯器只支援1.0。 請注意，1.1 根簽章將無法在不支援根簽章1.1 的作業系統上運作。

使用著色器編譯的根簽章版本，可以使用來強制執行特定版本 `/force_rootsig_ver <version>` 。 如果編譯器可以保留在強制版本中編譯之根簽章的行為，例如藉由將不支援的旗標放在僅供優化用途但不會影響行為的根簽章中，則強制執行版本將會成功。

比方說，應用程式可以在建立應用程式時將1.1 根簽章編譯為1.0 和1.1，視作業系統支援層級而定，在執行時間選取適當的版本。 但是，如果應用程式要個別編譯根簽章，這會是最有效率的空間 (特別是在需要多個版本時，請將其與著色器分開) 。 即使著色器最初不是以附加的根簽章進行編譯，也可以使用編譯器選項來保留編譯器驗證與著色器的根簽章相容性的優點 `/verifyrootsignature` 。 稍後在執行時間，您可以使用不具根簽章的著色器來建立 Pso，並傳遞所需的根簽章 (可能是作業系統所支援的適當版本) 作為個別參數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立根簽章](creating-a-root-signature.md)
</dt> <dt>

[根簽章](root-signatures.md)
</dt> <dt>

[在 HLSL 中指定根簽章](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 




