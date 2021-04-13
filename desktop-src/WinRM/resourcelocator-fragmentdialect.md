---
title: 'ResourceLocator. FragmentDialect 屬性 (WSManDisp .h) '
description: 取得或設定在會話物件作業（例如 Session. Get、Session. Put 或 Session. 列舉）中使用 ResourceLocator 時，資源片段方言的語言方言。
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- FragmentDialect 屬性 Windows 遠端管理
- FragmentDialect 屬性 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理、FragmentDialect 屬性
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1fe42c2bbe15c75d5f38ea47119f9649e678931
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466685"
---
# <a name="resourcelocatorfragmentdialect-property"></a><span data-ttu-id="532ba-106">ResourceLocator. FragmentDialect 屬性</span><span class="sxs-lookup"><span data-stu-id="532ba-106">ResourceLocator.FragmentDialect property</span></span>

<span data-ttu-id="532ba-107">取得或設定在 [**會話**](session.md)物件作業（例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**session. 列舉**](session-enumerate.md)）中使用 [**ResourceLocator**](resourcelocator.md)時，[*資源*](windows-remote-management-glossary.md)[*片段*](windows-remote-management-glossary.md)*方言* 的語言方言。</span><span class="sxs-lookup"><span data-stu-id="532ba-107">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) *dialect* when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="532ba-108">片段代表資源的一個屬性或部分。</span><span class="sxs-lookup"><span data-stu-id="532ba-108">A fragment represents one property or part of a resource.</span></span> <span data-ttu-id="532ba-109">您可以提供 [**ResourceLocator**](resourcelocator.md) 物件，而不是在 [**會話**](session.md) 物件作業中指定資源 URI。</span><span class="sxs-lookup"><span data-stu-id="532ba-109">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="532ba-110">此方言會指出哪一個 XML 語言描述處理 [WS-Management 通訊協定](ws-management-protocol.md) 並接收要求之服務的片段。</span><span class="sxs-lookup"><span data-stu-id="532ba-110">The dialect indicates what XML language describes the fragment to the service that implements the [WS-Management Protocol](ws-management-protocol.md) and receives the request.</span></span>

<span data-ttu-id="532ba-111">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="532ba-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="532ba-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="532ba-112">Syntax</span></span>


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a><span data-ttu-id="532ba-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="532ba-113">Property value</span></span>

<span data-ttu-id="532ba-114">識別 [**FragmentPath**](resourcelocator-fragmentpath.md) 屬性中所使用之語言的 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="532ba-114">An XML string that identifies the language used in the [**FragmentPath**](resourcelocator-fragmentpath.md) property.</span></span> <span data-ttu-id="532ba-115">此方言字串預設為 XPath 1.0 規格。</span><span class="sxs-lookup"><span data-stu-id="532ba-115">The dialect string defaults to the XPath 1.0 specification.</span></span> <span data-ttu-id="532ba-116">如需詳細資訊，請參閱 [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath)。</span><span class="sxs-lookup"><span data-stu-id="532ba-116">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="remarks"></a><span data-ttu-id="532ba-117">備註</span><span class="sxs-lookup"><span data-stu-id="532ba-117">Remarks</span></span>

<span data-ttu-id="532ba-118">[**IWSManResourceLocator：： FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) 是對應的 c + + 屬性。</span><span class="sxs-lookup"><span data-stu-id="532ba-118">[**IWSManResourceLocator::FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="532ba-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="532ba-119">Requirements</span></span>



| <span data-ttu-id="532ba-120">需求</span><span class="sxs-lookup"><span data-stu-id="532ba-120">Requirement</span></span> | <span data-ttu-id="532ba-121">值</span><span class="sxs-lookup"><span data-stu-id="532ba-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="532ba-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="532ba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="532ba-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="532ba-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="532ba-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="532ba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="532ba-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="532ba-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="532ba-126">標頭</span><span class="sxs-lookup"><span data-stu-id="532ba-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="532ba-127"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="532ba-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="532ba-128">Idl</span><span class="sxs-lookup"><span data-stu-id="532ba-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="532ba-129"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="532ba-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="532ba-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="532ba-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="532ba-131"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="532ba-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="532ba-132">DLL</span><span class="sxs-lookup"><span data-stu-id="532ba-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="532ba-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="532ba-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="532ba-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="532ba-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="532ba-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="532ba-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





