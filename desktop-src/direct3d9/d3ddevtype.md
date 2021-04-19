---
description: 定義裝置類型。
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: 'D3DDEVTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974849"
---
# <a name="d3ddevtype-enumeration"></a>D3DDEVTYPE 列舉

定義裝置類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE \_ HAL**
</dt> <dd>

硬體柵格化。 使用軟體、硬體或混合轉換和光源來完成陰影。

</dd> <dt>

<span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NullREF**
</dt> <dd>

在未提供硬體和參考光柵的電腦上初始化 Direct3D，並啟用建立3D 內容的資源。 請參閱＜備註＞。

</dd> <dt>

<span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ REF**
</dt> <dd>

Direct3D 功能是在軟體中執行;不過，參考轉譯器會在每次可以時使用特殊的 CPU 指示。

參考裝置是由 Windows SDK 8.0 或更新版本所安裝，旨在做為僅供開發之用的協助工具。

</dd> <dt>

<span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**
</dt> <dd>

已向 [**IDirect3D9：： RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice)註冊的可插入軟體裝置。

</dd> <dt>

<span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

如果指定了 D3DDEVTYPE NullREF，則採用 **D3DDEVTYPE** 裝置類型之 [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9)介面的所有方法都將會失敗 \_ 。 若要使用這些方法，請 \_ 在方法呼叫中替代 D3DDEVTYPE REF。

\_ \_ 除非需要頂點和索引緩衝區，否則應在 D3DPOOL 臨時記憶體中建立 D3DDEVTYPE REF 裝置。 若要支援頂點和索引緩衝區，請在 D3DPOOL SYSTEMMEM 記憶體中建立裝置 \_ 。

如果已安裝 D3dref9.dll，即使指定了 D3DDEVTYPE NullREF，Direct3D 仍會使用參考轉譯器來建立 D3DDEVTYPE \_ REF 裝置類型 \_ 。 如果 D3dref9.dll 無法使用且 \_ 已指定 D3DDEVTYPE NullREF，Direct3D 將不會轉譯或呈現場景。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**IDirect3D9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[**D3DDEVICE \_ 建立 \_ 參數**](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
