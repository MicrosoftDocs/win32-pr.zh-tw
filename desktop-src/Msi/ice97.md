---
description: ICE97 會確認兩個元件沒有將共用元件隔離到相同的目錄。
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29575d533e945cef922110315cd3300f56fe62ae61b34c92de7175916e6657ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315238"
---
# <a name="ice97"></a>ICE97

ICE97 會確認兩個元件沒有將共用元件隔離到相同的目錄。

## <a name="result"></a>結果

ICE97 會張貼下列警告。



| ICE97 警告                                                                                                                                                                    | 描述                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| 此元件 \[ 1 \] 會將共用的元件安裝到與 \[ 另一個相同的目錄 2 \] 中，如果已選取 (或更多) 元件進行安裝，則會中斷元件規則。 | 兩個元件不得將共用元件隔離到相同的目錄。 |



 

例如，Component1 和 Component2 （共用的 ComponentShared）會安裝在相同的目錄中。 兩者都會將 ComponentShared 指定為隔離的元件。 由於隔離的原因，ComponentShared 中的檔案會複製兩次到 \_ Component1 和 Component2 的目錄參考中。 元件的複本上現在有一個參考計數。 這違反了安裝程式元件規則。 如果卸載 Component1，則會移除隔離的元件檔案，而 Component2 會中斷。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



