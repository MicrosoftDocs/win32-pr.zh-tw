---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: 代表用來建立運算子、系結資料表、命令記錄器和其他物件的 DirectML 裝置。
helpviewer_keywords:
- IDMLDevice1
- IDMLDevice1 interface
- IDMLDevice1 interface
- described
- direct3d12.idmldevice1
- directml/IDMLDevice1
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1
- directml/IDMLDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.h
api_name:
- IDMLDevice1
ms.openlocfilehash: 7a10cf2c9fe683775d163c7b5cb0e30fe07de08f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417045"
---
# <a name="idmldevice1-interface-directmlh"></a>IDMLDevice1 介面 (directml .h) 

代表用來建立運算子、系結資料表、命令記錄器和其他物件的 DirectML 裝置。 **IDMLDevice1** 介面繼承自 [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)。

DirectML 裝置一律會與一個基礎 Direct3D 12 裝置相關聯。 DirectML 裝置所建立的所有物件都會維持其父裝置的強式參考。 不同于 Direct3D 12 裝置，DML 裝置不是 singleton。 因此，您可以透過相同的 Direct3D 12 裝置建立多個 DirectML 裝置。 不過，這不是建議的作法，因為 DirectML 裝置沒有可變動的狀態，因此在相同的 Direct3D 12 裝置上建立多個 DML 裝置並沒有什麼好處。

此物件是安全線程。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="availability"></a>可用性
此 API 是在 DirectML 版本中引進 `1.1.0` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
**目標平臺**： Windows


## <a name="inheritance"></a>繼承


IDMLDevice1 介面繼承自 IDMLDevice 介面。



## <a name="methods"></a>方法

<p><b>IDMLDevice1</b>介面具有這些方法。</p>

| 方法 | 描述 |
| ---- |:---- |
| [IDMLDevice1::CompileGraph](../directml/nf-directml-idmldevice1-compilegraph.md) | 將 DirectML 運算子的圖形編譯成可分派至 GPU 的物件。 |


## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **目標平台** | Windows |
| **標頭** | directml。h |

## <a name="see-also"></a>另請參閱

[IDMLDevice 介面](/windows/win32/api/directml/nn-directml-idmldevice)