---
description: 取得建立 Microsoft DirectX Graphic Infrastructure (DXGI) 物件時所使用的旗標。
ms.assetid: 1B4A5DC9-6853-4047-B64D-BD251352AC89
title: IDXGIFactory3：： GetCreationFlags 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDXGIFactory3.GetCreationFlags
api_type:
- COM
api_location:
- dxgi1_3.h
ms.openlocfilehash: 56d1f35ea5a4ce26a0d9ccb5ee0d79035f74a0ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108384"
---
# <a name="idxgifactory3getcreationflags-method"></a>IDXGIFactory3：： GetCreationFlags 方法

取得建立 Microsoft DirectX Graphic Infrastructure (DXGI) 物件時所使用的旗標。

## <a name="syntax"></a>語法


```C++
UINT GetCreationFlags();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

建立旗標。

## <a name="remarks"></a>備註

**GetCreationFlags** 方法會傳回傳遞給 [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)函式的旗標，或是由 [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)、 [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)、 [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice)或 [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain)隱含地所建立的旗標。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDXGIFactory3**](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgifactory3)
</dt> </dl>

 

 
