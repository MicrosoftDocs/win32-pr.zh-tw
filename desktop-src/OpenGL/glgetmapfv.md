---
title: 'glGetMapfv 函式 (Gl) '
description: 'GlGetMapdv、glGetMapfv 和 glGetMapiv 函數會傳回評估工具參數。 |glGetMapfv 函式 (Gl) '
ms.assetid: dc93e468-7b76-4b5d-a46c-63920ed05568
keywords:
- glGetMapfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1bedb1b5ff07b7331eb740c46392e80ad324c6cef7f843978d9a5a41edf8da1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741588"
---
# <a name="glgetmapfv-function"></a>glGetMapfv 函式

[**GlGetMapdv**](glgetmapdv.md)、 **glGetMapfv** 和 [**glGetMapiv**](glgetmapiv.md)函數會傳回評估工具參數。

## <a name="syntax"></a>語法


```C++
void WINAPI glGetMapfv(
   GLenum  target,
   GLenum  query,
   GLfloat *v
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

地圖的符號名稱。 以下是接受的值： GL \_ MAP1 \_ COLOR \_ 4、gl \_ MAP1 \_ INDEX、gl \_ MAP1 \_ NORMAL、gl \_ MAP1 \_ 材質 \_ COORD \_ 1、gl \_ MAP1 \_ 材質 \_ COORD \_ 2、gl \_ MAP1 \_ 材質 \_ COORD \_ 3、gl \_ MAP1 \_ 材質 \_ COORD \_ 4、GL \_ MAP1 \_ 頂點 \_ 3、gl \_ MAP1 \_ 頂點 \_ 4、gl \_ LIST.MAP2 \_ COLOR \_ 4、GL \_ List.map2 \_ INDEX、gl \_ list.map2 \_ NORMAL、gl \_ list.map2 \_ 材質 \_ COORD \_ 1、gl \_ list.map2 \_ 材質 \_ COORD \_ 2、gl \_ list.map2 \_ 材質 \_ COORD \_ 3、gl list.map2 材質 COORD \_ \_ \_ \_ 4、gl \_ list.map2 \_ 頂點 \_ 3 和 gl \_ list.map2 \_ 頂點 \_ 4。

</dd> <dt>

*查詢* 
</dt> <dd>

指定要傳回的參數。 接受下列符號名稱。



| 值                                                                                                                                             | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <dt>**GL \_ COEFF**</dt> </dl>    | *V* 參數會傳回評估工具函數的控制點。 一維評估工具會傳回 *順序* 控制點，而二維評估工具會傳回 *uorder* *x* *vorder* 控制點。 每個控制點都包含一個、兩個、三個或四個整數、單精確度浮點數或雙精確度浮點值（視評估工具的類型而定）。 二維控制點會以資料列主要順序傳回、快速遞增 *uorder* 索引，以及每個資料列之後的 *vorder* 索引。 在要求時，整數值會藉由將內部浮點值四捨五入為最接近的整數值來計算。<br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <dt>**GL \_ 訂單**</dt> </dl>    | *V* 參數會傳回評估工具函數的順序。 一維評估工具會傳回單一值、 *order*。 二維評估工具會傳回兩個值： *uorder* 和 *vorder*。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <dt>**GL \_ 網域**</dt> </dl> | *V* 參數會傳回線性 *u* 和 *v* 對應參數。 一維評估工具會傳回兩個值，例如 *u* 1 和 *u* 2，如 [**glMap1**](glmap1.md)所指定。 二維評估工具會傳回四個值 (*u1*、 *u2*、 *V1* 和 *v2*) 如 [**glMap2**](glmap2.md)所指定。 在要求時，整數值會藉由將內部浮點值四捨五入為最接近的整數值來計算。<br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

*v* 
</dt> <dd>

傳回要求的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *目標* 或 *查詢* 不是可接受的值。<br/>                                                                             |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlGetMap** 函數會傳回評估工具參數。  (**glMap1** 和 **glMap2** 函式定義評估工具。 ) *target* 參數指定對應， *查詢* 會選取特定的參數，而 *v* 指向將傳回值的儲存區。

[**GlMap1**](glmap1.md)和 [**glMap2**](glmap2.md)會說明 *目標* 參數可接受的值。

如果產生錯誤，則不會對 *v* 內容進行任何變更。

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





