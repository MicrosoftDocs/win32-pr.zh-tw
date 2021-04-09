---
description: 從. x 檔案載入第一個框架階層。
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: 'D3DXLoadMeshHierarchyFromX 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 308ebf127708849bec8ee8a4f2601f029562634a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946049"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a>D3DXLoadMeshHierarchyFromX 函式

從. x 檔案載入第一個框架階層。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*檔案名* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

指定檔案名之字串的指標。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，字串資料類型會解析為 LPCSTR。 請參閱＜備註＞。

</dd> <dt>

*MeshOptions* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

[**D3DXMESH**](./d3dxmesh.md)列舉中的一或多個旗標組合，可指定網格的建立選項。

</dd> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與網格相關聯的裝置物件。

</dd> <dt>

*pAlloc* \[在\]
</dt> <dd>

類型： **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

[**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)介面的指標。

</dd> <dt>

*pUserDataLoader* \[在\]
</dt> <dd>

類型： **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

應用程式提供的介面，可讓使用者資料載入。 請參閱 [**ID3DXLoadUserData**](id3dxloaduserdata.md)。

</dd> <dt>

*ppFrameHierarchy* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXFRAME**](d3dxframe.md)\***

傳回已載入框架階層的指標。 請參閱 [**D3DXFRAME**](d3dxframe.md)。

</dd> <dt>

*ppAnimController* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

傳回與. x 檔案中的動畫相對應的動畫控制器指標。 這會使用預設的追蹤和事件來建立。 請參閱 [**ID3DXAnimationController**](id3dxanimationcontroller.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXLoadMeshHierarchyFromXW。 否則，函式呼叫會解析為 D3DXLoadMeshHierarchyFromXA。

檔案中的所有網格都將折迭成一個輸出網格。 如果檔案包含框架階層，則所有轉換都會套用至網格。

**D3DXLoadMeshHierarchyFromX** 會從. x 檔案載入動畫資料和框架階層。 它會掃描. x 檔案，並根據透過 pAlloc 傳遞給它的 [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)衍生物件，建立框架階層和動畫控制器。 載入資料需要幾個步驟，如下所示：

1.  衍生 [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)，以執行每個方法。 這會控制如何配置和釋放畫面格和網格。
2.  衍生 [**ID3DXLoadUserData**](id3dxloaduserdata.md)，以執行每個方法。 如果您的. x 檔案沒有內嵌使用者定義的資料，或者您不需要它，您可以略過這個部分。
3.  建立 [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) 類別的物件，並選擇性地建立您的 LoadUserData 類別。 您不需要自行呼叫這些物件的任何方法。
4.  呼叫 **D3DXLoadMeshHierarchyFromX**，傳入您的 [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) 物件和 [**ID3DXLoadUserData**](id3dxloaduserdata.md) 物件 (或 **Null**) ，以建立框架階層和動畫控制器。 所有的動畫集合和框架都會自動註冊至動畫控制器。

在載入期間，會在每個畫面上呼叫 [**CreateFrame**](id3dxallocatehierarchy--createframe.md) 和 [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) ，以控制框架的載入和配置。 應用程式會定義這些方法來控制框架的儲存方式。 [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) 和 [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) 會在每個網格物件上被回呼，以控制網格物件的載入和配置。 針對不是由其他方法載入的每個最上層物件，會呼叫 [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) 。

若要釋放這項資料，請呼叫 ID3DXAnimationController：： Release 來釋出動畫集，並在框架階層的根節點和衍生 [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)類別的物件中傳遞 [**D3DXFRAMEDestroy**](d3dxframedestroy.md)。 系統會針對框架階層中的每個畫面格和網格物件呼叫 [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md)和 [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) 。 **DestroyFrame** 的執行應該釋出 [**CreateFrame**](id3dxallocatehierarchy--createframe.md)所配置的所有專案，同樣是針對網格容器方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[動畫函數](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
