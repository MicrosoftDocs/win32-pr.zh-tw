---
title: 'glDrawElements 函式 (Gl) '
description: GlDrawElements 函式會從陣列資料呈現基本專案。
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- glDrawElements 函式 OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976e779235dc330467d610406156534b5e72841d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508791"
---
# <a name="gldrawelements-function"></a>glDrawElements 函式

**GlDrawElements** 函式會從陣列資料呈現基本專案。

## <a name="syntax"></a>語法


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mode* 
</dt> <dd>

要轉譯的基本類型。 它可以採用下列其中一個符號值： GL \_ 點、gl \_ 線區域 \_ 、gl \_ 線 \_ 迴圈、gl \_ 線、gl 三角形區域 \_ \_ 、gl \_ 三角形 \_ 風扇、gl \_ 三角形、gl \_ QUAD \_ 、gl \_ 四邊形和 gl \_ 多邊形。

</dd> <dt>

*計數* 
</dt> <dd>

要呈現的元素數目。

</dd> <dt>

*type* 
</dt> <dd>

索引中值的型別。 必須是 GL 不 \_ 帶正負號的 \_ 位元組、gl 不 \_ 帶正負號的 \_ 整數或 gl 不 \_ 帶正負號整數之一 \_ 。

</dd> <dt>

*指標* 
</dt> <dd>

儲存索引之位置的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *模式* 不是可接受的值。<br/>                                                                                          |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *計數* 為負數值。<br/>                                                                                              |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlDrawElements** 函式可讓您使用極少數的函式呼叫來指定多個幾何基本類型。 您可以事先指定個別的頂點、法線和色彩陣列，並使用它們來定義一系列的基本類型 (所有相同類型) 與 **glDrawElements** 的單一呼叫，而不是呼叫 OpenGL 函式來傳遞每個頂點、法線或色彩。

當您呼叫 **glDrawElements** 函式時，它會使用來自 *索引* 的 *計數* 順序元素，來建立一系列幾何基本專案。 *Mode* 參數指定要建立的基本類型，以及陣列元素如何用來建立這些基本專案。 如果 \_ \_ 未啟用 GL 頂點陣列，則不會產生任何幾何基本專案。

**GlDrawElements** 修改的頂點屬性在 **glDrawElements** 傳回之後具有未指定的值。 例如，如果 \_ \_ 已啟用 GL 色彩陣列，則在 **glDrawElements** 執行之後，目前色彩的值會是未定義的。 未修改的屬性會維持不變。

您可以在顯示清單中包含 **glDrawElements** 函數。 當 **glDrawElements** 包含在顯示清單中時，必要的陣列資料 (由陣列指標決定，而且也可以在顯示清單中輸入) 。 因為陣列指標和可啟用的是用戶端狀態變數，所以它們的值會在建立清單時影響顯示清單，而不是在執行清單時影響。

> [!Note]  
> **GlDrawElements** 函數僅適用于 OpenGL 1.1 版或更新版本。

 

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





