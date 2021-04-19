---
title: 'D3DX12SerializeVersionedRootSignature 函式 (D3dx12) '
description: 有助於啟用根簽章1.1 功能（如果有的話），而且不需要維護兩個程式碼路徑來建立根簽章。 此 helper 方法會在版本1.1 不受支援時，重建版本1.0 的根簽章。
ms.assetid: 0F6BA6C1-9A33-4E99-BF34-4A0358E7427D
keywords:
- D3DX12SerializeVersionedRootSignature 函式
topic_type:
- apiref
api_name:
- D3DX12SerializeVersionedRootSignature
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70a9d0424f7f7a7f89edde18273c5d1fa22fae28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992699"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a>D3DX12SerializeVersionedRootSignature 函式

有助於啟用根簽章1.1 功能（如果有的話），而且不需要維護兩個程式碼路徑來建立根簽章。 此 helper 方法會在版本1.1 不受支援時，重建版本1.0 的根簽章。

## <a name="syntax"></a>語法


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pRootSignatureDesc* \[在\]
</dt> <dd>

類型： **CONST D3D12 已建立版本的根簽章 \_ \_ \_ \_ DESC \***

指定 [**D3D12 \_ 版本的 \_ 根 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) 簽章 DESC，其中包含任何版本之根簽章的描述。

</dd> <dt>

*Odata-maxversion* 
</dt> <dd>

類型： **D3D \_ 根 \_ \_** 簽章版本

指定支援的 [**D3D 根簽章 \_ \_ \_ 版本**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)上限。

</dd> <dt>

*ppBlob* \[擴展\]
</dt> <dd>

類型： **ID3DBlob \* \***

記憶體區塊的指標，該區塊會接收指向 [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) 介面的指標，您可以用來存取序列化的根簽章。

</dd> <dt>

*ppErrorBlob* \[out、optional\]
</dt> <dd>

類型： **ID3DBlob \* \***

記憶體區塊的指標，該區塊會接收您可以用來存取序列化程式錯誤訊息的 [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) 介面指標，如果沒有任何錯誤，則為 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果成功，則傳回 **\_ [確定]** ，否則會傳回其中一個 [Direct3D 12 傳回碼](d3d12-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

這個函式的發行與 Windows 10 年度更新版 (14393) 一致。 若要支援此之前的 Windows 10 版本，請使用此函式需要設定 d3d12 以進行 *延遲載入*。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx12。h</dt> </dl>  |
| 程式庫<br/> | <dl> <dt>D3D12 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[D3D12 的 Helper 函式](helper-functions-for-d3d12.md)
</dt> </dl>

 

