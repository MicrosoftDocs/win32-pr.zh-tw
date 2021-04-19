---
description: 鎖定資源表示將 CPU 存取權授與儲存體。
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: " (Direct3D 9) 的鎖定資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d66a7a420a33cb908d0974f9d942597019aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973350"
---
# <a name="locking-resources-direct3d-9"></a> (Direct3D 9) 的鎖定資源

鎖定資源表示將 CPU 存取權授與儲存體。 下列為資源定義的鎖定選項：

-   D3DLOCK \_ 捨棄
-   D3DLOCK \_ READONLY
-   D3DLOCK \_ NOOVERWRITE
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ 沒有 \_ 中途 \_ 更新

如需鎖定旗標以及這些旗標如何與特定資源相關的詳細資訊，請參閱個別資源鎖定方法上的參考頁面。 應用程式開發人員應該要注意的是，D3DLOCK \_ 捨棄、D3DLOCK \_ READONLY 和 D3DLOCK \_ NOOVERWRITE 旗標只是提示。 執行時間不會檢查應用程式是否遵循這些旗標所指定的功能。 指定 D3DLOCK \_ READONLY 但接著寫入資源的應用程式應該會預期未定義的結果。 一般情況下，不保證會在較新版本中使用鎖定旗標（包括鎖定使用旗標），而且可能會產生顯著的效能影響。

鎖定作業接著是解除鎖定作業。 例如，在鎖定材質之後，應用程式會透過解除鎖定來會讓出直接存取鎖定的材質。 除了授與處理器存取權之外，任何其他牽涉到該資源的作業都會在鎖定期間進行序列化。 即使是針對非重迭的區域，也只允許資源的單一鎖定，而且在該介面上的鎖定作業未完成時，介面上沒有任何加速器作業可以進行。

每個資源介面都有方法可鎖定包含的緩衝區。 每個材質資源也可以鎖定該資源的子部分。 2D 資源 (表面) 允許鎖定子矩形，而磁片區資源允許鎖定子磁片區或方塊。 每個鎖定方法都會傳回一個結構，其中包含支援資源的儲存體指標，以及表示資料列或資料平面之間距離的值（視資源類型而定）。 如需詳細資訊，請參閱資源介面的方法清單。 傳回的指標一律指向鎖定子領域中的左上角位元組。

使用索引和頂點緩衝區時，您可以進行多次鎖定呼叫;不過，您必須確定鎖定呼叫的數目符合解除鎖定呼叫的數目。

DXTn 會將圖元儲存在編碼的4x4 區塊中，而且只能在4x4 界限上鎖定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 資源](direct3d-resources.md)
</dt> </dl>

 

 



