---
description: SWbemPrivilege 物件的 IsEnabled 屬性是用來啟用或停用此許可權的布林值。 如需啟用特定許可權之結果的詳細資訊，請參閱以特殊許可權執行。
ms.assetid: 282c8865-ba0d-4e82-be05-96a940036590
ms.tgt_platform: multiple
title: 'SWbemPrivilege. IsEnabled 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.IsEnabled
- ISWbemPrivilege.IsEnabled
- ISWbemPrivilege.get_IsEnabled
- ISWbemPrivilege.put_IsEnabled
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ec27b2344c42dca56ac629144f6edc402f81ea4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982337"
---
# <a name="swbemprivilegeisenabled-property"></a><span data-ttu-id="35bb9-104">SWbemPrivilege. IsEnabled 屬性</span><span class="sxs-lookup"><span data-stu-id="35bb9-104">SWbemPrivilege.IsEnabled property</span></span>

<span data-ttu-id="35bb9-105">[**SWbemPrivilege**](swbemprivilege.md)物件的 **IsEnabled** 屬性是用來啟用或停用此許可權的布林值。</span><span class="sxs-lookup"><span data-stu-id="35bb9-105">The **IsEnabled** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a Boolean value that you use to enable or disable this privilege.</span></span> <span data-ttu-id="35bb9-106">如需啟用特定許可權之結果的詳細資訊，請參閱 [**以特殊許可權**](swbemsecurity-privileges.md)執行。</span><span class="sxs-lookup"><span data-stu-id="35bb9-106">For more information about the consequences of enabling specific privileges, see [**Running with Special Privileges**](swbemsecurity-privileges.md).</span></span>

<span data-ttu-id="35bb9-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="35bb9-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="35bb9-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="35bb9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="35bb9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="35bb9-109">Syntax</span></span>


```VB
SWbemPrivilege.IsEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="35bb9-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="35bb9-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="35bb9-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="35bb9-111">Requirements</span></span>



| <span data-ttu-id="35bb9-112">需求</span><span class="sxs-lookup"><span data-stu-id="35bb9-112">Requirement</span></span> | <span data-ttu-id="35bb9-113">值</span><span class="sxs-lookup"><span data-stu-id="35bb9-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35bb9-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35bb9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="35bb9-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35bb9-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35bb9-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35bb9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="35bb9-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35bb9-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35bb9-118">標頭</span><span class="sxs-lookup"><span data-stu-id="35bb9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="35bb9-119"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="35bb9-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="35bb9-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="35bb9-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="35bb9-121"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35bb9-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35bb9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="35bb9-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35bb9-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35bb9-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="35bb9-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="35bb9-124">CLSID</span></span><br/>                    | <span data-ttu-id="35bb9-125">CLSID \_ SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="35bb9-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="35bb9-126">IID</span><span class="sxs-lookup"><span data-stu-id="35bb9-126">IID</span></span><br/>                      | <span data-ttu-id="35bb9-127">IID \_ ISWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="35bb9-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




