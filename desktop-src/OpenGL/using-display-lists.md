---
title: 使用顯示清單
description: 使用顯示清單
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL、顯示清單
- 顯示清單 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322721868f3bf994382a7604aa2cb76802f268aec7a1298aaa14e3066d5f6cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932798"
---
# <a name="using-display-lists"></a>使用顯示清單

顯示清單是已儲存以供後續執行的 OpenGL 函數群組。 [**GlNewList**](glnewlist.md)函式會開始建立顯示清單，而 [**glEndList**](glendlist.md)會將它結束。 除了少數例外，在 **glNewList** 和 **glEndList** 之間呼叫的 OpenGL 函式會附加至顯示清單。  (請參閱 **glNewList** ，以取得您無法在顯示清單中儲存及執行的函式清單。 ) 若要觸發清單或清單集的執行，請使用 [**glCallList**](glcalllist.md) 或 [**glCallLists**](glcalllists.md) ，並提供特定清單或清單的識別編號。 您可以使用 [**glGenLists**](glgenlists.md)、 [**glListBase**](gllistbase.md)和 [**glIsList**](glislist.md)來管理用來識別顯示清單的索引。 若要刪除一組顯示清單，請使用 [**glDeleteLists**](gldeletelists.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[顯示清單參考](display-lists-reference.md)
</dt> </dl>

 

 




