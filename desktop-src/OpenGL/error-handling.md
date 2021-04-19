---
title: " (OpenGL) 處理錯誤"
description: 當 OpenGL 偵測到錯誤時，它會記錄目前的錯誤碼。
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- 處理 OpenGL 時發生錯誤
- OpenGL 錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2005eb38f85e6e57f814a3ec61abf8b76fa4761
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106967704"
---
# <a name="error-handling-opengl"></a> (OpenGL) 處理錯誤

當 OpenGL 偵測到錯誤時，它會記錄目前的錯誤碼。 會忽略造成錯誤的函式，因此它不會影響 OpenGL 狀態或畫面格緩衝區內容。  (，如果記錄的錯誤是 \_ GL \_ 的記憶體不足，則函式 \_ 的結果為未定義。 ) 記錄之後，除非您呼叫 [**glGetError**](glgeterror.md) 查詢函式，而該函式會傳回目前的錯誤碼，否則不會清除目前的錯誤碼。

OpenGL 的執行可能會傳回多個目前的錯誤碼，每個錯誤碼都會保持設定直到查詢為止。 當 \_ \_ 您查詢所有目前的錯誤碼或沒有錯誤時，glGetError 函式會傳回 GL 無錯誤。 因此，如果您收到錯誤代碼，請呼叫 **glGetError** 直到 GL \_ 未 \_ 傳回錯誤，以確定您已探索到所有錯誤。 如需錯誤碼清單，請參閱 [OpenGL 錯誤碼](opengl-error-codes.md)。

您可以使用 [**gluErrorString**](gluerrorstring.md) x.glu 隊函式來取得對應至傳入之錯誤碼的描述性字串。 如需 **gluErrorString** 的詳細資訊，請參閱 [處理錯誤](handling-errors.md)。

> [!Note]  
> 如果偵測到錯誤，X.GLU 隊函數通常會傳回錯誤值。 此外，OpenGL 公用程式程式庫會定義錯誤碼 X.GLU 隊 \_ 無效 \_ 的列舉、X.glu 隊 \_ 無效 \_ 值和 x.glu 隊 \_ \_ 記憶體不足 \_ ，其意義與相關的 OpenGL 錯誤碼相同。

 

 

 




