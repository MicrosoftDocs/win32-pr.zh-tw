---
description: SWbemRefresher 物件的 AutoReconnect 屬性是一個布林值，指出如果連接中斷，重新整理程式是否會自動重新連接至遠端提供者。
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: 'SWbemRefresher. AutoReconnect 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4faa02a4a77409bb8b1813ee433c326d1c45d1bd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321504"
---
# <a name="swbemrefresherautoreconnect-property"></a><span data-ttu-id="aa39d-103">SWbemRefresher. AutoReconnect 屬性</span><span class="sxs-lookup"><span data-stu-id="aa39d-103">SWbemRefresher.AutoReconnect property</span></span>

<span data-ttu-id="aa39d-104">[**SWbemRefresher**](swbemrefresher.md)物件的 **AutoReconnect** 屬性是一個布林值，指出如果連接中斷，重新整理程式是否會自動重新連接至遠端提供者。</span><span class="sxs-lookup"><span data-stu-id="aa39d-104">The **AutoReconnect** property of the [**SWbemRefresher**](swbemrefresher.md) object is a Boolean value that indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span>

<span data-ttu-id="aa39d-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="aa39d-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="aa39d-106">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="aa39d-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa39d-107">語法</span><span class="sxs-lookup"><span data-stu-id="aa39d-107">Syntax</span></span>


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a><span data-ttu-id="aa39d-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="aa39d-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="aa39d-109">備註</span><span class="sxs-lookup"><span data-stu-id="aa39d-109">Remarks</span></span>

<span data-ttu-id="aa39d-110">修改此屬性只會影響重新整理程式中由高效能提供者所支援的物件。</span><span class="sxs-lookup"><span data-stu-id="aa39d-110">Modifying this property affects only objects in the refresher that are backed by a high-performance provider.</span></span> <span data-ttu-id="aa39d-111">如果提供者不是高效能的提供者，則將 **AutoReconnect** 屬性設定為 **TRUE** 不會有任何作用，因為 [**SWbemRefresher**](swbemrefresher.md) 物件永遠不會重新連接。</span><span class="sxs-lookup"><span data-stu-id="aa39d-111">If the provider is not a high-performance provider, then setting the **AutoReconnect** property to **TRUE** has no effect because the [**SWbemRefresher**](swbemrefresher.md) object never reconnects.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa39d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa39d-112">Requirements</span></span>



| <span data-ttu-id="aa39d-113">需求</span><span class="sxs-lookup"><span data-stu-id="aa39d-113">Requirement</span></span> | <span data-ttu-id="aa39d-114">值</span><span class="sxs-lookup"><span data-stu-id="aa39d-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa39d-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa39d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="aa39d-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa39d-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa39d-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa39d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="aa39d-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa39d-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa39d-119">標頭</span><span class="sxs-lookup"><span data-stu-id="aa39d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa39d-120"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa39d-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa39d-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="aa39d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa39d-122"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aa39d-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aa39d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="aa39d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa39d-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa39d-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa39d-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="aa39d-125">CLSID</span></span><br/>                    | <span data-ttu-id="aa39d-126">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="aa39d-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="aa39d-127">IID</span><span class="sxs-lookup"><span data-stu-id="aa39d-127">IID</span></span><br/>                      | <span data-ttu-id="aa39d-128">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="aa39d-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="aa39d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa39d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa39d-130">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="aa39d-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




