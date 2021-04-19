---
description: WMI 目前不支援 WMI 上的 managed 程式碼，但在 MI 上則支援。
ms.assetid: ED6EF216-7FF7-45F2-9FDD-3A73D5F65F9B
ms.tgt_platform: multiple
title: 建立受控 WMI 用戶端
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb1339347c4e15cd29ebf4d4e98e5a8b61a24e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980784"
---
# <a name="creating-a-managed-wmi-client"></a><span data-ttu-id="1a88e-103">建立受控 WMI 用戶端</span><span class="sxs-lookup"><span data-stu-id="1a88e-103">Creating a Managed WMI Client</span></span>

<span data-ttu-id="1a88e-104">目前的 WMI 版本包含管理命名空間，此命名空間會公開與 WMI 互動的許多 API。</span><span class="sxs-lookup"><span data-stu-id="1a88e-104">The current release of WMI does contain the System.Management namespace, which exposes a number of API's that interact with WMI.</span></span> <span data-ttu-id="1a88e-105">但是，不建議使用此命名空間。</span><span class="sxs-lookup"><span data-stu-id="1a88e-105">However, it is not recommended that you use this namespace.</span></span>

<span data-ttu-id="1a88e-106">如果您想要建立受控 WMI 用戶端，建議您使用 Windows 管理基礎結構 (MI) 。</span><span class="sxs-lookup"><span data-stu-id="1a88e-106">If you wish to create a managed WMI client, it is recommended that you use the Windows Management Infrastructure (MI).</span></span> <span data-ttu-id="1a88e-107">MI 是新一代的 WMI 版本，包含對 managed 程式碼的完整支援。</span><span class="sxs-lookup"><span data-stu-id="1a88e-107">MI is the next-generation version of WMI, and contains full support for managed code.</span></span> <span data-ttu-id="1a88e-108">如需詳細資訊，請參閱 [如何執行受管理的 MI 用戶端](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client)。</span><span class="sxs-lookup"><span data-stu-id="1a88e-108">For more information, see [How to Implement a Managed MI Client](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).</span></span>

 

 
