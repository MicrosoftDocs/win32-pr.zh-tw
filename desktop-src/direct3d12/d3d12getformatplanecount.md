---
title: 'D3D12GetFormatPlaneCount 函式 (D3dx12) '
description: 針對指定的虛擬配接器 (ID3D12Device) ，取得指定之 DXGI 格式的平面數目。
ms.assetid: CD21F6F9-A9AA-4CE8-A430-57C70326CB4B
keywords:
- D3D12GetFormatPlaneCount 函式
topic_type:
- apiref
api_name:
- D3D12GetFormatPlaneCount
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0791a3326286d6a6e784bc179890258fd7bf320511b37564f538b2d040ed10f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098263"
---
# <a name="d3d12getformatplanecount-function"></a>D3D12GetFormatPlaneCount 函式

針對指定的虛擬配接器 (**ID3D12Device**) ，取得指定之 DXGI 格式的平面數目。

## <a name="syntax"></a>語法


```C++
UINT8 inline D3D12GetFormatPlaneCount(
  _In_ ID3D12Device *pDevice,
       DXGI_FORMAT  Format
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***

虛擬配接器 (用來取得平面計數的 [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) 。

</dd> <dt>

*格式* 
</dt> <dd>

類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

要取得平面計數的 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **UINT8**

指定之虛擬配接器上指定格式的平面計數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx12。h</dt> </dl>  |
| 程式庫<br/> | <dl> <dt>D3D12 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 功能 \_ 資料 \_ 格式 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)
</dt> <dt>

[**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
</dt> <dt>

[D3D12 的 Helper 函式](helper-functions-for-d3d12.md)
</dt> </dl>

 

