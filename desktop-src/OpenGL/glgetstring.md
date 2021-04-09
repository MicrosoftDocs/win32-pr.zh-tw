---
title: 'glGetString 函式 (Gl) '
description: GlGetString 函式會傳回描述目前 OpenGL 連接的字串。
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- glGetString 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetString
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e263e35802af752fa262c898d036fccaa37aff87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934987"
---
# <a name="glgetstring-function"></a>glGetString 函式

**GlGetString** 函式會傳回描述目前 OpenGL 連接的字串。

## <a name="syntax"></a>語法


```C++
const GLubyte* WINAPI glGetString(
   GLenum name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*name* 
</dt> <dd>

下列其中一個符號常數。



| 值                                                                                                                                                         | 意義                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <dt>**GL \_ 廠商**</dt> </dl>             | 傳回負責此 OpenGL 實的公司。 此名稱不會因為版本而變更。<br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <dt>**GL \_ 轉譯器**</dt> </dl>       | 傳回轉譯器的名稱。 此名稱通常專屬於特定的硬體平臺設定。 它不會因發行而變更。<br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <dt>**GL \_ 版本**</dt> </dl>          | 傳回版本或版本號碼。<br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <dt>**GL \_ 延伸模組**</dt> </dl> | 傳回 OpenGL 支援的延伸模組清單（以空格分隔）。<br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *名稱* 不是可接受的值。<br/>                                                                                          |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlGetString** 函式會傳回靜態字串的指標，此字串描述目前 OpenGL 連接的某個方面。

由於 OpenGL 不包含執行效能特性的查詢，因此某些應用程式應該會被撰寫以辨識已知的平臺，並根據這些平臺的已知效能特性修改其 OpenGL 使用量。 字串 GL \_ 廠商和 GL 轉譯器 \_ 會以唯一的方式指定平臺，而不會從版本變更為版本。 它們應該以平臺辨識演算法的形式來使用。

**GlGetString** 所傳回之字串的格式和內容取決於執行，不同之處在于：

-   延伸模組名稱不會包含空白字元，而且會以 GL 擴充字串中的空白字元分隔 \_ 。
-   GL \_ 版本字串的開頭為版本號碼。 版本號碼會使用下列其中一種形式：

    *主要 \_ 號碼*。*次要 \_ 編號*

    *主要 \_ 號碼*。*次要 \_ 號碼*。*版本 \_ 號碼*

-   廠商特定的資訊可能會遵循版本號碼。 其格式取決於執行，但空格一律會分隔版本號碼和廠商專屬的資訊。
-   所有字串都以 null 終止。

如果產生錯誤， **glGetString** 會傳回零。

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
</dt> </dl>

 

 





