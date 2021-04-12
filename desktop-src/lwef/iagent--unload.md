---
title: IAgent UnLoad
description: IAgent UnLoad
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc30d6c4c06c1d292a26a2f503477dcca651dd18
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315049"
---
# <a name="iagentunload"></a><span data-ttu-id="b3b66-103">IAgent：： UnLoad</span><span class="sxs-lookup"><span data-stu-id="b3b66-103">IAgent::UnLoad</span></span>

<span data-ttu-id="b3b66-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b3b66-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

<span data-ttu-id="b3b66-105">從 [**字元**](/windows/desktop/lwef/the-characters-object) 集合中卸載指定字元的字元資料。</span><span class="sxs-lookup"><span data-stu-id="b3b66-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="b3b66-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="b3b66-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b3b66-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="b3b66-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="b3b66-108">字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3b66-108">The character's ID.</span></span>

</dd> </dl>

<span data-ttu-id="b3b66-109">當您不再需要字元時，請使用這個方法來釋出用來儲存字元相關資訊的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b3b66-109">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="b3b66-110">如果您再次存取此字元，請使用 [**Load**](load-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b3b66-110">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3b66-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3b66-111">See Also</span></span>

[<span data-ttu-id="b3b66-112">**IAgent：： Load**</span><span class="sxs-lookup"><span data-stu-id="b3b66-112">**IAgent::Load**</span></span>](iagent--load.md)


 

 