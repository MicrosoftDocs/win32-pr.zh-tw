---
title: 'glAddSwapHintRectWIN 函式 (Gl) '
description: GlAddSwapHintRectWIN 回呼函式會指定一組要由 SwapBuffers 複製的矩形。
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- glAddSwapHintRectWIN 函式 OpenGL
topic_type:
- apiref
api_name:
- glAddSwapHintRectWIN
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3e10c2f51ff8d7c9763ff1dad7d09d800cd60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384833"
---
# <a name="gladdswaphintrectwin-function"></a>glAddSwapHintRectWIN 函式

**GlAddSwapHintRectWIN** 回呼函式會指定一組要由 [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)複製的矩形。

## <a name="syntax"></a>語法


```C++
void WINAPI glAddSwapHintRectWIN(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*x* 
</dt> <dd>

視窗中的 *x* 座標 (會協調提示區域矩形左下角的) 。

</dd> <dt>

*y* 
</dt> <dd>

視窗中的 *y* 座標 (會協調提示區域矩形左下角的) 。

</dd> <dt>

*width* (寬度) 
</dt> <dd>

提示區域矩形的寬度。

</dd> <dt>

*height* (高度) 
</dt> <dd>

提示區域矩形的高度。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GlAddSwapHintRectWIN** 函式會藉由減少畫面格之間的重畫量來加快動畫的速度。 使用 **glAddSwapHintRectWIN**，您可以指定一組要在呼叫 [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)時複製的矩形區域。 當您在呼叫 **SwapBuffers** 之前未指定具有 **glAddSwapHintRectWIN** 的任何矩形時，會交換整個畫面格緩衝區。 使用 **glAddSwapHintRectWIN** 只複製已變更的緩衝區部分，可大幅提高 **SwapBuffers** 的效能，特別是在軟體中執行 **SwapBuffers** 時。

**GlAddSwapHintRectWIN** 函式會將矩形新增至提示區域。 當 \_ \_ 設定 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) 像素格式結構的 PFD SWAP COPY 旗標時， **SwapBuffers** 會使用此區域來將背景緩衝區的複製工作裁剪至前端緩衝區。 您不會指定 PFD \_ SWAP COPY，而 \_ 是由可用的硬體設定。 每次呼叫 **SwapBuffers** 之後，就會清除提示區域。 使用一些硬體設定時， **SwapBuffers** 可以忽略提示區域並交換整個緩衝區。 **SwapBuffers** 是由系統所執行，而不是由應用程式所執行。

OpenGL 會針對每個視窗維護個別的提示區域。 當您在與視窗相關聯的任何轉譯內容上呼叫 **glAddSwapHintRectWIN** 時，提示矩形會合並到單一區域中。

針對針對框架繪製的每個物件，使用周框矩形呼叫 **glAddSwapHintRectWIN** ，並清除每個矩形以清除先前的框架物件。

> [!Note]  
> **GlAddSwapHintRectWIN** 函式是延伸模組函式，不是標準 OpenGL 程式庫的一部分，而是 GL \_ WIN \_ 交換 \_ 提示擴充功能的一部分。 若要檢查您的 OpenGL 執行是否支援 **glAddSwapHintRectWIN**，請) 呼叫 **glGetString** (GL \_ 延伸模組。 如果它傳回 GL \_ WIN \_ 交換 \_ 提示，則會支援 **glAddSwapHintRectWIN** 。 若要取得擴充功能函式的位址，請呼叫 **wglGetProcAddress**。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                      |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Gl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





