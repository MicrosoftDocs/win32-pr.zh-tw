---
description: 從 Direct3D 10.0 介面指標取得 Direct3D 10.1 裝置介面指標。
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: 'D3DX10GetFeatureLevel1 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: c6511e0d3963e21f8950529b32cf8c3b414cc00b0625b97b2a9d569d1523c326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753168"
---
# <a name="d3dx10getfeaturelevel1-function"></a>D3DX10GetFeatureLevel1 函式

從 Direct3D 10.0 介面指標取得 Direct3D 10.1 裝置介面指標。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Direct3D 10.0 裝置的指標 (查看 [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) 介面) 。

</dd> <dt>

*ppDevice* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***

Direct3D 10.1 裝置的指標 (查看 [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) 介面) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

此函數會傳回下列其中一個 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)。 如果可以取得 Direct3D 10.1 裝置介面，此函式會成功，並使用 *ppDevice* 參數將指標傳遞至10.1 介面。 如果無法取得 Direct3D 10.1 裝置介面，此函式會傳回 E \_ 失敗，而且不會傳回任何 *ppDevice* 參數的任何參數。

## <a name="remarks"></a>備註

若要讓此函式成功，您必須使用 [**D3DX10CreateDevice**](d3dx10createdevice.md)函數、 [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md)函式、 [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1)函數或 [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)函數的呼叫來取得提供的 [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)指標。

您只能在執行 Windows Vista Service Pack 1 或更新版本的電腦上，以及安裝 direct3d 10.1 相容硬體的電腦上建立 Direct3D 10.1 裝置。 此函式會 \_ 在任何電腦上傳回 E 失敗，而不符合這些需求。 不過，您可以在已安裝 D3DX10 DLL 的任何 Windows 版本上呼叫此函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Core。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




