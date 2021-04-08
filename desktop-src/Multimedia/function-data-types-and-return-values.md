---
title: 函數資料類型和傳回值
description: 函數資料類型和傳回值
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28bd7484c3d968e92da5fcd19ee738da1ee811a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932134"
---
# <a name="function-data-types-and-return-values"></a>函數資料類型和傳回值

AVIFile 函式和宏使用以 OLE 技術所執行的檔案和資料流程處理常式。 OLE 函數的標準資料型別為 **STDAPI**，函式會傳回 **HRESULT** 值 (零表示成功，否則會傳回錯誤) 。 如果函式傳回的值不是 **HRESULT**，則函式原型的型別會有稍微不同的語法，將傳回值型別內嵌在 "STDAPI" 後面的括弧中 \_ 。 例如，傳回 **LONG** 資料值的函數在 prototype 語句中使用 **STDAPI \_ (LONG)** 。

 

 




