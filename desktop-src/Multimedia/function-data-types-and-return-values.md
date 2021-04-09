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
# <a name="function-data-types-and-return-values"></a><span data-ttu-id="5ff7b-103">函數資料類型和傳回值</span><span class="sxs-lookup"><span data-stu-id="5ff7b-103">Function Data Types and Return Values</span></span>

<span data-ttu-id="5ff7b-104">AVIFile 函式和宏使用以 OLE 技術所執行的檔案和資料流程處理常式。</span><span class="sxs-lookup"><span data-stu-id="5ff7b-104">The AVIFile functions and macros use file and stream handlers implemented with OLE technology.</span></span> <span data-ttu-id="5ff7b-105">OLE 函數的標準資料型別為 **STDAPI**，函式會傳回 **HRESULT** 值 (零表示成功，否則會傳回錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="5ff7b-105">The standard data type of an OLE function is **STDAPI**, and the function returns an **HRESULT** value (zero for success or an error otherwise).</span></span> <span data-ttu-id="5ff7b-106">如果函式傳回的值不是 **HRESULT**，則函式原型的型別會有稍微不同的語法，將傳回值型別內嵌在 "STDAPI" 後面的括弧中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5ff7b-106">If a function returns a value other than an **HRESULT**, the type of the function's prototype has a slightly different syntax that embeds the return value type in parentheses following "STDAPI\_".</span></span> <span data-ttu-id="5ff7b-107">例如，傳回 **LONG** 資料值的函數在 prototype 語句中使用 **STDAPI \_ (LONG)** 。</span><span class="sxs-lookup"><span data-stu-id="5ff7b-107">For example, a function that returns a **LONG** data value uses **STDAPI\_(LONG)** in the prototype statement.</span></span>

 

 




