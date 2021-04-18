---
title: GL 函數
description: GL 函數
ms.assetid: 44773cd3-1cb9-4d59-9a10-6a9e7e6516cc
keywords:
- OpenGL、GL 函數
- OpenGL 參考、GL 函數
- GL 函數 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5968a49c6774f4cf7fa1218ab1d8e7b27db7649
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966207"
---
# <a name="gl-functions"></a>GL 函數

在這裡會顯示 OpenGL 命令（以字母順序排列）。 每個參考頁面都會描述一個或多個函式。 另請參閱 [x.glu 隊](glu-functions.md)函式。



| 函式                                                                                                                                       | 描述                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**glAccum**](glaccum.md)                                                                                                                     | 在累積緩衝區上運作。                                                                                  |
| [**glAddSwapHintRectWIN**](gladdswaphintrectwin.md)                                                                                           | 指定 [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)要複製的一組矩形。                            |
| [**glAlphaFunc**](glalphafunc.md)                                                                                                             | 可讓您的應用程式設定 Alpha 測試函數。                                                              |
| [**glAreTexturesResident**](glaretexturesresident.md)                                                                                         | 判斷指定的材質物件是否常駐在材質記憶體中。                                          |
| [**glArrayElement**](glarrayelement.md)                                                                                                       | 指定用來呈現頂點的陣列元素。                                                                 |
| [**glBegin**](glbegin.md)、 [ **glEnd**](glend.md)                                                                                             | 分隔基本或類似基本類型群組的頂點。                                                    |
| [**glBindTexture**](glbindtexture.md)                                                                                                         | 可建立系結至材質目標的命名材質。                                            |
| [**glBitmap**](glbitmap.md)                                                                                                                   | 繪製點陣圖。                                                                                                       |
| [**glBlendFunc**](glblendfunc.md)                                                                                                             | 指定圖元算術。                                                                                           |
| [**glCallList**](glcalllist.md)                                                                                                               | 執行顯示清單。                                                                                              |
| [**glCallLists**](glcalllists.md)                                                                                                             | 執行顯示清單清單。                                                                                     |
| [**glClear**](glclear.md)                                                                                                                     | 清除緩衝區為預設值。                                                                                      |
| [**glClearAccum**](glclearaccum.md)                                                                                                           | 指定累積緩衝區的明確值。                                                               |
| [**glClearColor**](glclearcolor.md)                                                                                                           | 指定色彩緩衝區的明確值。                                                                         |
| [**glClearDepth**](glcleardepth.md)                                                                                                           | 指定深度緩衝區的清除值。                                                                       |
| [**glClearIndex**](glclearindex.md)                                                                                                           | 指定色彩索引緩衝區的清除值。                                                                |
| [**glClearStencil**](glclearstencil.md)                                                                                                       | 指定樣板緩衝區的清除值。                                                                     |
| [**glClipPlane**](glclipplane.md)                                                                                                             | 指定要對其裁剪所有幾何的平面。                                                              |
| [**glColor**](glcolor-functions.md) 函式                                                                                                 | 設定目前的色彩。                                                                                                |
| [**glColorMask**](glcolormask.md)                                                                                                             | 啟用和停用框架緩衝區色彩元件的寫入。                                                        |
| [**glColorMaterial**](glcolormaterial.md)                                                                                                     | 導致材質色彩追蹤目前的色彩。                                                                   |
| [**glColorPointer**](glcolorpointer.md)                                                                                                       | 定義色彩的陣列。                                                                                           |
| [**glColorTableEXT**](glcolortableext.md)                                                                                                     | 指定目標調色板材質之調色板的格式和大小。                                            |
| [**glColorSubTableEXT**](glcolorsubtableext.md)                                                                                               | 指定要取代之目標材質調色板的一部分。                                                 |
| [**glCopyPixels**](glcopypixels.md)                                                                                                           | 複製畫面格緩衝區中的圖元。                                                                                     |
| [**glCopyTexImage1D**](glcopyteximage1d.md)                                                                                                   | 將畫面格緩衝區中的圖元複製到一維材質影像。                                              |
| [**glCopyTexImage2D**](glcopyteximage2d.md)                                                                                                   | 將畫面格緩衝區的圖元複製到二維紋理影像。                                              |
| [**glCopyTexSubImage1D**](glcopytexsubimage1d.md)                                                                                             | 從畫面格緩衝區複製一維材質影像的子影像。                                           |
| [**glCopyTexSubImage2D**](glcopytexsubimage2d.md)                                                                                             | 從畫面格緩衝區複製二維材質影像的子影像。                                           |
| [**glCullFace**](glcullface.md)                                                                                                               | 指定是否可以挑選前端或後端的 facet。                                                         |
| [**glDeleteLists**](gldeletelists.md)                                                                                                         | 刪除連續的顯示清單群組。                                                                          |
| [**glDeleteTextures**](gldeletetextures.md)                                                                                                   | 刪除命名的材質。                                                                                               |
| [**glDepthFunc**](gldepthfunc.md)                                                                                                             | 指定用於深度緩衝區比較的值。                                                                |
| [**glDepthMask**](gldepthmask.md)                                                                                                             | 啟用或停用寫入深度緩衝區。                                                                    |
| [**glDepthRange**](gldepthrange.md)                                                                                                           | 指定從正規化的裝置座標至視窗座標之 *z* 值的對應。                         |
| [**glDrawArrays**](gldrawarrays.md)                                                                                                           | 指定要轉譯的多個基本類型。                                                                              |
| [**glDrawBuffer**](gldrawbuffer.md)                                                                                                           | 指定要繪製的色彩緩衝區。                                                                   |
| [**glDrawElements**](gldrawelements.md)                                                                                                       | 從陣列資料呈現基本專案。                                                                                   |
| [**glDrawPixels**](gldrawpixels.md)                                                                                                           | 將圖元區塊寫入至畫面格緩衝區。                                                                          |
| [**glEdgeFlag**](gledgeflag-functions.md) 函式                                                                                           | 定義邊緣旗標的陣列。                                                                                        |
| [**glEdgeFlagPointer**](gledgeflagpointer.md)                                                                                                 | 定義邊緣旗標的陣列。                                                                                       |
| [**glEnable**](glenable.md)、 [ **glDisable**](gldisable.md)                                                                                   | 啟用或停用 OpenGL 功能。                                                                              |
| [**glEnableClientState**](glenableclientstate.md)、 [ **glDisableClientState**](gldisableclientstate.md)                                       | 分別啟用和停用陣列。                                                                            |
| [**glEvalCoord**](glevalcoord-functions.md) 函式                                                                                         | 評估已啟用一和二維的地圖。                                                                       |
| [**glEvalMesh**](glevalmesh-functions.md) 函式                                                                                           | 計算點或線條的一或二維方格。                                                            |
| [**glEvalPoint**](glevalpoint.md) 函式                                                                                                   | 產生和評估網格中的單一點。                                                                       |
| [**glFeedbackBuffer**](glfeedbackbuffer.md)                                                                                                   | 控制意見反應模式。                                                                                               |
| [**glFinish**](glfinish.md)                                                                                                                   | 封鎖直到所有 OpenGL 執行完成為止。                                                                        |
| [**glFlush**](glflush.md)                                                                                                                     | 在有限的時間內強制執行 OpenGL 函數。                                                                  |
| [**glFog**](glfog.md) 函式                                                                                                               | 指定霧化參數。                                                                                               |
| [**glFrontFace**](glfrontface.md)                                                                                                             | 定義前端和後置多邊形。                                                                              |
| [**glFrustum**](glfrustum.md)                                                                                                                 | 將目前的矩陣乘以透視圖矩陣。                                                                |
| [**glGenLists**](glgenlists.md)                                                                                                               | 產生一組連續的空白顯示清單。                                                                    |
| [**glGenTextures**](glgentextures.md)                                                                                                         | 產生材質名稱。                                                                                              |
| [**glGetBooleanv**](glgetbooleanv.md)                                                                                                         | 抓取選取的布林值參數值。                                                        |
| [**glGetClipPlane**](glgetclipplane.md)                                                                                                       | 抓取指定裁剪平面的係數。                                                           |
| [**glGetColorTableEXT**](glgetcolortableext.md)                                                                                               | 抓取目前目標材質調色板的色彩資料表資料。                                               |
| [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)、 [ **glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) | 從色彩表抓取調色板參數。                                                                       |
| [**glGetDoublev**](glgetdoublev.md)                                                                                                           | 抓取選取的雙精度浮點數參數值。                                                         |
| [**glGetError**](glgeterror.md)                                                                                                               | 捕獲錯誤資訊。                                                                                          |
| [**glGetFloatv**](glgetfloatv.md)                                                                                                             | 抓取選定 float 參數的值或值。                                                          |
| [**glGetIntegerv**](glgetintegerv.md)                                                                                                         | 抓取所選取 int 參數的值或值。                                                            |
| [**glGetLight**](glgetlight.md) 函式                                                                                                     | 取出燈光來源參數值。                                                                               |
| [**glGetMap**](glgetmap.md) 函式                                                                                                         | 取出評估工具參數。                                                                                        |
| [**glGetMaterial**](glgetmaterial.md) 函式                                                                                               | 取出材質參數。                                                                                         |
| [**glGetPixelMap**](glgetpixelmap.md) 函式                                                                                               | 取出指定的圖元映射。                                                                                     |
| [**glGetPointerv**](glgetpointerv.md)                                                                                                         | 捕獲頂點資料陣列的位址。                                                                         |
| [**glGetPolygonStipple**](glgetpolygonstipple.md)                                                                                             | 抓取多邊形 stipple 模式。                                                                                |
| [**glGetString**](glgetstring.md)                                                                                                             | 抓取描述目前 OpenGL 連接的字串。                                                          |
| [**glGetTexEnv**](glgettexenv.md) 函式                                                                                                   | 取出紋理環境參數。                                                                              |
| [**glGetTexGen**](glgettexgen.md) 函式                                                                                                   | 取出紋理座標產生參數。                                                                    |
| [**glGetTexImage**](glgetteximage.md)                                                                                                         | 捕獲材質影像。                                                                                            |
| [**glGetTexLevelParameter**](glgettexlevelparameter.md) 函式                                                                             | 取得特定詳細資料層級的材質參數值。                                                     |
| [**glGetTexParameter**](glgettexparameter.md) 函式                                                                                       | 取得材質參數值。                                                                                    |
| [**glHint**](glhint.md)                                                                                                                       | 指定執行特定的提示。                                                                              |
| [**glIndex**](glindex-functions.md) 函式                                                                                                 | 設定目前的色彩索引。                                                                                          |
| [**glIndexMask**](glindexmask.md)                                                                                                             | 控制在色彩索引緩衝區中寫入個別位的程式。                                                   |
| [**glIndexPointer**](glindexpointer.md)                                                                                                       | 定義色彩索引的陣列。                                                                                    |
| [**glInitNames**](glinitnames.md)                                                                                                             | 初始化名稱堆疊。                                                                                           |
| [**glInterleavedArrays**](glinterleavedarrays.md)                                                                                             | 同時指定並啟用大型匯總陣列中的數個交錯陣列。                          |
| [**glIsEnabled**](glisenabled.md)                                                                                                             | 測試是否啟用功能。                                                                                |
| [**glIsList**](glislist.md)                                                                                                                   | 顯示清單存在的測試。                                                                                     |
| [**glIsTexture**](glistexture.md)                                                                                                             | 判斷名稱是否對應至材質。                                                                   |
| [**glLight**](gllight-functions.md) 函式                                                                                                 | 設定燈光來源參數。                                                                                          |
| [**glLightModel**](gllightmodel-functions.md) 函式                                                                                       | 設定光源模型參數。                                                                                    |
| [**glLineStipple**](gllinestipple.md)                                                                                                         | 指定行 stipple 模式。                                                                                   |
| [**glLineWidth**](gllinewidth.md)                                                                                                             | 指定柵格線的寬度。                                                                              |
| [**glListBase**](gllistbase.md)                                                                                                               | 設定 **glCallLists** 的顯示清單基底。                                                                       |
| [**glLoadIdentity**](glloadidentity.md)                                                                                                       | 將目前的矩陣取代為識別矩陣。                                                                 |
| [**glLoadMatrix**](glloadmatrix.md) 函式                                                                                                 | 將目前的矩陣取代為任意矩陣。                                                                  |
| [**glLoadName**](glloadname.md)                                                                                                               | 將名稱載入至名稱堆疊。                                                                                     |
| [**glLogicOp**](gllogicop.md)                                                                                                                 | 指定色彩索引呈現的邏輯圖元運算。                                                        |
| [**glMap1**](glmap1.md) 函式                                                                                                             | 定義一維評估工具。                                                                                   |
| [**glMap2**](glmap2.md) 函式                                                                                                             | 定義二維評估工具。                                                                                   |
| [**glMapGrid**](glmapgrid-functions.md) 函式                                                                                             | 定義一或兩維網格。                                                                                |
| [**glMaterial**](glmaterial-functions.md) 函式                                                                                           | 指定光源模型的材質參數。                                                                   |
| [**glMatrixMode**](glmatrixmode.md)                                                                                                           | 指定目前矩陣的矩陣。                                                                         |
| [**glMultMatrix**](glmultmatrix.md) 函式                                                                                                 | 將目前的矩陣乘以任意矩陣。                                                                   |
| [**glNewList**](glnewlist.md)、 [ **glEndList**](glendlist.md)                                                                                 | 建立或取代顯示清單。                                                                                     |
| [**glNormal**](glnormal-functions.md) 函式                                                                                               | 設定目前的一般向量。                                                                                        |
| [**glNormalPointer**](glnormalpointer.md)                                                                                                     | 定義法線的陣列。                                                                                          |
| [**glOrtho**](glortho.md)                                                                                                                     | 將目前的矩陣與正向矩陣相乘。                                                              |
| [**glPassThrough**](glpassthrough.md)                                                                                                         | 將標記放在意見緩衝區中。                                                                               |
| [**glPixelMap**](glpixelmap.md) 函式                                                                                                     | 設定圖元傳輸對應。                                                                                           |
| [**glPixelStore**](glpixelstore-functions.md) 函式                                                                                       | 設定圖元儲存模式。                                                                                              |
| [**glPixelTransfer**](glpixeltransfer.md) 函式                                                                                           | 設定圖元傳輸模式。                                                                                             |
| [**glPixelZoom**](glpixelzoom.md)                                                                                                             | 指定圖元縮放因數。                                                                                     |
| [**glPointSize**](glpointsize.md)                                                                                                             | 指定柵格點的直徑。                                                                          |
| [**glPolygonMode**](glpolygonmode.md)                                                                                                         | 選取多邊形的點陣化模式。                                                                                 |
| [**glPolygonOffset**](glpolygonoffset.md)                                                                                                     | 設定 OpenGL 用來計算深度值的小數位數和單位數。                                                       |
| [**glPolygonStipple**](glpolygonstipple.md)                                                                                                   | 設定多邊形 stippling 模式。                                                                                   |
| [**glPrioritizeTextures**](glprioritizetextures.md)                                                                                           | 設定紋理的居住優先權。                                                                              |
| [**glPushAttrib**](glpushattrib.md)、 [ **glPopAttrib**](glpopattrib.md)                                                                       | 推送和 pop 屬性堆疊。                                                                                     |
| [**glPushClientAttrib**](glpushclientattrib.md)、 [ **glPopClientAttrib**](glpopclientattrib.md)                                               | 在用戶端屬性堆疊上儲存和還原用戶端狀態變數的群組。                                      |
| [**glPushMatrix**](glpushmatrix.md)、 [ **glPopMatrix**](glpopmatrix.md)                                                                       | 分別推送和 pop 目前的矩陣堆疊。                                                                  |
| [**glPushName**](glpushname.md)、 [ **glPopName**](glpopname.md)                                                                               | 分別推送和 pop 名稱堆疊。                                                                            |
| [**glRasterPos**](glrasterpos-functions.md) 函式                                                                                         | 指定圖元運算的點陣位置。                                                                     |
| [**glReadBuffer**](glreadbuffer.md)                                                                                                           | Slects 圖元的色彩緩衝區來源。                                                                              |
| [**glReadPixels**](glreadpixels.md)                                                                                                           | 從畫面格緩衝區讀取圖元區塊。                                                                         |
| [**glRect**](glrect-functions.md) 函式                                                                                                   | 繪製矩形。                                                                                                     |
| [**glRenderMode**](glrendermode.md)                                                                                                           | 設定點陣化模式。                                                                                          |
| [**glRotate**](glrotate.md) 函式                                                                                                         | 將目前的矩陣乘以旋轉矩陣。                                                                     |
| [**glScale**](glscale.md) 函式                                                                                                           | 將目前的矩陣乘以一般調整矩陣。                                                              |
| [**glScissor**](glscissor.md)                                                                                                                 | 定義剪式方塊。                                                                                              |
| [**glSelectBuffer**](glselectbuffer.md)                                                                                                       | 建立選取模式值的緩衝區。                                                                       |
| [**glShadeModel**](glshademodel.md)                                                                                                           | 選取平面或平滑陰影。                                                                                       |
| [**glStencilFunc**](glstencilfunc.md)                                                                                                         | 設定樣板測試的函數和參考值。                                                            |
| [**glStencilMask**](glstencilmask.md)                                                                                                         | 控制樣板平面中個別位的寫入。                                                        |
| [**glStencilOp**](glstencilop.md)                                                                                                             | 設定樣板測試動作。                                                                                        |
| [**glTexCoord**](gltexcoord-functions.md) 函式                                                                                           | 設定目前的材質座標。                                                                                  |
| [**glTexCoordPointer**](gltexcoordpointer.md)                                                                                                 | 定義材質座標的陣列。                                                                              |
| [**glTexEnv**](gltexenv-functions.md) 函式                                                                                               | 設定紋理環境參數。                                                                                   |
| [**glTexGen**](gltexgen-functions.md) 函式                                                                                               | 控制材質座標的產生。                                                                        |
| [**glTexImage1D**](glteximage1d.md)                                                                                                           | 指定一維材質影像。                                                                            |
| [**glTexImage2D**](glteximage2d.md)                                                                                                           | 指定二維紋理影像。                                                                            |
| [**glTexParameter**](gltexparameter-functions.md) 函式                                                                                   | 設定材質參數。                                                                                               |
| [**glTexSubImage1D**](gltexsubimage1d.md)                                                                                                     | 指定現有一維材質影像的一部分。 您無法使用此函式來定義新的材質。 |
| [**glTexSubImage2D**](gltexsubimage2d.md)                                                                                                     | 指定現有二維材質影像的一部分。 您無法使用此函式來定義新的材質。 |
| [**glTranslate**](gltranslate.md) 函式                                                                                                   | 將目前的矩陣乘以平移矩陣。                                                                  |
| [**glVertex**](glvertex-functions.md)                                                                                                         | 這些函數會指定頂點。                                                                                     |
| [**glVertexPointer**](glvertexpointer.md)                                                                                                     | 定義頂點資料的陣列。                                                                                      |
| [**glViewport**](glviewport.md)                                                                                                               | 設定 [區]。                                                                                                    |



 

 

 




