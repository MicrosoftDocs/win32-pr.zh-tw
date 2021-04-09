---
title: MIDL 列舉類型
description: MIDL 編譯器不會將列舉宣告轉譯成 \ 定義語句，因為它是由某些 DCE 編譯器所組成。 它會在產生的標頭檔中重現為 C 語言列舉宣告。
ms.assetid: 778d83e6-ec99-4781-87df-46da4cc86f5a
keywords:
- 資料類型 MIDL、列舉類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb28ef95c32549a2c373af292581d09923fce8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840320"
---
# <a name="midl-enumerated-types"></a><span data-ttu-id="91ae5-105">MIDL 列舉類型</span><span class="sxs-lookup"><span data-stu-id="91ae5-105">MIDL Enumerated Types</span></span>

<span data-ttu-id="91ae5-106">MIDL 編譯器不會將 [**列舉**](enum.md)宣告轉譯為 **\# define** 語句，因為它是由某些 DCE 編譯器所組成。</span><span class="sxs-lookup"><span data-stu-id="91ae5-106">The [**enum**](enum.md) declaration is not translated by the MIDL compiler into **\#define** statements, as it is by some DCE compilers.</span></span> <span data-ttu-id="91ae5-107">它會在產生的標頭檔中重現為 C 語言 **列舉** 宣告。</span><span class="sxs-lookup"><span data-stu-id="91ae5-107">It is reproduced as a C-language **enum** declaration in the generated header file.</span></span>

 

 




