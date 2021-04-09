---
title: SAM RPC 通訊協定的遠端呼叫僅限於本機系統管理員
description: SAM RPC 通訊協定受到限制。 這表示只有本機系統管理員群組的成員可以對此通訊協定中的方法進行遠端呼叫。 Active Directory 網域控制站的行為不會受到影響。
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 669c20503551b0a380372524b898559dff472f2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092321"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a><span data-ttu-id="dcfe3-105">SAM RPC 通訊協定的遠端呼叫僅限於本機系統管理員</span><span class="sxs-lookup"><span data-stu-id="dcfe3-105">Remote calls to the SAM RPC protocol are restricted to only local administrators</span></span>

<span data-ttu-id="dcfe3-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="dcfe3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dcfe3-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="dcfe3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dcfe3-108">SAM RPC 通訊協定受到限制。</span><span class="sxs-lookup"><span data-stu-id="dcfe3-108">The SAM RPC protocol is being restricted.</span></span> <span data-ttu-id="dcfe3-109">這表示只有本機系統管理員群組的成員可以對此通訊協定中的方法進行遠端呼叫。</span><span class="sxs-lookup"><span data-stu-id="dcfe3-109">This means that only members of the local Administrator group can make remote calls against methods in this protocol.</span></span> <span data-ttu-id="dcfe3-110">Active Directory 網域控制站的行為不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="dcfe3-110">Active Directory domain controller behavior is unaffected.</span></span>

## <a name="mitigations"></a><span data-ttu-id="dcfe3-111">風險降低</span><span class="sxs-lookup"><span data-stu-id="dcfe3-111">Mitigations</span></span>

<span data-ttu-id="dcfe3-112">確定已將正確的使用者設定為電腦上的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="dcfe3-112">Ensure that the right users are set as administrators on the PC.</span></span> <span data-ttu-id="dcfe3-113">用於存取檢查的 ACL 可透過群組原則來設定。</span><span class="sxs-lookup"><span data-stu-id="dcfe3-113">The ACL used for the access check is configurable via group policy.</span></span>

 

 




