---
title: 'glReadBuffer 函式 (Gl) '
description: GlReadBuffer 函式會選取圖元的色彩緩衝區來源。
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- glReadBuffer 函式 OpenGL
topic_type:
- apiref
api_name:
- glReadBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e88cdcb2b1b3257b23606f8160e0986584db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966525"
---
# <a name="glreadbuffer-function"></a>glReadBuffer 函式

**GlReadBuffer** 函式會選取圖元的色彩緩衝區來源。

## <a name="syntax"></a>語法


```C++
void WINAPI glReadBuffer(
   GLenum mode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mode* 
</dt> <dd>

色彩緩衝區。 接受的值為 GL \_ front \_ 、gl \_ FRONT \_ 右邊、gl 向 \_ 左、gl 向右、 \_ \_ \_ gl \_ front、gl \_ back、gl \_ LEFT、GL \_ RIGHT，以及 gl \_ aux *i*，在 0 和 gl \_ aux \_ 緩衝區1之間。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *模式* 不是 12 (或更) 接受值的其中之一。<br/>                                                             |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | *模式* 指定了不存在的緩衝區。<br/>                                                                             |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlReadBuffer** 函式會將色彩緩衝區指定為後續 [**glReadPixels**](glreadpixels.md)和 [**glCopyPixels**](glcopypixels.md)命令的來源。 *Mode* 參數接受十二個或更多預先定義的值之一。 \_一律會定義透過 gl AUX3 的 (gl AUX0 \_ ) 。在完整設定的系統、gl \_ front、GL 左方和 gl 前端中，都是以 \_ \_ \_ 所有名稱作為左上角緩衝區、gl \_ front \_ 右邊和 gl 右邊 \_ 的 \_ \_ \_ 名稱，並將右緩衝區命名為後置緩衝區。

Nonstereo 雙重緩衝設定只會有左上角的緩衝區和左邊的緩衝區。 如果有身歷聲，單一緩衝的設定會有左上角和右中的緩衝區，而且只有在 nonstereo 時才會使用 front 左緩衝區。 將不存在的緩衝區指定給 **glReadBuffer** 是錯誤的。

根據預設， *模式* 在單一緩衝設定中是 gl \_ 前端，而 \_ 在雙緩衝設定中則為 gl。

下列函式會抓取 **glReadBuffer** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 讀取 \_ 緩衝區的 glGet

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> </dl>

 

 





