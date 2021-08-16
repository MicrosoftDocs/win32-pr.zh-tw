---
title: 'glFlush 函式 (Gl) '
description: GlFlush 函式會在有限的時間內強制執行 OpenGL 函數。
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- glFlush 函式 OpenGL
topic_type:
- apiref
api_name:
- glFlush
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece5f0aa96140b6fa16b5fbde1a857f1e14f1570ad7fc734626a27ac660a65ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360405"
---
# <a name="glflush-function"></a>glFlush 函式

**GlFlush** 函式會在有限的時間內強制執行 OpenGL 函數。

## <a name="syntax"></a>語法


```C++
void WINAPI glFlush(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

許多不同位置中的不同 OpenGL 執行緩衝區命令，包括網路緩衝區和圖形加速器本身。 **GlFlush** 函式會清空所有這些緩衝區，使所有發出的命令都能以實際轉譯引擎接受的速度快速執行。 雖然這項執行可能不會在任何特定時間內完成，但會在有限的時間內完成。

因為任何 OpenGL 程式可能會在網路上執行，或在緩衝命令的加速器上執行，所以請務必在要求所有先前發出的命令都已完成的程式中呼叫 **glFlush** 。 例如，在等候相依于所產生影像的使用者輸入之前，請先呼叫 **glFlush** 。

**GlFlush** 函式可以隨時返回。 它不會等到所有先前發行的 OpenGL 函式執行完成為止。

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

[**glFinish**](glfinish.md)
</dt> </dl>

 

 





