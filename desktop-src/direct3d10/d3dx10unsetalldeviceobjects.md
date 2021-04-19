---
description: 將所有資源的指標設為 Null，以移除裝置中的所有資源。 這應該會在應用程式關閉時呼叫。 這有助於確保當某個資源釋出所有資源時，都不會將這些資源系結至裝置。
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: 'D3DX10UnsetAllDeviceObjects 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10UnsetAllDeviceObjects
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4d3a113be935f77dbd62b2f3fac4c16c7cac9881
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976488"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a>D3DX10UnsetAllDeviceObjects 函式

將所有資源的指標設為 **Null**，以移除裝置中的所有資源。 這應該會在應用程式關閉時呼叫。 這有助於確保當某個資源釋出所有資源時，都不會將這些資源系結至裝置。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

裝置的指標。 請參閱 [**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




