---
description: 許多應用程式都需要使用不失真的資料壓縮和解壓縮。 壓縮 api 會透過公用 API 公開 Windows 壓縮演算法來簡化此工作。
ms.assetid: D603A7DE-D4A1-4515-9702-B03C81504661
title: 使用壓縮 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fedc1d57ad48196290500383686b35f557c87c34099aad842b1e8ff18f00d318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551382"
---
# <a name="using-the-compression-api"></a>使用壓縮 API

許多應用程式都需要使用不失真的資料壓縮和解壓縮。 壓縮 api 會透過公用 API 公開 Windows 壓縮演算法來簡化此工作。 每個壓縮演算法都有一組屬性，可控制其行為。 壓縮 API 會公開介面，讓開發人員可以設定或查詢這些屬性的值。 支援的壓縮演算法的所有屬性都有預設值，代表這些屬性常用的值。 如果壓縮和解壓縮都需要屬性，則預設值將會相同，以確保使用相同的值進行壓縮和解壓縮。

## <a name="selecting-the-compression-algorithm"></a>選取壓縮演算法

在開發人員決定應用程式需要壓縮或解壓縮資料之後，下一步就是選擇壓縮演算法。 這可能取決於測試，以找出最佳的速度、壓縮率和特定應用程式的記憶體需求組合。 下列清單提供壓縮 API 目前支援的壓縮演算法的相對比較。 並非每個壓縮演算法都可以使用每個選項，而且比較是近似的，因為效能可能取決於輸入資料。

XPRESS (**壓縮 \_ 演算法 \_ XPRESS**) 

-   使用低資源需求非常快速
-   中壓縮比例
-   高壓縮和解壓縮速度
-   記憶體不足需求
-   支援 [**壓縮 \_ 資訊 \_ 類別**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class)列舉中提供的 [**壓縮 \_ 資訊 \_ 類別] \_ 層級** 選項。 預設值為 **(DWORD) 0**。 對於某些資料而言， **(DWORD) 1** 的值可以改善壓縮率，速度會稍微慢一點。

使用 Huffman 編碼的 XPRESS (**壓縮 \_ 演算法 \_ XPRESS \_ HUFF**) 

-   壓縮比例高於 **壓縮 \_ 演算法 \_ XPRESS**
-   中壓縮比例
-   中高壓縮和解壓縮速度
-   記憶體不足需求
-   支援 [**壓縮 \_ 資訊 \_ 類別**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class)列舉中的 **壓縮 \_ 資訊 \_ 類別 \_ 層級** 選項。 預設值為 **(DWORD) 0**。 對於某些資料而言， **(DWORD) 1** 的值可以改善壓縮率，速度會稍微慢一點。

MSZIP (**壓縮 \_ 演算法 \_ MSZIP**) 

-   使用的資源比 **壓縮 \_ 演算法 \_ XPRESS \_** 更多 HUFF
-   產生類似于 RFC 1951 的壓縮區塊。
-   中到高壓縮比例
-   中壓縮速度和高解壓縮速度
-   中記憶體需求

LZMS (**壓縮 \_ 演算法 \_ LZMS**) 

-   如果要壓縮的資料大小超過2MB，則為良好的演算法。
-   高壓縮比例
-   低壓縮速度和高解壓縮速度
-   中型至高記憶體需求
-   支援 [**壓縮 \_ 資訊 \_ 類別**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class)列舉中的 **壓縮 \_ 資訊 \_ 類別 \_ 區塊 \_ 大小** 選項。 建議的大小下限為 1 MB，以取得較佳的壓縮比率。

## <a name="deciding-which-compression-api-mode-to-use"></a>決定要使用的壓縮 API 模式

在開發人員選取壓縮演算法之後，下一次決定要使用的壓縮 API 模式有兩種：緩衝區模式或封鎖模式。 緩衝區模式是為了方便使用而開發，建議用於大部分的情況。

緩衝區模式會自動將輸入緩衝區分割成適用于所選壓縮演算法的大社區塊。 緩衝區模式會自動格式化，並將未壓縮的緩衝區大小儲存在壓縮的緩衝區中。 壓縮緩衝區的大小不會自動儲存，而且應用程式需要儲存此值以進行解壓縮。 當您呼叫 [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor)和 [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor)來使用緩衝區模式時，請勿在 *演算法* 參數中包含 **壓縮 \_ 原始** 旗標。 如需緩衝區模式應用程式的程式碼範例，請參閱在 [緩衝區模式中使用壓縮 API](using-the-compression-api-in-buffer-mode.md) 一節。

[封鎖] 模式可讓開發人員控制區塊大小，但應用程式需要更多工作。 使用區塊模式時，應用程式必須在壓縮時將輸入資料分解成適當大小的部分，然後在解壓縮時將這些部分放在一起。 如果輸入緩衝區的大小大於壓縮演算法的內部區塊大小，區塊模式將會失敗。 內部區塊大小為 MSZIP 的32KB 和 1 GB，適用于 XPRESS 壓縮演算法。 LZMS 的內部區塊大小可設定為64GB，而且記憶體使用量相對增加。 壓縮緩衝區的大小不會自動儲存，而且應用程式也需要儲存此值以供解壓縮。 [**解壓縮**](/windows/desktop/api/compressapi/nf-compressapi-decompress)的 *UncompressedBufferSize* 參數值必須完全等於未壓縮資料的原始大小，而不只是輸出緩衝區的大小。 這表示您的應用程式應該在使用區塊模式時，儲存未壓縮資料的確切原始大小，以及壓縮的資料和壓縮的大小。 當您同時呼叫 [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor)和 [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor)來使用區塊模式時，請在 *演算法* 參數中包含 **壓縮 \_ 原始** 旗標。 如需區塊模式應用程式的程式碼範例，請參閱在 [區塊模式中使用壓縮 API](using-the-compression-api-in-block-mode.md) 一節。

## <a name="custom-memory-allocation"></a>自訂記憶體配置

當緩衝區和區塊模式應用程式呼叫 [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) 和 [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor)時，可以選擇指定自訂記憶體配置常式。 *AllocationRoutines* 參數會指定包含記憶體配置常式的 [**壓縮 \_ 配置 \_ 常式**](/windows/desktop/api/compressapi/ns-compressapi-compress_allocation_routines)結構。 然後，應用程式可以使用 [**SetCompressorInformation**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation)設定壓縮程式的區塊大小。 如需簡單自訂配置常式的範例，請參閱在 [區塊模式中使用壓縮 API](using-the-compression-api-in-block-mode.md) 一節。

 

 



