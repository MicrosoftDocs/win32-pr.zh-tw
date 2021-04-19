---
title: ID3D12Resource GetDesc 方法
description: 取得資源描述。
ms.assetid: B8D84D69-6B13-4E86-8EF6-A841354B1E5C
keywords:
- GetDesc 方法
- GetDesc 方法，ID3D12Resource 介面
- ID3D12Resource 介面，GetDesc 方法
topic_type:
- apiref
api_name:
- ID3D12Resource.GetDesc
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
api_location:
- d3d12.h
ms.openlocfilehash: 5be3f6f825370c467388805c84096240441d09a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106966428"
---
# <a name="id3d12resourcegetdesc-method"></a>ID3D12Resource：： GetDesc 方法

取得資源描述。

## <a name="syntax"></a>語法


```C++
D3D12_RESOURCE_DESC GetDesc();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **D3D12 \_ 資源 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)**

Direct3D 12 資源描述結構。

## <a name="examples"></a>範例

傳回所需的緩衝區大小，以用於資料上傳。


```C++
// Returns required size of a buffer to be used for data upload
inline UINT64 GetRequiredIntermediateSize(
    _In_ ID3D12Resource* pDestinationResource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES) UINT FirstSubresource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES-FirstSubresource) UINT NumSubresources)
{
    D3D12_RESOURCE_DESC Desc = pDestinationResource->GetDesc();
    UINT64 RequiredSize = 0;
    
    ID3D12Device* pDevice;
    pDestinationResource->GetDevice(__uuidof(*pDevice), reinterpret_cast<void**>(&pDevice));
    pDevice->GetCopyableFootprints(&Desc, FirstSubresource, NumSubresources, 0, nullptr, nullptr, nullptr, &RequiredSize);
    pDevice->Release();
    
    return RequiredSize;
}
```



請參閱 [D3D12 參考中的範例程式碼](notes-on-example-code.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)
</dt> </dl>

 

 




