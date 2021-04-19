---
description: 描述目前的剪輯狀態。
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: 'D3DCLIPSTATUS9 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPSTATUS9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3b22fdfcc136c05ec8fe03ae491612606b2df62f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986501"
---
# <a name="d3dclipstatus9-structure"></a>D3DCLIPSTATUS9 結構

描述目前的剪輯狀態。

## <a name="syntax"></a>語法


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a>成員

<dl> <dt>

**ClipUnion**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

描述目前剪輯狀態的剪輯聯集旗標。 這個成員可以是下列其中一個或多個旗標：



| 值                                                                                                                                                      | 意義                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <dt>**D3DCS \_ 全部**</dt> </dl>          | 所有剪輯旗標的組合。<br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <dt>**\_左 D3DCS**</dt> </dl>       | 所有頂點都會由 [視圖] 的左平面裁剪。<br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <dt>**D3DCS \_ RIGHT**</dt> </dl>    | 所有頂點都會由「視圖」分隔的右平面裁剪。<br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <dt>**D3DCS \_ TOP**</dt> </dl>          | 所有頂點都是由「視圖」截斷的最上層平面所修剪。<br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <dt>**D3DCS \_ 底部**</dt> </dl> | 所有頂點都會由「視圖」分隔的下平面裁剪。<br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <dt>**D3DCS \_ FRONT**</dt> </dl>    | 所有頂點都是由「視圖」分隔的前平面所修剪。<br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <dt>**D3DCS \_ 回來**</dt> </dl>       | 所有頂點都是由「視圖」分隔的背面平面所修剪。<br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <dt>**D3DCS \_ PLANE0**</dt> </dl> | 應用程式定義的裁剪平面。<br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <dt>**D3DCS \_ PLANE1**</dt> </dl> | 應用程式定義的裁剪平面。<br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <dt>**D3DCS \_ PLANE2**</dt> </dl> | 應用程式定義的裁剪平面。<br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <dt>**D3DCS \_ PLANE3**</dt> </dl> | 應用程式定義的裁剪平面。<br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <dt>**D3DCS \_ PLANE4**</dt> </dl> | 應用程式定義的裁剪平面。<br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <dt>**D3DCS \_ PLANE5**</dt> </dl> | 應用程式定義的裁剪平面。<br/>                                 |



 

</dd> <dt>

**ClipIntersection**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

描述目前剪輯狀態的剪輯交集旗標。 這個成員可以採用與 ClipUnion 相同的旗標。

</dd> </dl>

## <a name="remarks"></a>備註

當 [**ProcessVertices**](/windows/desktop/api)、 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)或其他) 繪圖函式 (頂點處理期間啟用裁剪時，Direct3D 會計算每個頂點的剪輯代碼。 剪輯程式碼是 D3DCS 位的組合 \_ \* 。 當頂點在特定裁剪平面之外時，會在裁剪程式碼中設定對應的位。 Direct3D 會使用具有 ClipUnion 和 ClipIntersection 成員的 **D3DCLIPSTATUS9** 來維護剪輯狀態。 ClipUnion 是所有頂點剪輯代碼的位 OR，而 ClipIntersection 是所有頂點剪輯代碼的位 AND。 ClipUnion 的初始值為零，而 ClipIntersection 的值為0xFFFFFFFF。 當 D3DRS \_ 剪切設定為 **FALSE** 時，ClipUnion 和 ClipIntersection 會設定為零。 Direct3D 會在繪製呼叫期間更新剪輯狀態。 若要計算特定物件的剪輯狀態，請將 ClipUnion 和 ClipIntersection 設定為初始值並繼續繪製。

[**DrawRectPatch**](/windows/desktop/api)和 [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)不會更新剪輯狀態，因為它們沒有軟體模擬。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[**SetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
