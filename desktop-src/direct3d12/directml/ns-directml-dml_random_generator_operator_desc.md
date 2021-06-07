---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: 以決定性產生的虛擬隨機、一致分散式位來填滿輸出 tensor。 這個運算子也可能會輸出已更新的內部產生器狀態，可在後續執行運算子期間使用。
helpviewer_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- DML_RANDOM_GENERATOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_OPERATOR_DESC, DML_RANDOM_GENERATOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.openlocfilehash: 6807c3a1ac91716739075f51196a75ae76ca479b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417051"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a>DML_RANDOM_GENERATOR_OPERATOR_DESC 結構 (directml .h) 

以決定性產生的虛擬隨機、一致分散式位來填滿輸出 tensor。 這個運算子也可能會輸出已更新的內部產生器狀態，可在後續執行運算子期間使用。

這個運算子具有決定性，而且行為就像是純虛擬函式，它的 &mdash; 執行不會產生副作用，也不會使用全域狀態。 這個運算子所產生的虛擬隨機輸出，只取決於 *InputStateTensor* 中提供的值。

這個運算子所執行的產生器不會以密碼編譯方式安全;因此，此操作員不應用於加密、金鑰產生，或需要以密碼編譯安全亂數產生的其他應用程式。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a>成員

`InputStateTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含內部產生器狀態的輸入 tensor。 此輸入 tensor 的大小和格式取決於 [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)。

針對 **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**，此 tensor 必須屬於 **UINT32** 類型，而且具有大小 `{1,1,1,6}` 。 第一個 4 32 位值包含單純增加的128位計數器。 最後一個 2 32 位值包含產生器的64位索引鍵值。

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

第一次初始化產生器的輸入狀態時，通常是128位計數器 (第一個 4 32 位 UINT32 值) 應該初始化為0。 您可以任意選擇此金鑰;不同的索引鍵值會產生不同的數位序列。 通常會使用使用者提供的 *種子* 來產生金鑰的值。

`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含所產生之虛擬隨機值的輸出 tensor。 此 tensor 可以是任何大小。

`OutputStateTensor`

類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

選用的輸出 tensor，其中保留已更新的內部產生器狀態。 如果有提供，這個運算子會使用 *InputStateTensor* 來計算適當的已更新產生器狀態，並將結果寫入 *OutputStateTensor*。 一般而言，呼叫端會儲存此結果，並在後續執行此運算子時，提供它做為輸入狀態。

`Type`

類型： **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**

[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)列舉中的其中一個值，表示要使用之產生器的類型。 目前唯一有效的值是 **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**，這會根據 [PHILOX 4X32-10 演算法](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf)產生虛擬亂數。

## <a name="remarks"></a>備註
在每次執行此運算子時，128位計數器應遞增。 如果提供了 *OutputStateTensor* ，則這個運算子會代表您以正確的值遞增計數器，並將結果寫入 *OutputStateTensor*。 應該遞增的數量取決於所產生的32位輸出元素數目，以及產生器的類型。

針對 **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**，128位計數器應該 `ceil(outputSize / 4)` 在每次執行時遞增，其中 `outputSize` 是 *OutputTensor* 中的元素數目。

假設有一個範例，其中128位計數器的值目前為 `0x48656c6c'6f46726f'6d536561'74746c65` ，而 OutputTensor 的大小為 `{3,3,20,7219}` 。 執行這個運算子一次之後，計數器應遞增 324855 (所產生的輸出元素數目除以4，進位) 產生的計數器值 `0x48656c6c'6f46726f'6d536561'746f776e` 。 接著，您應該將這個更新的值做為輸入，提供給這個運算子的下一次執行。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
`InputStateTensor` 和 `OutputStateTensor` 必須有相同的 *大小*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 種類 | 維度 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputStateTensor | 輸入 | {1，1，1，6} | 4 | UINT32 |
| OutputTensor | 輸出 | {D0，D1，D2，D3} | 4 | UINT32 |
| OutputStateTensor | 選用輸出 | {1，1，1，6} | 4 | UINT32 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |