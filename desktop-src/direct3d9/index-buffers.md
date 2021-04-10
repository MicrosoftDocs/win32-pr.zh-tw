---
description: IDirect3DIndexBuffer9 介面所代表的索引緩衝區是包含索引資料的記憶體緩衝區。
ms.assetid: baa60cd1-a1f0-4dbe-b934-aeb1a5c6b784
title: " (Direct3D 9) 的索引緩衝區"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7151fae6deb72a0c569d269c80e5b13bf946f9d0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845964"
---
# <a name="index-buffers-direct3d-9"></a> (Direct3D 9) 的索引緩衝區

[**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)介面所代表的索引緩衝區是包含索引資料的記憶體緩衝區。 索引資料（或索引）是頂點緩衝區的整數位移，可用來使用 [**IDirect3DDevice9：:D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 方法來呈現基本資料。

頂點緩衝包含頂點，因此，您可以使用或不使用索引的基本類型來繪製頂點緩衝。 不過，因為索引緩衝包含索引，您無法使用無對應頂點緩衝的索引緩衝。  (為 [**IDirect3DDevice9：:D rawindexedprimitiveup**](/windows/desktop/api) 和 [**IDirect3DDevice9：:D rawprimitiveup**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup) 是唯一繪製沒有索引或頂點緩衝區的繪圖方法。 ) 

## <a name="index-buffer-description"></a>索引緩衝描述

索引緩衝是依照其能力來描述，例如存在於記憶體中的哪裡、是否支援讀取和寫入，以及可包含的索引類型以數目。 這些特性會保留在 [**D3DINDEXBUFFER \_ DESC**](d3dindexbuffer-desc.md) 結構中。

索引緩衝描述會告訴您的應用程式現有緩衝區是如何建立的。 您為系統提供空描述結構，以填入先前建立的索引緩衝功能。

-   格式成員描述索引緩衝區資料的介面格式。
-   此類型會識別索引緩衝區的資源類型。
-   使用結構成員包含一般功能旗標。 D3DUSAGE \_ SOFTWAREPROCESSING 旗標表示索引緩衝區要與軟體頂點處理搭配使用。 使用中的 D3DUSAGE WRITEONLY 旗標是否存在， \_ 表示索引緩衝區記憶體只用于寫入作業。 這樣就可以釋出驅動程式，將索引資料放在最佳的記憶體位置，以啟用快速處理和轉譯。 如果 \_ 未使用 D3DUSAGE WRITEONLY 旗標，驅動程式較不可能將資料放在讀取作業效率不佳的位置。 這犧牲了一些處理和轉譯速度。 如果未指定此旗標，則會假設應用程式會對索引緩衝區中的資料執行讀取和寫入作業。
-   集區會指定配置給索引緩衝區的記憶體類別。 D3DPOOL \_ SYSTEMMEM 旗標表示系統已在系統記憶體中建立索引緩衝區。
-   大小成員會儲存頂點緩衝區資料的大小（以位元組為單位）。
-   未使用最後一個參數 pSharedHandle。 將它設定為 **Null**。

## <a name="index-processing-requirements"></a>索引處理需求

索引處理作業指數的效能，大幅仰賴索引緩衝存在於記憶體中的位置，以及正在使用何種轉譯裝置。 應用程式控制索引緩衝在建立時的記憶體配置。 \_設定 D3DPOOL SYSTEMMEM memory 旗標時，會在系統記憶體中建立索引緩衝區。 \_使用 D3DPOOL 預設記憶體旗標時，設備磁碟機會判斷索引緩衝區的記憶體最適合配置的位置，通常稱為驅動程式優化的記憶體。 驅動程式-最佳的記憶體可以是本機視訊記憶體、非本機視訊記憶體或系統記憶體。

\_在呼叫 [**IDirect3DDevice9：： CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)方法時設定 D3DUSAGE SOFTWAREPROCESSING 行為旗標，指定要搭配軟體頂點處理使用的索引緩衝區。 \_使用軟體頂點處理時，在混合模式頂點處理 (D3DCREATE 混合 VERTEXPROCESSING) 需要此旗標 \_ 。

應用程式可以直接將索引寫入驅動程式最佳化記憶體中配置的索引緩衝。 這項技術會防止稍後的冗餘複製作業。 如果您的應用程式從索引緩衝讀回資料，這項技術無法正常運作，因為主機從驅動程式最佳化記憶體完成讀取作業的速度非常緩慢。 因此，如果應用程式在不規律地處理或將資料寫入緩衝區期間需要讀取，系統記憶體索引緩衝則是較理想的選擇。

> [!Note]  
> \_除非您不想要在驅動程式將頂點或索引緩衝區放置於 AGP 記憶體時使用影片記憶體或使用大量頁面鎖定 RAM，否則請一律使用 D3DPOOL 預設值。

 

## <a name="create-an-index-buffer"></a>建立索引緩衝區

藉由呼叫 [**IDirect3DDevice9：： CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) 方法（可接受六個參數）來建立索引緩衝區物件。

-   第一個參數會指定索引緩衝區長度（以位元組為單位）。
-   第二個參數是一組使用方式控制項。 此外，它的值會決定索引所參考的頂點是否能夠包含剪切資訊。 若要改善效能，請 \_ 在不需要剪切時指定 D3DUSAGE DONOTCLIP。

    當您 \_ 針對該裝置啟用混合模式或軟體頂點處理 (D3DCREATE \_ mixed \_ VERTEXPROCESSING/D3DCREATE \_ software \_ VERTEXPROCESSING) 時，可以設定 D3DUSAGE SOFTWAREPROCESSING 旗標。 您 \_ 必須針對要在混合模式中使用軟體頂點處理的緩衝區設定 D3DUSAGE SOFTWAREPROCESSING，但不應針對在混合模式中使用硬體索引處理的最佳效能設定 (D3DCREATE \_ 硬體 \_ VERTEXPROCESSING) 。 不過， \_ 當單一緩衝區同時搭配硬體和軟體頂點處理使用時，設定 D3DUSAGE SOFTWAREPROCESSING 是唯一的選項。 \_混合和軟體裝置允許 D3DUSAGE SOFTWAREPROCESSING。

    您可以指定 D3DPOOL SYSTEMMEM，將頂點和索引緩衝區強制到系統記憶體中 \_ ，即使是在硬體中完成索引處理也是一樣。 這是一種方法，可在驅動程式將這些緩衝區放入 AGP 記憶體時避免過度大量的頁面鎖定記憶體。

-   第三個參數是 \_ \_ [D3DFORMAT](d3dformat.md) 列舉型別的 D3DFMT INDEX16 或 D3DFMT INDEX32 成員，它會指定每個索引的大小。

-   第四個參數是 [**D3DPOOL**](./d3dpool.md) 列舉型別的成員，它會告訴系統要將新的索引緩衝區放在記憶體中的哪個位置。

-   [**IDirect3DDevice9：： CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)所接受的最後一個參數是變數的位址，這個變數會填入頂點緩衝區物件的新 [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)介面指標（如果呼叫成功）。

下列 c + + 程式碼範例會示範如何在程式碼中建立索引緩衝區。


```
/*
 * For the purposes of this example, the d3dDevice variable is the 
 * address of an IDirect3DDevice9 interface exposed by a 
 * Direct3DDevice object, g_IB is a variable of type 
 * LPDIRECT3DINDEXBUFFER9.
 */

if( FAILED( d3dDevice->CreateIndexBuffer( 16384 *sizeof(WORD),
           D3DUSAGE_WRITEONLY, D3DFMT_INDEX16, D3DPOOL_DEFAULT, 
           &g_IB, NULL ) ) )
    return E_FAIL;
```



## <a name="access-an-index-buffer"></a>存取索引緩衝區

索引緩衝區物件可讓應用程式直接存取配置給索引資料的記憶體。 您可以藉由呼叫 [**IDirect3DIndexBuffer9：： Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) 方法來取得索引緩衝區記憶體的指標，然後視需要存取記憶體，以使用新的索引資料來填滿緩衝區或讀取其包含的任何資料。 鎖定方法接受四個參數。 第一個 *OffsetToLock* 是索引資料中的位移。 第二個參數是索引資料的大小（以位元組為單位）。 **IDirect3DIndexBuffer9：： Lock** 方法（ *ppbData*）接受的第三個參數是在呼叫成功時，以索引資料指標填滿的位元組指標位址。

最後一個參數 *旗標* 會告知系統應該如何鎖定記憶體。 您可以使用它來表示應用程式如何存取緩衝區中的資料。 根據您的應用程式存取索引資料的方式，指定 *旗標* 參數的常數。 這可讓驅動程式鎖定記憶體，並提供所要求之存取類型的最佳效能。 \_如果您的應用程式只會從索引緩衝區記憶體讀取，請使用 D3DLOCK READONLY 旗標。 包含這個旗標可讓 Direct3D 將其內部程式優化，以改善效率（假設存取記憶體將會是唯讀的）。

填滿或讀取索引資料之後，請呼叫 [**IDirect3DIndexBuffer9：： Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-unlock) 方法，如下列程式碼範例所示。


```
// This code example assumes the m_pIndexBuffer is a variable of type 
// LPDIRECT3DINDEXBUFFER9 and that g_Indices has been properly 
// initialized with indices.

// To fill the index buffer, you must lock the buffer to gain 
// access to the indices. This mechanism is required because index
// buffers may be in device memory.

VOID* pIndices;

if( FAILED( m_pIndexBuffer->Lock( 
      0,                 // Fill from start of the buffer
      sizeof(g_Indices), // Size of the data to load
      BYTE**)&pIndices,  // Returned index data
      0 ) ) )            // Send default flags to the lock
{
    SAFE_RELEASE(m_pIndexBuffer);
    return E_FAIL;
}

memcpy( pIndices, g_Indices, sizeof(g_Indices) );
m_pIndexBuffer->Unlock();
```



> [!Note]
>
> 如果您使用 D3DUSAGE WRITEONLY 旗標建立索引緩衝區 \_ ，請勿使用 D3DLOCK \_ READONLY 鎖定旗標。 \_如果您的應用程式只會從索引緩衝區記憶體讀取，請使用 D3DLOCK READONLY 旗標。 包含這個旗標可讓 Direct3D 將其內部程式優化，以改善效率（假設存取記憶體將會是唯讀的）。
>
> 如需針對 \_ \_ [**IDirect3DIndexBuffer9：： Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)方法的 *Flags* 參數使用 D3DLOCK 捨棄或 D3DLOCK NOOVERWRITE 的詳細資訊，請參閱 [ (Direct3D 9) 的效能優化](performance-optimizations.md)。

 

在 c + + 中，因為您直接存取為索引緩衝區配置的記憶體，請確定您的應用程式能夠正確地存取配置的記憶體。 否則，您會面臨轉譯記憶體不正確風險。 使用您的應用程式用來從配置緩衝區中的一個索引移至另一個索引的索引格式的 stride。

藉由呼叫 [**IDirect3DIndexBuffer9：： GetDesc**](/windows/desktop/api) 方法，取得索引緩衝區的相關資訊。 這個方法會使用索引緩衝區的相關資訊，填滿 [**D3DINDEXBUFFER \_ DESC**](d3dindexbuffer-desc.md) 結構的成員。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 資源](direct3d-resources.md)
</dt> <dt>

[從頂點和索引緩衝區轉譯 (Direct3D 9) ](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[ (Direct3D 9) 的頂點緩衝區 ](vertex-buffers.md)
</dt> </dl>

 

 
