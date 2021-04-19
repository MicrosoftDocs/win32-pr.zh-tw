---
description: SWbemPrivilege 物件的 DisplayName 屬性是顯示 SWbemPrivilege 物件描述的字串。
ms.assetid: 9ed91a6a-e513-4a72-b8a9-3180e42b811f
ms.tgt_platform: multiple
title: 'SWbemPrivilege： DisplayName 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.DisplayName
- ISWbemPrivilege.DisplayName
- ISWbemPrivilege.get_DisplayName
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bb45bdce52b1930f1893f7716d573033627e0cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980763"
---
# <a name="swbemprivilegedisplayname-property"></a><span data-ttu-id="2eeb3-103">SWbemPrivilege DisplayName 屬性</span><span class="sxs-lookup"><span data-stu-id="2eeb3-103">SWbemPrivilege.DisplayName property</span></span>

<span data-ttu-id="2eeb3-104">[**SWbemPrivilege**](swbemprivilege.md)物件的 **DisplayName** 屬性是顯示 **SWbemPrivilege** 物件描述的字串。</span><span class="sxs-lookup"><span data-stu-id="2eeb3-104">The **DisplayName** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a string that displays a description of an **SWbemPrivilege** object.</span></span> <span data-ttu-id="2eeb3-105">例如，控制使用者是否可以執行物件的 shutdown 方法的許可權，就會在 **SWbemPrivilege DisplayName** 屬性中「關閉系統」字串。</span><span class="sxs-lookup"><span data-stu-id="2eeb3-105">For example, the privilege that controls whether a user can execute the shutdown method of an object has the "Shut down the system" string in the **SWbemPrivilege.DisplayName** property.</span></span> <span data-ttu-id="2eeb3-106">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="2eeb3-106">This property is read-only.</span></span>

<span data-ttu-id="2eeb3-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="2eeb3-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="2eeb3-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2eeb3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eeb3-109">語法</span><span class="sxs-lookup"><span data-stu-id="2eeb3-109">Syntax</span></span>


```VB
SWbemPrivilege.DisplayName As 
```



## <a name="property-value"></a><span data-ttu-id="2eeb3-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="2eeb3-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="2eeb3-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="2eeb3-111">Requirements</span></span>



| <span data-ttu-id="2eeb3-112">需求</span><span class="sxs-lookup"><span data-stu-id="2eeb3-112">Requirement</span></span> | <span data-ttu-id="2eeb3-113">值</span><span class="sxs-lookup"><span data-stu-id="2eeb3-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2eeb3-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2eeb3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2eeb3-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2eeb3-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2eeb3-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2eeb3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2eeb3-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2eeb3-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2eeb3-118">標頭</span><span class="sxs-lookup"><span data-stu-id="2eeb3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eeb3-119"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="2eeb3-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2eeb3-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2eeb3-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="2eeb3-121"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2eeb3-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2eeb3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2eeb3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eeb3-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2eeb3-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2eeb3-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="2eeb3-124">CLSID</span></span><br/>                    | <span data-ttu-id="2eeb3-125">CLSID \_ SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="2eeb3-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="2eeb3-126">IID</span><span class="sxs-lookup"><span data-stu-id="2eeb3-126">IID</span></span><br/>                      | <span data-ttu-id="2eeb3-127">IID \_ ISWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="2eeb3-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




