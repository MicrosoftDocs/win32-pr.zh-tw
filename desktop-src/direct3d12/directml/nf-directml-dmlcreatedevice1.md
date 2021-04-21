---
UID: NF:directml.DMLCreateDevice1
title: DMLCreateDevice1 函式
description: 為指定的 Direct3D 12 裝置建立 DirectML 裝置。
helpviewer_keywords:
- DMLCreateDevice1
- DMLCreateDevice1 function
- direct3d12.dmlcreatedevice1
- directml/DMLCreateDevice1
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
- DMLCreateDevice1
- directml/DMLCreateDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- DirectML.dll
api_name:
- DMLCreateDevice1
ms.openlocfilehash: f722b12208bd808f01e177feb907f94c33541496
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803768"
---
# <a name="dmlcreatedevice1-function-directmlh"></a>DMLCreateDevice1 函式 (directml) 

為指定的 Direct3D 12 裝置建立 DirectML 裝置。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a>參數

`d3d12Device`

類型： <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>*</b>

[ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device)的指標，代表要建立 DirectML 裝置的 Direct3D 12 裝置。 DirectML 支援任何 D3D 功能等級，以及在任何介面卡上建立的 Direct3D 12 裝置，包括變形。 不過，並非 DirectML 中的所有功能都可以根據 Direct3D 12 裝置的功能來使用。 如需詳細資訊，請參閱 [IDMLDevice：： CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) 。

如果 **DMLCreateDevice1** 的呼叫成功，則 DirectML 裝置會維護提供的 Direct3D 12 裝置的強式參考。

`flags`

類型： <b>DML_CREATE_DEVICE_FLAGS</b>

指定其他裝置建立選項的 [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) 值。

`minimumFeatureLevel`

類型： <b>DML_FEATURE_LEVEL</b>

[DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)值，指定所需的最小功能層級支援。

此參數對於需要特定 DirectML 版本的呼叫端很有用，但可能會發現本身呼叫舊版 DirectML 的人員。 例如，當使用者在舊版 Windows 10 上執行您的應用程式時，就會發生這種情況。

明確相依于特定功能等級所引進之功能的應用程式，可以將它指定為 *minimumFeatureLevel*。 這可保證 **DMLCreateDevice1** 將不會成功，除非基礎執行 *至少* 與這項要求的最小功能等級相同。

請注意，因為此參數指定 *最小* 的功能等級，所以基礎 DirectML 裝置實際上支援的功能層級高於所要求的最小值。 裝置建立成功之後，您就可以使用 [IDMLDevice：： CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport)來查詢此裝置支援的所有功能層級。

`riid`

類型： <b>REFIID</b>

您要在 <i>裝置</i>中傳回之介面 (GUID) 的全域唯一識別碼的參考。 這應該是 [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)的 GUID。

`ppv`

類型： \_ COM \_ Outptr \_ opt \_ <b>void * *</b>

記憶體區塊的指標，該區塊會接收裝置的指標。 這是 [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)指標的位址，代表所建立的 DirectML 裝置。


## <a name="return-value"></a>傳回值

類型： [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

如果函式成功，它會傳回 <b>S_OK</b>。 否則，它會傳回 [HRESULT](/windows/desktop/winprog/windows-data-types) 錯誤碼。

如果此版本的 DirectML 不支援所要求的 *minimumFeatureLevel* ，則此函式會傳回 **DXGI_ERROR_UNSUPPORTED**。

您必須安裝「圖形工具」隨選功能 (FOD) 才能使用 DirectML 的調試層。 如果在 *旗標* 中指定 [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags)旗標，且未安裝調試層，則 **DMLCreateDevice1** 會傳回 **DXGI_ERROR_SDK_COMPONENT_MISSING**。

## <a name="remarks"></a>備註

這個函式 [DMLCreateDevice1]()的較新版本是在 DirectML 版本1.1.0 中引進。 **DMLCreateDevice1** 相當於呼叫 **DMLCreateDevice1** 並提供 [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level)的 *minimumFeatureLevel* 。

## <a name="availability"></a>可用性

此 API 是在 DirectML 版本中引進 `1.1.0` 。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **目標平台** | Windows |
| **標頭** | directml。h |
| **程式庫** | DirectML .lib |
| **DLL** | DirectML.dll |

## <a name="see-also"></a>另請參閱

* [DML_FEATURE_LEVEL 列舉](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [DirectML 版本歷程記錄](../dml-version-history.md)
* [DirectML 功能等級歷程記錄](/windows/win32/direct3d12/dml-feature_level-history)    
* [使用 DirectML debug layer](../dml-debug-layer.md)