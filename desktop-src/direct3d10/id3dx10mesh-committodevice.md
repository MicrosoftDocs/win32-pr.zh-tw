---
description: 將對網格所做的任何變更認可到裝置，以便轉譯變更。 這應該在網格的資料改變之後，以及轉譯之前呼叫。 除非已對裝置認可網狀，否則無法轉譯。 請參閱＜備註＞。
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: 'ID3DX10Mesh：： CommitToDevice 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CommitToDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 160f97a3a00ddc7bbf69989991b2794ab3d6e5e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035360"
---
# <a name="id3dx10meshcommittodevice-method"></a>ID3DX10Mesh：： CommitToDevice 方法

將對網格所做的任何變更認可到裝置，以便轉譯變更。 這應該在網格的資料改變之後，以及轉譯之前呼叫。 除非已對裝置認可網狀，否則無法轉譯。 請參閱＜備註＞。

## <a name="syntax"></a>語法


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

當網格載入時，就會將它的資料載入預備資源，這表示資料可以改變但無法轉譯。 呼叫 CommitToDevice 時，會將來自預備資源的資料複製到裝置資源，以便轉譯。 雖然資料會認可至裝置，但暫存資源仍可供修改。 如果對預備資源進行任何修改，則必須再次將預備資源認可至裝置，才能在螢幕上轉譯這些變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




