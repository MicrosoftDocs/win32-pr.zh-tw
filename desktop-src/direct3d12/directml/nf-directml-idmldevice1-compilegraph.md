---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: 將 DirectML 運算子的圖形編譯成可分派至 GPU 的物件。
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 8a9b4ce9bd8f8bd8b1d6f2a6bbd144009eb0d79d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417044"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a>IDMLDevice1：： CompileGraph 方法 (directml .h) 

將 DirectML 運算子的圖形編譯成可分派至 GPU 的物件。

已編譯的運算子代表適合在 GPU 上執行之運算子的有效率、內建形式。 已編譯的運算子會保存狀態 (例如著色器和其他物件) 執行所需。 由於編譯的運算子會執行 [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) 介面，因此您可以視需要從 GPU 記憶體中收回一個。 如需詳細資訊，請參閱 [IDMLDevice1：：收回](/windows/win32/api/directml/nf-directml-idmldevice-evict) 和 [IDMLDevice1：： MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) 。

在這個方法傳回之後，編譯的運算子不會使用或參考圖形描述內提供的 [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) 物件。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a>參數

`desc`

類型： **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***

要編譯之圖形的描述。 請參閱 [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)。

`flags`

類型： [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)

用來控制此運算子執行的任何旗標。

`riid`

類型： <b>REFIID</b>

全域唯一識別碼的參考， (您想要在 <i>ppv</i>中傳回之介面的 GUID) 。 這應該是 [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)的 GUID。

`ppv`

類型： <b>void * *</b>

記憶體區塊的指標，該區塊會接收已編譯之運算子的指標。 這是 [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)指標的位址，表示已建立的已編譯運算子。


## <a name="return-value"></a>傳回值

類型： [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

如果這個方法成功，它會傳回 **S_OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

DirectML 運算子圖形 API 提供了一種可在不同硬體上有效率地使用 DirectML 的抽象方法。 DirectML 會套用 tensor 層級的優化，例如根據所使用的介面卡，選擇最有效率的 tensor 版面配置。 它也會套用優化，例如移除聯結或分割運算子。

建議您在建立 DirectML 圖形之前套用高階優化。 例如，使用 BatchNorm、常數折迭和常見的子運算式刪除來融合加積運算子。 DirectML 圖優化器內的優化目的在於補充這類裝置獨立的優化，通常是由機器學習架構進行一般處理。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **目標平台** | Windows |
| **標頭** | directml。h |
| **程式庫** | DirectML .lib |
| **DLL** | DirectML.dll |

## <a name="see-also"></a>另請參閱

[IDMLDevice1](/windows/win32/api/directml/nn-directml-idmldevice)