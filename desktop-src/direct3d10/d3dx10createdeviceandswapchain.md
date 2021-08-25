---
description: 建立最佳的 Direct3D 裝置和交換鏈。
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: 'D3DX10CreateDeviceAndSwapChain 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: aa92b0fd7efb9c6f457fd035fad28992d965a4cf2f6fdad39936292f7a70a996
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852368"
---
# <a name="d3dx10createdeviceandswapchain-function"></a>D3DX10CreateDeviceAndSwapChain 函式

建立最佳的 Direct3D 裝置和交換鏈。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAdapter* \[在\]
</dt> <dd>

類型： **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)的指標。

</dd> <dt>

*DriverType* \[在\]
</dt> <dd>

類型： **[ **D3D10 \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

裝置的驅動程式類型。 請參閱 [**D3D10 \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)。

</dd> <dt>

*軟體* \[在\]
</dt> <dd>

類型： **[ **HMODULE**](../winprog/windows-data-types.md)**

執行軟體轉譯器之 DLL 的控制碼。 如果 DriverType 為非軟體，則必須是 **Null** 。 您可以使用 [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)、 [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)或 [GETMODULEHANDLE](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)來取得 DLL 的 HMODULE。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

選擇性。 裝置建立旗標 (查看啟用 [API 層](d3d10-graphics-programming-guide-api-features-layers.md)的 [**D3D10 \_ 建立 \_ 裝置 \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)標) 。 這些旗標可以是位 OR。

</dd> <dt>

*pSwapChainDesc* \[在\]
</dt> <dd>

類型： **[ **DXGI \_ 交換 \_ 鏈 \_ DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***

交換鏈的描述。 請參閱 [**DXGI \_ 交換 \_ 鏈 \_ DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)。

</dd> <dt>

*ppSwapChain* \[擴展\]
</dt> <dd>

類型： **[ **IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***

[**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)指標的位址。

</dd> <dt>

*ppDevice* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

[**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)的指標位址，此介面會接收新建立的裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

這個方法會傳回下列其中一個 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

若要建立最佳裝置，這個方法會執行一個以上的裝置建立選項。 首先，此方法會嘗試建立10.1 裝置 (和交換鏈) 。 如果失敗，方法會嘗試建立10.0 裝置。 如果失敗，方法將會失敗。 如果您的應用程式只需要建立10.1 裝置或僅限10.0 裝置，請改用這些 Api：

-   使用 [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) 建立僅) 裝置和交換鏈的 Direct3D 10.0 (。
-   使用 [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) 建立僅) 裝置和交換鏈的 Direct3D 10.1 (。

此方法需要 Windows Vista Service Pack 1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Core。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
