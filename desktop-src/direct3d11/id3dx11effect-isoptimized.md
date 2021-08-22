---
title: 'ID3DX11Effect IsOptimized 方法 (D3dx11effect .h) '
description: 測試效果，以查看反映中繼資料是否已從記憶體中移除。
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- IsOptimized 方法 Direct3D 11
- IsOptimized 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，IsOptimized 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd04bf43869f23bfec38db34be1b83b2c4f3953c7017120ebe2f0c985504b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124503"
---
# <a name="id3dx11effectisoptimized-method"></a>ID3DX11Effect：： IsOptimized 方法

測試效果，以查看反映中繼資料是否已從記憶體中移除。

## <a name="syntax"></a>語法


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

如果效果已優化，則為 **TRUE** ;否則 **為 FALSE**。

## <a name="remarks"></a>備註

效果會使用兩種不同方式的記憶體空間：儲存執行時間執行效果所需的資訊，以及儲存使用 API 將資訊反映回應用程式所需的中繼資料。 您可以藉由呼叫 [**ID3DX11Effect：： Optimize**](id3dx11effect-optimize.md) 來將反映中繼資料從記憶體中移除，以將效果所需的記憶體數量降到最低。 當然，將反映資料移除之後，讀取變數的 API 方法將無法再運作。

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

