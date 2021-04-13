---
title: 'glPolygonOffset 函式 (Gl) '
description: GlPolygonOffset 函式會設定 OpenGL 用來計算深度值的小數位數和單位數。
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- glPolygonOffset 函式 OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fa7d130fcc300fc1ebe33d091253e33f2d1e03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384813"
---
# <a name="glpolygonoffset-function"></a>glPolygonOffset 函式

**GlPolygonOffset** 函式會設定 OpenGL 用來計算深度值的小數位數和單位數。

## <a name="syntax"></a>語法


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*因素* 
</dt> <dd>

指定用來為每個多邊形建立可變深度位移的比例因數。 初始值為零。

</dd> <dt>

*單位* 
</dt> <dd>

指定乘以實值指定值的值，以建立常數深度位移。 初始值為0。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

當 \_ 啟用 GL 多邊形 \_ 位移時，每個片段的深度值將會在從適當頂點的深度值中插補之後位移。 位移的值是 *係數* \* ？ z + r \* *單位*，其中？ z 是相對於多邊形螢幕區域的變更深度度量，而 r 是保證為指定的執行產生可解析位移的最小值。 在執行深度測試之前，以及將值寫入深度緩衝區之前，會加入位移。

**GlPolygonOffset** 函式適用于轉譯隱藏行影像、將 decals 套用至表面，以及用來呈現具有反白顯示邊緣的純色。

**GlPolygonOffset** 函式對在意見緩衝區中放置的深度座標沒有任何作用。 它也不會影響選取專案。

下列函式會取出與 **glPolygonOffset** 相關的資訊：

-   [](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 多邊形 \_ 位移 \_ 因數的 glGet
-   [](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 多邊形 \_ 位移 \_ 單位的 glGet
-   [](glisenabled.md)具有引數 GL \_ 多邊形 \_ 位移 \_ 填滿的 glIsEnabled
-   [](glisenabled.md)具有引數 GL \_ 多邊形 \_ 位移 \_ 線的 glIsEnabled
-   [](glisenabled.md)具有引數 GL \_ 多邊形 \_ 位移 \_ 點的 glIsEnabled

> [!Note]  
> **GlPolygonOffset** 函式僅適用于 OpenGl 1.1 版或更高版本。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Gl</dt> </dl>         |
| 程式庫<br/>                  | <dl> <dt>Opengl32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





