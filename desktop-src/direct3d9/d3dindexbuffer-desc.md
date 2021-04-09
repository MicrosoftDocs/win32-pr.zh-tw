---
description: 描述索引緩衝區。
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: 'D3DINDEXBUFFER_DESC 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DINDEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a0bf63e732541f9394231cd82c23ff71a584b1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946128"
---
# <a name="d3dindexbuffer_desc-structure"></a>D3DINDEXBUFFER \_ DESC 結構

描述索引緩衝區。

## <a name="syntax"></a>語法


```C++
typedef struct D3DINDEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
} D3DINDEXBUFFER_DESC, *LPD3DINDEXBUFFER_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**格式**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

[D3DFORMAT](d3dformat.md)列舉型別的成員，描述索引緩衝區資料的介面格式。

</dd> <dt>

**型別**
</dt> <dd>

類型： **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

[**D3DRESOURCETYPE**](./d3dresourcetype.md)列舉型別的成員，將此資源識別為索引緩衝區。

</dd> <dt>

**使用量**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

下列其中一個或多個旗標的組合，指定此資源的使用方式。



| 值                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <dt>**D3DUSAGE \_ DONOTCLIP**</dt> </dl>                            | 設定以指出索引緩衝區內容永遠不需要剪切。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <dt>**D3DUSAGE \_ 動態**</dt> </dl>                                  | 設定以表示索引緩衝區需要動態記憶體使用。 這對驅動程式很有用，因為它可讓它們決定緩衝區的放置位置。 一般而言，靜態索引緩衝區會放置在視訊記憶體中，而且動態索引緩衝區會放置在 AGP 記憶體中。 請注意，沒有個別的靜態使用方式;如果您未指定 D3DUSAGE \_ 動態，索引緩衝區就會設為靜態。 D3DUSAGE \_ DYNAMIC 是透過 D3DLOCK \_ 捨棄和 D3DLOCK \_ NOOVERWRITE 鎖定旗標嚴格強制執行。 因此，D3DLOCK \_ 捨棄和 D3DLOCK \_ NOOVERWRITE 只適用于使用 D3DUSAGE 動態建立的索引緩衝區 \_ ; 它們在靜態頂點緩衝區上是不正確旗標。<br/> 如需使用動態索引緩衝區的詳細資訊，請參閱 [使用動態頂點和索引緩衝區](performance-optimizations.md)。<br/> 請注意， \_ 無法在 managed 索引緩衝區上指定 D3DUSAGE DYNAMIC。 如需詳細資訊，請參閱 [管理資源 (Direct3D 9) ](managing-resources.md)。<br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <dt>**D3DUSAGE \_ RTPATCHES**</dt> </dl>                            | 設定以指出何時要使用索引緩衝區來繪製高序位基本專案。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <dt>**D3DUSAGE \_ NPATCHES**</dt> </dl>                               | 設定以指出何時使用索引緩衝區來繪製 N 個修補程式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <dt>**D3DUSAGE \_ 點**</dt> </dl>                                     | 設定以指出何時要將索引緩衝區用於繪製點 sprite 或索引點清單。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <dt>**D3DUSAGE \_ SOFTWAREPROCESSING**</dt> </dl> | 設定以表示緩衝區要與軟體處理搭配使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <dt>**D3DUSAGE \_ WRITEONLY**</dt> </dl>                            | 通知系統應用程式只寫入索引緩衝區。 使用這個旗標可讓驅動程式選擇最佳的記憶體位置，以進行有效率的寫入作業和轉譯。 嘗試從使用這項功能建立的索引緩衝區讀取，可能會導致效能降低。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

**集區**
</dt> <dd>

類型： **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

[**D3DPOOL**](./d3dpool.md)列舉型別的成員，指定配置給此索引緩衝區的記憶體類別。

</dd> <dt>

**大小**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

索引緩衝區的大小（以位元組為單位）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[ (Direct3D 9) 的索引緩衝區 ](index-buffers.md)
</dt> </dl>

 

 
