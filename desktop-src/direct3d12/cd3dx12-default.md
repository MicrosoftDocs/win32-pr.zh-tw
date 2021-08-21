---
title: 'CD3DX12_DEFAULT 結構 (D3dx12 .h) '
description: 將 D3D12 \_ 預設值傳遞至每個 helper 結構的函式。 此結構只是用來做為在其他 helper 結構上設定預設參數的機制。
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- CD3DX12_DEFAULT 結構
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 876fbb5e666680e85854196fb9136bfd4d765d6eecf8f16bf6101bb321a7039a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531285"
---
# <a name="cd3dx12_default-structure"></a>CD3DX12 \_ 預設結構

將 D3D12 \_ 預設值傳遞至每個 helper 結構的函式。 此結構只是用來做為在其他 helper 結構上設定預設參數的機制。

## <a name="remarks"></a>備註

此結構的宣告方式如下：

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

將 D3D12 \_ 預設值傳遞至每個 helper 結構的函式。 例如，下列的函式會在 d3dx12 中宣告：

CD3DX12 \_ CPU \_ 描述項 \_ 控制碼 (CD3DX12 \_ 預設) {ptr = 0;}

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





