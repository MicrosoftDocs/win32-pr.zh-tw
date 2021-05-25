---
description: 識別查詢類型。
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: 'D3DQUERYTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7a9c20050e7d0dce5a19664d937c016a475a9a13
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343073"
---
# <a name="d3dquerytype-enumeration"></a>D3DQUERYTYPE 列舉

識別查詢類型。 如需查詢的詳細資訊，請參閱 [ (Direct3D 9 的查詢) ](queries.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_ResourceManager    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ VCACHE**
</dt> <dd>

查詢有關頂點快取之資料配置的驅動程式提示。

</dd> <dt>

<span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**
</dt> <dd>

查詢資源管理員。 針對此查詢，裝置行為旗標必須包含 [D3DCREATE \_ 停用 \_ 驅動程式 \_ 管理](d3dcreate.md)。

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**
</dt> <dd>

查詢頂點統計資料。

</dd> <dt>

<span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE \_ 事件**
</dt> <dd>

查詢從 API 呼叫發出的任何和所有非同步事件。

</dd> <dt>

<span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE \_ 遮蔽**
</dt> <dd>

遮蔽查詢會傳回通過 z 測試的圖元數。 這些圖元適用于 [**D3DISSUE \_ BEGIN**](d3dissue-begin.md) 和 [**D3DISSUE \_ END**](d3dissue-end.md)問題之間繪製的基本專案。 這可讓應用程式針對0檢查遮蔽結果。 零是完全 pixels occluded 的，這表示目前相機位置看不到圖元。

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE \_ 時間戳記**
</dt> <dd>

傳回64位的時間戳記。

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ TIMESTAMPDISJOINT**
</dt> <dd>

如果計數器頻率已從 D3DQUERYTYPE 時間戳記變更，請使用此查詢來通知應用程式 \_ 。

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ TIMESTAMPFREQ**
</dt> <dd>

如果 D3DQUERYTYPE 時間戳記查詢中的值在 \_ D3DQUERYTYPE TIMESTAMPDISJOINT 查詢的整個持續期間無法保證是連續的，則此查詢結果為 TRUE \_ 。 否則，查詢結果會是 **FALSE**。

</dd> <dt>

<span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ PIPELINETIMINGS**
</dt> <dd>

處理管線資料的時間百分比。

</dd> <dt>

<span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE \_ INTERFACETIMINGS**
</dt> <dd>

驅動程式中處理資料的時間百分比。

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ VERTEXTIMINGS**
</dt> <dd>

處理頂點著色器資料的時間百分比。

</dd> <dt>

<span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ PIXELTIMINGS**
</dt> <dd>

處理圖元著色器資料的時間百分比。

</dd> <dt>

<span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**
</dt> <dd>

協助您瞭解應用程式效能的輸送量度量比較。

</dd> <dt>

<span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**
</dt> <dd>

測量紋理和索引頂點的快取點擊率效能。

</dd> <dt>

<span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**
</dt> <dd>

包含在 [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) 結構中的記憶體配置效率。

Direct3D 9 與 Direct3D 9Ex 之間的差異：

- D3DQUERYTYPE \_ MEMORYPRESSURE 僅適用于在 Windows 7 上執行的 Direct3D9Ex (或更多目前的作業系統) 。



 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9：： CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
