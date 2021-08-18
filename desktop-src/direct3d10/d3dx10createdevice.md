---
description: 建立最佳的 Direct3D 10 裝置，以代表顯示配接器。 如果可以建立 Direct3D 10.1 相容裝置，就可以從傳回的裝置介面指標取得 ID3D10Device1 介面指標。
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: 'D3DX10CreateDevice 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 9300eb74027d25562dabb9a596face10105110d1750b359bcaae9ab6b2b83084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634698"
---
# <a name="d3dx10createdevice-function"></a>D3DX10CreateDevice 函式

建立最佳的 Direct3D 10 裝置，以代表顯示配接器。 如果可以建立 Direct3D 10.1 相容裝置，就可以從傳回的裝置介面指標取得 [**ID3D10Device1 介面**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) 指標。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAdapter* \[在\]
</dt> <dd>

類型： **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

顯示配接器的指標 (在建立硬體裝置時看到 [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) 介面) ;否則，請將此參數設定為 **Null**。 如果在建立硬體裝置時指定了 **Null** ，Direct3D 將會使用 [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) 介面所列舉的第一個介面卡。

</dd> <dt>

*DriverType* \[在\]
</dt> <dd>

類型： **[ **D3D10 \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

裝置驅動程式類型 (查看 [**D3D10 \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) 列舉) 。 驅動程式類型可決定您將建立的裝置類型。

</dd> <dt>

*軟體* \[在\]
</dt> <dd>

類型： **[ **HMODULE**](../winprog/windows-data-types.md)**

已載入模組的控制碼，可執行軟體驅動程式 (例如 D3D10Ref.dll) 。 若要取得控制碼，請呼叫 [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 函數。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

裝置建立旗標 (查看啟用 [API 層](d3d10-graphics-programming-guide-api-features-layers.md)的 [**D3D10 \_ 建立 \_ 裝置 \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)標列舉) 。 這些旗標可以是位 OR。

</dd> <dt>

*ppDevice* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

所建立之裝置的指標位址 (查看 [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) 介面) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

此函數會傳回下列其中一個 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

此函式會嘗試為硬體建立最佳裝置。 首先，此函式會嘗試建立10.1 裝置。 如果無法建立10.1 裝置，此函式會嘗試建立10.0 裝置。 如果未成功建立任何裝置，則函式會傳回 E \_ 失敗。

如果您的應用程式只需要建立10.1 裝置或僅限10.0 裝置，請改為使用下列功能：

-   您只能使用 [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) 函式來建立 Direct3D 10.0 裝置。
-   您只能使用 [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) 函式來建立 Direct3D 10.1 裝置。
-   您可以使用 [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md)函數，從 [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)介面指標取得 [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)介面指標。

只有在執行 Windows Vista Service Pack 1 或更新版本的電腦上，以及安裝 direct3d 10.1 相容的硬體時，才能建立 Direct3D 10.1 裝置。 不過，在執行任何已安裝 D3DX10 DLL 的 Windows 版本的電腦上呼叫此函式是合法的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Core。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
