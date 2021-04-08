---
title: IAgent 取消註冊
description: IAgent 取消註冊
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842280"
---
# <a name="iagentunregister"></a><span data-ttu-id="539a0-103">IAgent：：取消註冊</span><span class="sxs-lookup"><span data-stu-id="539a0-103">IAgent::Unregister</span></span>

<span data-ttu-id="539a0-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="539a0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

<span data-ttu-id="539a0-105">從 [**字元**](/windows/desktop/lwef/the-characters-object) 集合中卸載指定字元的字元資料。</span><span class="sxs-lookup"><span data-stu-id="539a0-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="539a0-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="539a0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="539a0-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*</span><span class="sxs-lookup"><span data-stu-id="539a0-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="539a0-108">通知接收識別碼。</span><span class="sxs-lookup"><span data-stu-id="539a0-108">The notification sink ID.</span></span>

</dd> </dl>

<span data-ttu-id="539a0-109">當您不再需要 Microsoft 代理程式服務時，例如當您的應用程式關閉時，請使用此方法。</span><span class="sxs-lookup"><span data-stu-id="539a0-109">Use this method when you no longer need Microsoft Agent services, such as when your application shuts down.</span></span>

## <a name="see-also"></a><span data-ttu-id="539a0-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="539a0-110">See Also</span></span>

[<span data-ttu-id="539a0-111">**IAgent：： Register**</span><span class="sxs-lookup"><span data-stu-id="539a0-111">**IAgent::Register**</span></span>](iagent--register.md)


 

 