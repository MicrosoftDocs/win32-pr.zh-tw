---
title: 'glFrontFace 函式 (Gl) '
description: GlFrontFace 函式會定義正面和背面的多邊形。
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- glFrontFace 函式 OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106fa40989f21e50eb738f1a218394e8e7e9b4bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935067"
---
# <a name="glfrontface-function"></a>glFrontFace 函式

**GlFrontFace** 函式會定義正面和背面的多邊形。

## <a name="syntax"></a>語法


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mode* 
</dt> <dd>

正面多邊形的方向。 \_已接受 gl CW 和 gl \_ CCW。 預設值為 GL \_ CCW。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *模式* 不是可接受的值。<br/>                                                                                          |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

在完全由不透明封閉表面組成的場景中，永遠不會看到背面的多邊形。 排除這些隱藏的多邊形具有加速影像呈現的明顯優點。 您可以使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) （使用引數 GL 剔除臉部）來啟用和停用後置多邊形 \_ \_ 。

將多邊形的座標投射到視窗座標時，會被視為具有順向繞組，如果在路徑的第一個頂點、第二個頂點等之後，最後一個頂點，最後再回到第一個頂點，則會以順向方向與多邊形內部移動。 如果在相同路徑後面的虛數物件以逆時針方向移動多邊形內部的方向，則會將多邊形的纏繞視為逆時針。 **GlFrontFace** 函式會指定在視窗座標中具有順時針繞組的多邊形，或在視窗座標中以逆時針方式纏繞的多邊形，會被正面朝上。 將 GL \_ CCW 傳遞至 *模式* 時，會選取逆時針多邊形作為正面的多邊形;GL \_ CW 會選取順時針多邊形作為正面的多邊形。 依預設，會將逆時針多邊形視為正面朝上。

下列函數會抓取 **glFrontface** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 正面 \_ 臉部的 glGet

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

[**glCullFace**](glcullface.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





