---
title: 'ID3DX11ThreadPump ProcessDeviceWorkItems 方法 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 在裝置完成載入和處理之後，將工作專案設定為裝置。
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- ProcessDeviceWorkItems 方法 Direct3D 11
- ProcessDeviceWorkItems 方法 Direct3D 11，ID3DX11ThreadPump 介面
- ID3DX11ThreadPump 介面 Direct3D 11，ProcessDeviceWorkItems 方法
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.ProcessDeviceWorkItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad570785ac7dc36fb5dd9d464e97ef46f52ca93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974528"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a>ID3DX11ThreadPump：:P rocessDeviceWorkItems 方法

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

在裝置完成載入和處理之後，將工作專案設定為裝置。

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

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

要設定至裝置的工作專案數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

當執行緒抽取完成載入和處理資源或著色器時，它會將其保留在佇列中，直到呼叫此 API 為止，此時已處理的專案將會設定為裝置。 這對於控制每個畫面系將資源系結至裝置所花費的處理量相當有用。

例如，假設您接近遊戲的某個層級，而且您想要開始預先載入紋理、著色器和其他資源，以進行下一個層級。 執行緒抽取將開始在個別執行緒上載入、解壓縮和處理資源和著色器，直到它們準備好設定至裝置為止，此時會將它們保留在佇列中。 您可能不想要一次將所有資源和著色器設定為裝置，因為這可能會造成遊戲效能明顯降低的情況。 因此，每個框架可呼叫此 API 一次，如此一來，就只會在每個畫面上將一個小數位的工作專案設定為裝置，藉此將系結資源的工作負載分散到數個畫面上的裝置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

