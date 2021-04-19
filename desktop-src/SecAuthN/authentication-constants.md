---
description: 列出用於 Microsoft 驗證 Api 的常數。
ms.assetid: 3e5b7fd8-01bf-4090-b68f-006b7e2228a9
title: '驗證常數 (驗證) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d671f356f11ccaf1f5aece1dc1168d3106d578c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985033"
---
# <a name="authentication-constants-authentication"></a><span data-ttu-id="62455-103">驗證常數 (驗證) </span><span class="sxs-lookup"><span data-stu-id="62455-103">Authentication Constants (Authentication)</span></span>

## <a name="credentials-management-constants"></a><span data-ttu-id="62455-104">認證管理常數</span><span class="sxs-lookup"><span data-stu-id="62455-104">Credentials Management Constants</span></span>

<span data-ttu-id="62455-105">認證管理會使用下列常數來指定字串大小上限。</span><span class="sxs-lookup"><span data-stu-id="62455-105">Credentials Management uses the following constants to specify maximum string sizes.</span></span>



| <span data-ttu-id="62455-106">常數</span><span class="sxs-lookup"><span data-stu-id="62455-106">Constant</span></span>                                        | <span data-ttu-id="62455-107">描述</span><span class="sxs-lookup"><span data-stu-id="62455-107">Description</span></span>                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62455-108">CREDUI \_ \_ 訊息 \_ 長度上限</span><span class="sxs-lookup"><span data-stu-id="62455-108">CREDUI\_MAX\_MESSAGE\_LENGTH</span></span><br/>         | <span data-ttu-id="62455-109">[**CREDUI \_ 資訊**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa)結構的 **pszMessageText** 成員最大字元數。</span><span class="sxs-lookup"><span data-stu-id="62455-109">Maximum number of characters for the **pszMessageText** member of a [**CREDUI\_INFO**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) structure.</span></span><br/> |
| <span data-ttu-id="62455-110">CREDUI \_ 最大 \_ 標題 \_ 長度</span><span class="sxs-lookup"><span data-stu-id="62455-110">CREDUI\_MAX\_CAPTION\_LENGTH</span></span><br/>         | <span data-ttu-id="62455-111">[**CREDUI \_ 資訊**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa)結構的 **pszCaptionText** 成員最大字元數。</span><span class="sxs-lookup"><span data-stu-id="62455-111">Maximum number of characters for the **pszCaptionText** member of a [**CREDUI\_INFO**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) structure.</span></span><br/> |
| <span data-ttu-id="62455-112">CREDUI \_ 最大 \_ 泛型 \_ 目標 \_ 長度</span><span class="sxs-lookup"><span data-stu-id="62455-112">CREDUI\_MAX\_GENERIC\_TARGET\_LENGTH</span></span><br/> | <span data-ttu-id="62455-113">字串中指定目標名稱的最大字元數。</span><span class="sxs-lookup"><span data-stu-id="62455-113">Maximum number of characters in a string that specifies a target name.</span></span><br/>                                             |
| <span data-ttu-id="62455-114">CREDUI \_ 最大 \_ 網域 \_ 目標 \_ 長度</span><span class="sxs-lookup"><span data-stu-id="62455-114">CREDUI\_MAX\_DOMAIN\_TARGET\_LENGTH</span></span><br/>  | <span data-ttu-id="62455-115">字串中指定功能變數名稱的最大字元數。</span><span class="sxs-lookup"><span data-stu-id="62455-115">Maximum number of characters in a string that specifies a domain name.</span></span><br/>                                             |
| <span data-ttu-id="62455-116">CREDUI \_ 使用者 \_ 名稱 \_ 長度上限</span><span class="sxs-lookup"><span data-stu-id="62455-116">CREDUI\_MAX\_USERNAME\_LENGTH</span></span><br/>        | <span data-ttu-id="62455-117">字串中指定使用者帳戶名稱的最大字元數。</span><span class="sxs-lookup"><span data-stu-id="62455-117">Maximum number of characters in a string that specifies a user account name.</span></span><br/>                                       |
| <span data-ttu-id="62455-118">CREDUI \_ \_ 密碼 \_ 長度上限</span><span class="sxs-lookup"><span data-stu-id="62455-118">CREDUI\_MAX\_PASSWORD\_LENGTH</span></span><br/>        | <span data-ttu-id="62455-119">字串中指定密碼的最大字元數。</span><span class="sxs-lookup"><span data-stu-id="62455-119">Maximum number of characters in a string that specifies a password.</span></span><br/>                                                |



 

## <a name="gina-defined-values"></a><span data-ttu-id="62455-120">Gina 定義的值</span><span class="sxs-lookup"><span data-stu-id="62455-120">Gina Defined Values</span></span>

<span data-ttu-id="62455-121">[*GINA*](/windows/desktop/SecGloss/g-gly) 介面函式和 [*Winlogon*](/windows/desktop/SecGloss/w-gly) 支援函數會使用下列定義的值。</span><span class="sxs-lookup"><span data-stu-id="62455-121">[*GINA*](/windows/desktop/SecGloss/g-gly) interface functions and [*Winlogon*](/windows/desktop/SecGloss/w-gly) support functions use the following defined values.</span></span>

> [!Note]  
> <span data-ttu-id="62455-122">在 Windows Vista 中會忽略 GINA Dll。</span><span class="sxs-lookup"><span data-stu-id="62455-122">GINA DLLs are ignored in Windows Vista.</span></span>

 



| <span data-ttu-id="62455-123">值</span><span class="sxs-lookup"><span data-stu-id="62455-123">Value</span></span>                                                              | <span data-ttu-id="62455-124">描述</span><span class="sxs-lookup"><span data-stu-id="62455-124">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62455-125">**WLX \_ LOGON \_ 選項 \_ XXX**</span><span class="sxs-lookup"><span data-stu-id="62455-125">**WLX\_LOGON\_OPTION\_XXX**</span></span>](wlx-logon-option-xxx.md)<br/> | <span data-ttu-id="62455-126">包含預先定義的登入選項。</span><span class="sxs-lookup"><span data-stu-id="62455-126">Contains predefined logon options.</span></span> <span data-ttu-id="62455-127">[**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)的 *>dwoptions* 參數會使用它。</span><span class="sxs-lookup"><span data-stu-id="62455-127">It is used by the *dwOptions* parameter of [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span></span><br/> |
| [<span data-ttu-id="62455-128">**WLX \_ SAS \_ 類型 \_ XXX**</span><span class="sxs-lookup"><span data-stu-id="62455-128">**WLX\_SAS\_TYPE\_XXX**</span></span>](wlx-sas-type-xxx.md)<br/>         | <span data-ttu-id="62455-129">定義特定的 SAS 類型。</span><span class="sxs-lookup"><span data-stu-id="62455-129">Defines a specific SAS type.</span></span><br/>                                                                                              |



 

 

