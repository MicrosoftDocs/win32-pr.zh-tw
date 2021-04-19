---
description: CSingleFilterTerminal 是另一個適用于靜態和動態終端機的終端基類。
ms.assetid: d423438f-1324-4df3-beaa-fdef325fac2e
title: CSingleFilterTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 111a20e59ab0c549e994695610364c451c07fd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987676"
---
# <a name="csinglefilterterminal"></a><span data-ttu-id="3bb32-103">CSingleFilterTerminal</span><span class="sxs-lookup"><span data-stu-id="3bb32-103">CSingleFilterTerminal</span></span>

<span data-ttu-id="3bb32-104">**CSingleFilterTerminal** 是另一個適用于靜態和動態終端機的終端基類。</span><span class="sxs-lookup"><span data-stu-id="3bb32-104">**CSingleFilterTerminal** is an additional terminal base class applicable to both static and dynamic terminals.</span></span> <span data-ttu-id="3bb32-105">它衍生自 [**CBaseTerminal**](cbaseterminal.md) ，並假設終端機具有單一的 DirectShow 篩選器，讓執行更為明確。</span><span class="sxs-lookup"><span data-stu-id="3bb32-105">It is derived from [**CBaseTerminal**](cbaseterminal.md) and makes the implementation more specific by assuming that the terminal has a single DirectShow filter.</span></span> <span data-ttu-id="3bb32-106">當符合這項條件時，從 **CSingleFilterTerminal** 衍生終端機會比從 **CBaseTerminal** 衍生的簡單得多。</span><span class="sxs-lookup"><span data-stu-id="3bb32-106">When this condition is met, deriving a terminal implementation from **CSingleFilterTerminal** is much easier than deriving from **CBaseTerminal**.</span></span>

<span data-ttu-id="3bb32-107">定義于 MSPterm 中。</span><span class="sxs-lookup"><span data-stu-id="3bb32-107">Defined in MSPterm.h.</span></span>

 

 



