---
title: C + + 中的範圍解析運算子
description: C + + 中的範圍解析運算子
ms.assetid: 908cf2b0-41d2-442d-aba8-82f3328c72c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb888fa9d56b6a84f8ecbc5efb2c235d1a38be03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840087"
---
# <a name="the-scope-resolution-operator-in-c"></a><span data-ttu-id="37cbf-103">C + + 中的範圍解析運算子</span><span class="sxs-lookup"><span data-stu-id="37cbf-103">The Scope Resolution Operator in C++</span></span>

<span data-ttu-id="37cbf-104">在 c + + 中使用兩個冒號 (：： ) 作為 *範圍解析* 運算子。</span><span class="sxs-lookup"><span data-stu-id="37cbf-104">Two colons (::) are used in C++ as a *scope resolution* operator.</span></span> <span data-ttu-id="37cbf-105">這個運算子可讓您使用相同名稱的變數來區分變數，讓您更自由地命名變數。</span><span class="sxs-lookup"><span data-stu-id="37cbf-105">This operator gives you more freedom in naming your variables by letting you distinguish between variables with the same name.</span></span> <span data-ttu-id="37cbf-106">例如， *myfile.txt：： read* 指的是物件 *Myfile.txt* 類別的 *Read* 方法，而不是 *YourFile：： read*，後者參考 *YourFile* 類別中的 *read* 方法。</span><span class="sxs-lookup"><span data-stu-id="37cbf-106">For example, *MyFile::Read* refers to the *Read* method of the *MyFile* class of objects, as opposed to *YourFile::Read*, which refers to a *Read* method in the *YourFile* class.</span></span>

 

 




