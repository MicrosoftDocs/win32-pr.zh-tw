---
description: 取出與字型物件相關聯的 Direct3D 裝置。
ms.assetid: aad2406e-9461-4a84-9875-74b53d68ef40
title: 'ID3DX10Font：： GetDevice 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72719e07c62b681579162fda56000d2d6238bd52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986097"
---
# <a name="id3dx10fontgetdevice-method"></a>ID3DX10Font：： GetDevice 方法

取出與字型物件相關聯的 Direct3D 裝置。

## <a name="syntax"></a>語法


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppDevice* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

ID3D10Device 介面指標的位址，表示與字型物件相關聯的 Direct3D 裝置物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

> [!Note]  
> 呼叫這個方法將會增加 ID3D10Device 介面上的內部參考計數。 當您使用這個 ID3D10Device 介面完成時，請務必呼叫 IUnknown，否則會發生記憶體流失。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




