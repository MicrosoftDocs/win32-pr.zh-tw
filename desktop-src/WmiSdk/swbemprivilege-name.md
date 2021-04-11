---
description: SWbemPrivilege 物件的 Name 屬性是可唯一描述許可權的字串。
ms.assetid: cc1cdde7-20ad-4ff7-ad49-43eb46c15df9
ms.tgt_platform: multiple
title: 'SWbemPrivilege.Name 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.Name
- ISWbemPrivilege.Name
- ISWbemPrivilege.get_Name
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b83ccc7c2757c5d5a0746efd4434db3d108b6992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195037"
---
# <a name="swbemprivilegename-property"></a><span data-ttu-id="df455-103">SWbemPrivilege.Name 屬性</span><span class="sxs-lookup"><span data-stu-id="df455-103">SWbemPrivilege.Name property</span></span>

<span data-ttu-id="df455-104">[**SWbemPrivilege**](swbemprivilege.md)物件的 **Name** 屬性是可唯一描述許可權的字串。</span><span class="sxs-lookup"><span data-stu-id="df455-104">The **Name** property of an [**SWbemPrivilege**](swbemprivilege.md) object is a string that uniquely describes a privilege.</span></span> <span data-ttu-id="df455-105">例如，控制使用者是否可以執行物件的 shutdown 方法的許可權，會在 **SWbemPrivilege.Name** 屬性中包含 "SeShutdownPrivilege" 字串。</span><span class="sxs-lookup"><span data-stu-id="df455-105">For example, the privilege that controls whether a user can execute the shutdown method of an object has the "SeShutdownPrivilege" string in the **SWbemPrivilege.Name** property.</span></span> <span data-ttu-id="df455-106">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="df455-106">This property is read-only.</span></span>

<span data-ttu-id="df455-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="df455-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="df455-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="df455-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="df455-109">語法</span><span class="sxs-lookup"><span data-stu-id="df455-109">Syntax</span></span>


```VB
SWbemPrivilege.Name As 
```



## <a name="property-value"></a><span data-ttu-id="df455-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="df455-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="df455-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="df455-111">Requirements</span></span>



| <span data-ttu-id="df455-112">需求</span><span class="sxs-lookup"><span data-stu-id="df455-112">Requirement</span></span> | <span data-ttu-id="df455-113">值</span><span class="sxs-lookup"><span data-stu-id="df455-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df455-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df455-114">Minimum supported client</span></span><br/> | <span data-ttu-id="df455-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df455-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df455-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df455-116">Minimum supported server</span></span><br/> | <span data-ttu-id="df455-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df455-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df455-118">標頭</span><span class="sxs-lookup"><span data-stu-id="df455-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="df455-119"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="df455-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="df455-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="df455-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="df455-121"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="df455-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="df455-122">DLL</span><span class="sxs-lookup"><span data-stu-id="df455-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df455-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df455-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="df455-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="df455-124">CLSID</span></span><br/>                    | <span data-ttu-id="df455-125">CLSID \_ SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="df455-125">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="df455-126">IID</span><span class="sxs-lookup"><span data-stu-id="df455-126">IID</span></span><br/>                      | <span data-ttu-id="df455-127">IID \_ ISWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="df455-127">IID\_ISWbemPrivilege</span></span><br/>                                                         |



 

 




