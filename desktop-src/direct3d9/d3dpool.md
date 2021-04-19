---
description: 定義保存資源緩衝區的記憶體類別。
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: 'D3DPOOL 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPOOL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc1d69d094b2f810855f9ce2116c472ba8ab605e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985531"
---
# <a name="d3dpool-enumeration"></a>D3DPOOL 列舉

定義保存資源緩衝區的記憶體類別。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DPOOL { 
  D3DPOOL_DEFAULT      = 0,
  D3DPOOL_MANAGED      = 1,
  D3DPOOL_SYSTEMMEM    = 2,
  D3DPOOL_SCRATCH      = 3,
  D3DPOOL_FORCE_DWORD  = 0x7fffffff
} D3DPOOL, *LPD3DPOOL;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL \_ 預設值**
</dt> <dd>

資源會放在記憶體集區中，最適合指定資源所要求的一組使用方式。 這通常是視訊記憶體，包括本機視訊記憶體和 AGP 記憶體。 D3DPOOL \_ 預設集區與 D3DPOOL \_ MANAGED 和 D3DPOOL SYSTEMMEM 不同 \_ ，它指定將資源放在慣用的記憶體中，以供存取裝置。 請注意，D3DPOOL \_ 預設值絕對不會指出 \_ 應該選擇 D3DPOOL MANAGED 或 D3DPOOL \_ SYSTEMMEM 做為此資源的記憶體集區類型。 放在 D3DPOOL 預設集區中的材質 \_ 無法鎖定，除非它們是動態紋理或私用、FOURCC、驅動程式格式。 若要存取 unlockable 材質，您必須使用 [**IDirect3DDevice9：： UpdateSurface**](/windows/desktop/api)、 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)、 [**IDirect3DDevice9：： GetFrontBufferData**](/windows/desktop/api)和 [**IDirect3DDevice9：： GetRenderTargetData**](/windows/desktop/api)等函數。 D3DPOOL \_ 受控的選擇可能比 \_ 大多數應用程式的 D3DPOOL 預設值更好。 請注意，在驅動程式專屬像素格式中建立的某些紋理（Direct3D 執行時間不明）可以鎖定。 另請注意，-不同于材質交換鏈回緩衝區、轉譯目標、頂點緩衝區和索引緩衝區都可以鎖定。 裝置遺失時，必須先釋出使用 D3DPOOL 預設建立的資源， \_ 然後再呼叫 [**IDirect3DDevice9：： Reset**](/windows/desktop/api)。 如需詳細資訊，請參閱 [ (Direct3D 9) 的遺失裝置 ](lost-devices.md)。

使用 D3DPOOL 建立資源時 \_ ，如果已認可視訊卡記憶體，將會收回 managed 資源以釋出足夠的記憶體來滿足要求。

</dd> <dt>

<span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL \_ 受控**
</dt> <dd>

系統會視需要自動將資源複製到裝置可存取的記憶體。 受管理的資源是由系統記憶體所支援，且不需要在裝置遺失時重新建立。 如需詳細資訊，請參閱 [ (Direct3D 9 管理資源) ](managing-resources.md) 。 受控資源可以鎖定。 系統只會直接修改系統記憶體複製。 Direct3D 會視需要將您的變更複製到驅動程式可存取的記憶體。



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D 9 與 Direct3D 9Ex 之間的差異：<br/> D3DPOOL \_ MANAGED 適用于 [**IDirect3DDevice9**](/windows/desktop/api)，但它對 [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)而言是不正確。<br/> |



 

</dd> <dt>

<span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL \_ SYSTEMMEM**
</dt> <dd>

資源會放在通常不是由 Direct3D 裝置存取的記憶體中。 此記憶體配置會耗用系統 RAM，但不會減少可分頁的 RAM。 裝置遺失時，不需要重新建立這些資源。 此集區中的資源可以鎖定，並可作為 [**IDirect3DDevice9：： UpdateSurface**](/windows/desktop/api) 或 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) 作業的來源，以使用 D3DPOOL 預設建立的記憶體資源 \_ 。

</dd> <dt>

<span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL \_ 臨時**
</dt> <dd>

資源會放在系統 RAM 中，而且不需要在裝置遺失時重新建立。 這些資源不是依裝置大小或格式限制來系結。 因此，Direct3D 裝置無法存取這些資源，也無法將其設定為紋理或轉譯目標。 不過，您一律可以建立、鎖定和複製這些資源。

</dd> <dt>

<span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

所有的集區類型都適用于所有資源，包括：頂點緩衝區、索引緩衝區、材質和表面。

下表指出針對轉譯目標、深度樣板和動態和 mipmap 使用方式的集區類型限制。 X 表示相容的組合;缺少 x 表示不相容。



| 集區               | D3DUSAGE \_ RENDERTARGET | D3DUSAGE \_ DEPTHSTENCIL |
|--------------------|------------------------|------------------------|
| D3DPOOL \_ 預設值   | x                      | x                      |
| D3DPOOL \_ 受控   |                        |                        |
| D3DPOOL \_ 臨時   |                        |                        |
| D3DPOOL \_ SYSTEMMEM |                        |                        |



 



| 集區               | D3DUSAGE \_ 動態 | D3DUSAGE \_ AUTOGENMIPMAP |
|--------------------|-------------------|-------------------------|
| D3DPOOL \_ 預設值   | x                 | x                       |
| D3DPOOL \_ 受控   |                   | x                       |
| D3DPOOL \_ 臨時   |                   |                         |
| D3DPOOL \_ SYSTEMMEM | x                 |                         |



 

如需使用類型的詳細資訊，請參閱 [**D3DUSAGE**](d3dusage.md)。

集區無法針對 mipmap) 中一個資源 (mip 層級內包含的不同物件混合使用，而且當選擇集區時，就無法變更。

應用程式應該 \_ 針對大部分靜態資源使用 D3DPOOL 管理，因為這可讓應用程式不需要處理遺失的裝置。 執行時間會還原 (的受控資源。 ) 這對 (UMA) 系統的統一記憶體架構特別有用。 其他動態資源不適合用于 D3DPOOL \_ 管理。 事實上，您無法使用 D3DPOOL \_ MANAGED 搭配 D3DUSAGE DYNAMIC 來建立索引緩衝區和頂點緩衝區 \_ 。

若為動態紋理，有時會想要使用一對影片記憶體和系統記憶體材質，使用 D3DPOOL \_ 預設值和系統記憶體（使用 D3DPOOL SYSTEMMEM）配置視訊記憶體 \_ 。 您可以使用鎖定方法來鎖定和修改系統記憶體材質的位。 然後，您可以使用 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)來更新視訊記憶體材質。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DUSAGE**](d3dusage.md)
</dt> <dt>

[**IDirect3DDevice9::CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
</dt> <dt>

[**IDirect3DDevice9::CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
</dt> <dt>

[**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
</dt> <dt>

[**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
</dt> <dt>

[**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
</dt> <dt>

[**D3DINDEXBUFFER \_ DESC**](d3dindexbuffer-desc.md)
</dt> <dt>

[**D3DSURFACE \_ DESC**](d3dsurface-desc.md)
</dt> <dt>

[**D3DVERTEXBUFFER \_ DESC**](d3dvertexbuffer-desc.md)
</dt> <dt>

[**D3DVOLUME \_ DESC**](d3dvolume-desc.md)
</dt> </dl>

 

 
