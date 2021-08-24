---
title: 'glSelectBuffer 函式 (Gl) '
description: GlSelectBuffer 函數會建立選取模式值的緩衝區。
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- glSelectBuffer 函式 OpenGL
topic_type:
- apiref
api_name:
- glSelectBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c40030c34ece43f4e24ac6937c35400fed7ab7acc005e99c653b233e08b69e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519818"
---
# <a name="glselectbuffer-function"></a>glSelectBuffer 函式

**GlSelectBuffer** 函數會建立選取模式值的緩衝區。

## <a name="syntax"></a>語法


```C++
void WINAPI glSelectBuffer(
   GLsizei size,
   GLuint  *buffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*size* 
</dt> <dd>

*緩衝區* 的大小。

</dd> <dt>

*緩衝區* 
</dt> <dd>

傳回選取資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *大小* 為負數。<br/>                                                                                                       |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 當轉譯模式為 GL SELECT 時，即會呼叫此函數 \_ 。<br/>                                                              |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlSelectBuffer** 函式有兩個參數： *buffer* 是不帶正負號整數陣列的指標，而 *size* 表示陣列的大小。 *Buffer* 參數會從名稱堆疊傳回值 (請參閱 [**glInitNames**](glinitnames.md)、 [**glLoadName**](glloadname.md)、 [**glPushName**](glpushname.md)) 當轉譯模式為 GL 時，請 \_ 選取 (查看 [**glRenderMode**](glrendermode.md)) 。 **GlSelectBuffer** 函式必須在啟用選取模式之前發出，而且當轉譯模式為 GL 選取時，不能發出此函數 \_ 。

程式設計師會使用選取範圍來決定要將哪些基本專案繪製到某個視窗的某個區域。 區域是由目前的模型和透視圖矩陣所定義。

在選取模式中，不會從柵格化產生任何圖元片段。 相反地，如果基本型別與 [視圖] 的 [剪取] 和 [使用者定義裁剪] 平面所定義的剪輯磁片區相交，則此基本型別會造成選取的點擊。 使用多邊形 (時，如果多邊形挑選，就不會發生命中。 ) 變更名稱堆疊，或呼叫 [**glRenderMode**](glrendermode.md) 時，如果在上一次這類事件之後發生任何命中，則會將叫用記錄複製到 *緩衝區* ，因為這類事件 (名稱堆疊變更或 **glRenderMode** 呼叫) 。 點擊記錄是由事件時名稱堆疊中的名稱數目所組成;然後是自從上一個事件以來碰到的所有頂點的最小和最大深度值;後面接著名稱堆疊內容、下名。

傳回的深度值會對應到最大的不帶正負號的整數值對應至視窗座標深度1.0，而零對應至視窗座標深度0.0。

當輸入選取模式時， *緩衝區* 的內部索引會重設為零。 每次將點擊記錄複製到 *緩衝區* 時，索引就會遞增，以指向下一個可用儲存格剛好超過 namesthat 區塊結尾的資料格。 如果點擊記錄大於 *緩衝區* 中剩餘的位置數目，就會複製符合可容納的資料量，並設定溢位旗標。 如果在複製點擊記錄時，名稱堆疊是空的，則該記錄是由零開始，後面接著最小和最大深度值。

使用 GL SELECT 以外的引數呼叫 **glRenderMode** ，結束選取模式 \_ 。 每當在轉譯模式為 GL 時呼叫 **glRenderMode** 時 \_ ，它會傳回復制到 *緩衝區* 的點擊記錄數目，重設溢位旗標和選取範圍緩衝區指標，並將名稱堆疊初始化為空白。 如果在呼叫 **glRenderMode** 時設定溢位，則會傳回負的命中記錄計數。

在使用 GL SELECT 以外的引數呼叫 [**glRenderMode**](glrendermode.md)之前，不會定義 *緩衝區* 的內容 \_ 。

**GlBegin** / **glEnd** 基本專案和對 [**glRasterPos**](glrasterpos-functions.md)的呼叫可能會導致點擊。

下列函式會抓取 **glSelectBuffer** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 名稱 \_ STACK \_ 深度的 glGet

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

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





