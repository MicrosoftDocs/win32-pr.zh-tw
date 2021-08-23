---
description: 抓取在建立時為此網格啟用的網格選項。
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: 'ID3DXBaseMesh：： GetOptions 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetOptions
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b8ed6281e1418246027a05f281ef5c01d8fbe757a8bd88d2bf6f44ca41ed1d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121760"
---
# <a name="id3dxbasemeshgetoptions-method"></a>ID3DXBaseMesh：： GetOptions 方法

抓取在建立時為此網格啟用的網格選項。

## <a name="syntax"></a>語法


```C++
DWORD GetOptions();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

傳回下列一或多個旗標的組合，表示在建立時為此網格啟用的選項。



| 值                   | 描述                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXMESH \_ 32 位         | 使用32位的索引。                                                                                                                                                                              |
| D3DXMESH \_ DONOTCLIP     | \_針對頂點和索引緩衝區使用 D3DUSAGE DONOTCLIP usage 旗標。                                                                                                                             |
| D3DXMESH \_ 動態       | 相當於同時指定 D3DXMESH \_ VB \_ 動態和 D3DXMESH \_ IB \_ 動態。                                                                                                                   |
| D3DXMESH \_ RTPATCHES     | \_針對頂點和索引緩衝區使用 D3DUSAGE RTPATCHES usage 旗標。                                                                                                                             |
| D3DXMESH \_ NPATCHES      | 指定此旗標會讓網格的頂點和索引緩衝區以 D3DUSAGE \_ NPATCHES 旗標建立。 如果要使用 N 修補程式增強功能來呈現網格物件，則這是必要的。 |
| D3DXMESH \_ 受控       | 相當於指定 D3DXMESH \_ VB \_ managed 和 D3DXMESH \_ IB \_ managed。                                                                                                                   |
| D3DXMESH \_ 點        | \_針對頂點和索引緩衝區使用 D3DUSAGE 點使用方式旗標。                                                                                                                                |
| D3DXMESH \_ IB \_ 動態   | 使用 \_ 索引緩衝區的 D3DUSAGE 動態使用旗標。                                                                                                                                          |
| D3DXMESH \_ IB \_ 管理   | 將 D3DPOOL \_ 受控記憶體類別用於索引緩衝區。                                                                                                                                         |
| D3DXMESH \_ IB \_ SYSTEMMEM | 將 D3DPOOL \_ SYSTEMMEM memory 類別用於索引緩衝區。                                                                                                                                       |
| D3DXMESH \_ IB \_ WRITEONLY | 使用 \_ 索引緩衝區的 D3DUSAGE WRITEONLY 使用旗標。                                                                                                                                        |
| D3DXMESH \_ SYSTEMMEM     | 相當於同時指定 D3DXMESH \_ VB \_ SYSTEMMEM 和 D3DXMESH \_ IB \_ SYSTEMMEM。                                                                                                               |
| D3DXMESH \_ VB \_ 動態   | \_針對頂點緩衝區使用 D3DUSAGE 動態使用旗標。                                                                                                                                         |
| D3DXMESH \_ VB \_ 受控   | \_針對頂點緩衝區使用 D3DPOOL 受控記憶體類別。                                                                                                                                        |
| D3DXMESH \_ VB \_ SYSTEMMEM | \_針對頂點緩衝區使用 D3DPOOL SYSTEMMEM memory 類別。                                                                                                                                      |
| D3DXMESH \_ VB \_ WRITEONLY | \_針對頂點緩衝區使用 D3DUSAGE WRITEONLY 使用旗標。                                                                                                                                       |
| D3DXMESH \_ WRITEONLY     | 相當於同時指定 D3DXMESH \_ VB \_ WRITEONLY 和 D3DXMESH \_ IB \_ WRITEONLY。                                                                                                               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
