---
title: ADSI 擴充功能類型程式庫
description: 延伸模組的類型程式庫不會合並。
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- ADSI 擴充功能類型程式庫 ADSI
- 延伸模組 ADSI、延伸型別程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7efc89bd491d5ee244c5a2a64dd7df4c84b61ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507041"
---
# <a name="adsi-extension-type-libraries"></a><span data-ttu-id="f7e55-105">ADSI 擴充功能類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f7e55-105">ADSI Extension Type Libraries</span></span>

<span data-ttu-id="f7e55-106">延伸模組的類型程式庫不會合並。</span><span class="sxs-lookup"><span data-stu-id="f7e55-106">The type libraries for extensions are not merged.</span></span> <span data-ttu-id="f7e55-107">ADSI 用戶端必須特別包含每個延伸模組的類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="f7e55-107">ADSI clients must specifically include the type library for each extension.</span></span> <span data-ttu-id="f7e55-108">Visual Basic 需要類型程式庫才能啟用早期繫結。</span><span class="sxs-lookup"><span data-stu-id="f7e55-108">The type library is required for Visual Basic to enable early bindings.</span></span> <span data-ttu-id="f7e55-109">以 C/c + + 撰寫的用戶端應用程式可以在延伸模組標頭檔中定義的延伸模組介面上呼叫 **QueryInterface** 方法。</span><span class="sxs-lookup"><span data-stu-id="f7e55-109">Client applications written in C/C++ can call the **QueryInterface** method on the extension interfaces defined in the extension header files.</span></span>

 

 




