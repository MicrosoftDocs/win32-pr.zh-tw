---
title: WinRM 外掛程式 API 結構
description: WinRM 外掛程式 API 結構
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685bcf87ef8c634db367db62b3ec1472b50e3b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301519"
---
# <a name="winrm-plug-in-api-structures"></a><span data-ttu-id="ded48-103">WinRM 外掛程式 API 結構</span><span class="sxs-lookup"><span data-stu-id="ded48-103">WinRM Plug-in API Structures</span></span>

<span data-ttu-id="ded48-104">下表概要說明 Windows 遠端管理 (WinRM) 外掛程式應用程式開發介面 (API) 中的結構。</span><span class="sxs-lookup"><span data-stu-id="ded48-104">The following table provides an overview of the structures in the Windows Remote Management (WinRM) plug-in application programming interface (API).</span></span>



| <span data-ttu-id="ded48-105">結構</span><span class="sxs-lookup"><span data-stu-id="ded48-105">Structure</span></span>                                                        | <span data-ttu-id="ded48-106">Description</span><span class="sxs-lookup"><span data-stu-id="ded48-106">Description</span></span>                                                                              |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ded48-107">**WSMAN \_ 授權 \_ 配額**</span><span class="sxs-lookup"><span data-stu-id="ded48-107">**WSMAN\_AUTHZ\_QUOTA**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_authz_quota)                 | <span data-ttu-id="ded48-108">以每個使用者為基礎來定義配額資訊。</span><span class="sxs-lookup"><span data-stu-id="ded48-108">Defines quota information on a per-user basis.</span></span>                                           |
| [<span data-ttu-id="ded48-109">**WSMAN \_ 憑證 \_ 詳細資料**</span><span class="sxs-lookup"><span data-stu-id="ded48-109">**WSMAN\_CERTIFICATE\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_certificate_details) | <span data-ttu-id="ded48-110">代表用戶端憑證中的欄位。</span><span class="sxs-lookup"><span data-stu-id="ded48-110">Represents the fields within the client certificate.</span></span>                                     |
| [<span data-ttu-id="ded48-111">**WSMAN \_ 命令 \_ ARG \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="ded48-111">**WSMAN\_COMMAND\_ARG\_SET**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_command_arg_set)        | <span data-ttu-id="ded48-112">表示傳入命令列的引數集。</span><span class="sxs-lookup"><span data-stu-id="ded48-112">Represents the set of arguments that are passed in to the command line.</span></span>                  |
| [<span data-ttu-id="ded48-113">**WSMAN \_ 篩選**</span><span class="sxs-lookup"><span data-stu-id="ded48-113">**WSMAN\_FILTER**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_filter)                            | <span data-ttu-id="ded48-114">定義用於操作的篩選。</span><span class="sxs-lookup"><span data-stu-id="ded48-114">Defines the filtering used for an operation.</span></span>                                             |
| [<span data-ttu-id="ded48-115">**WSMAN \_ 片段**</span><span class="sxs-lookup"><span data-stu-id="ded48-115">**WSMAN\_FRAGMENT**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_fragment)                        | <span data-ttu-id="ded48-116">定義作業的片段資訊。</span><span class="sxs-lookup"><span data-stu-id="ded48-116">Defines the fragment information for an operation.</span></span>                                       |
| [<span data-ttu-id="ded48-117">**WSMAN \_ 操作 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="ded48-117">**WSMAN\_OPERATION\_INFO**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_operation_info)           | <span data-ttu-id="ded48-118">表示外掛程式必須執行要求的特定資源端點。</span><span class="sxs-lookup"><span data-stu-id="ded48-118">Represents a specific resource end-point for which the plug-in must perform the request.</span></span> |
| [<span data-ttu-id="ded48-119">**WSMAN \_ 外掛程式 \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="ded48-119">**WSMAN\_PLUGIN\_REQUEST**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)           | <span data-ttu-id="ded48-120">包含要求的相關資訊，並傳遞至每個外掛程式作業。</span><span class="sxs-lookup"><span data-stu-id="ded48-120">Contains information about the request and is passed into every plug-in operation.</span></span>       |
| [<span data-ttu-id="ded48-121">**WSMAN \_ 寄件者 \_ 詳細資料**</span><span class="sxs-lookup"><span data-stu-id="ded48-121">**WSMAN\_SENDER\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_sender_details)           | <span data-ttu-id="ded48-122">指定每個輸入要求的用戶端詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ded48-122">Specifies client details for every inbound request.</span></span>                                      |



 

 

 




