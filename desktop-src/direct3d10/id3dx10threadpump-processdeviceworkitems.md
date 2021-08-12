---
description: 在裝置完成載入和處理之後，將工作專案設定為裝置。
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: 'ID3DX10ThreadPump：:P rocessDeviceWorkItems 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.ProcessDeviceWorkItems
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e7179cf285c056601d00df5126ba98aaa34f827cbcac15400166d8301dc143a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301774"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a>ID3DX10ThreadPump：:P rocessDeviceWorkItems 方法

在裝置完成載入和處理之後，將工作專案設定為裝置。 當執行緒抽取完成載入和處理資源或著色器時，它會將其保留在佇列中，直到呼叫此 API 為止，此時已處理的專案將會設定為裝置。 這對於控制每個畫面系將資源系結至裝置所花費的處理量相當有用。 請參閱＜備註＞。

## <a name="syntax"></a>語法


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*iWorkItemCount* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要設定至裝置的工作專案數。 ProcessDeviceObjectCreation 會建立最多 iWorkItemCount 的物件。 如果佇列中沒有足夠的工作專案來處理 iWorkItemCount 物件，ProcessDeviceObjectCreation 將會建立與佇列中的專案數目一樣多的裝置物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

例如，假設您接近遊戲的某個層級，而且您想要開始預先載入紋理、著色器和其他資源，以進行下一個層級。 執行緒抽取將開始在個別執行緒上載入、解壓縮和處理資源和著色器，直到它們準備好設定至裝置為止，此時會將它們保留在佇列中。 您可能不想要一次將所有資源和著色器設定為裝置，因為這可能會導致遊戲效能的明顯暫時變慢。 因此，每個框架可呼叫此 API 一次，如此一來，就只會在每個畫面上將一個小數位的工作專案設定為裝置，藉此將系結資源的工作負載分散到裝置上的數個框架，並將遊戲效能降低明顯的可能性降至最低。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
