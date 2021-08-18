---
description: 描述裝置的建立參數。
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: 'D3DDEVICE_CREATION_PARAMETERS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 64b3e13300d6c305d06b6b13db246134cb889cbfc407e4a99c6ae45adbf916e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805017"
---
# <a name="d3ddevice_creation_parameters-structure"></a>D3DDEVICE \_ 建立 \_ 參數結構

描述裝置的建立參數。

## <a name="syntax"></a>語法


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a>成員

<dl> <dt>

**AdapterOrdinal**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

表示顯示配接器的序數。 D3DADAPTER \_ 預設一律是主顯示器介面卡。 使用此序數做為任何 [**IDirect3D9**](/windows/desktop/api) 方法的介面卡參數。 請注意，Direct3D 9.0 物件的不同實例可以使用不同的序數。 例如，當使用者新增或移除多個監視器系統中的監視時，或當他們熱交換膝上型電腦時，介面卡可進入或離開系統。 因此，您只能在已知有效的 Direct3D 9.0 實例中使用此序數，也就是建立此 [**IDirect3DDevice9**](/windows/desktop/api) 介面的 direct3d 9.0 或從 [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d)傳回的 direct3d 9.0，如同透過這個 **IDirect3DDevice9** 介面所呼叫。

</dd> <dt>

**DeviceType**
</dt> <dd>

類型： **[ **D3DDEVTYPE**](./d3ddevtype.md)**

</dd> <dd>

[**D3DDEVTYPE**](./d3ddevtype.md)列舉型別的成員。 代表此裝置的模擬功能數量。 此參數的值會反映傳遞給建立此裝置之 [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) 呼叫的值。

</dd> <dt>

**hFocusWindow**
</dt> <dd>

類型： **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

焦點屬於此 Direct3D 裝置的視窗控制碼。 此參數的值會反映傳遞給建立此裝置之 [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) 呼叫的值。

</dd> <dt>

**BehaviorFlags**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

一或多個 [D3DCREATE](d3dcreate.md) 常數的組合，可控制裝置的全域行為。 這些常數會在建立裝置時反映傳遞給 [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) 的常數。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetCreationParameters**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
