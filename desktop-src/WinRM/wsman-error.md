---
title: 'WSMan. Error 屬性 (WSManDisp .h) '
description: 如果 Windows 遠端管理服務無法建立會話物件、ConnectionOptions 物件或 ResourceLocator 物件，請在 XML 資料流程中取得先前呼叫 WSMan 方法的其他錯誤資訊。
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Error 屬性 Windows 遠端管理
- Error 屬性 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，Error 屬性
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f9e7ffd42d67807f2f7b6096a89ed91e3d95af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103805"
---
# <a name="wsmanerror-property"></a><span data-ttu-id="b956c-106">WSMan. Error 屬性</span><span class="sxs-lookup"><span data-stu-id="b956c-106">WSMan.Error property</span></span>

<span data-ttu-id="b956c-107">如果 Windows 遠端管理服務無法建立 [**會話**](session.md)物件、 [**ConnectionOptions**](connectionoptions.md)物件或 [**RESOURCELOCATOR**](resourcelocator.md)物件，請在 XML 資料流程中取得先前呼叫 [**WSMan**](wsman.md)方法的其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="b956c-107">Gets additional error information, in an XML stream, for the preceding call to a [**WSMan**](wsman.md) method if Windows Remote Management service was unable to create a [**Session**](session.md) object, a [**ConnectionOptions**](connectionoptions.md) object, or a [**ResourceLocator**](resourcelocator.md) object.</span></span>

<span data-ttu-id="b956c-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b956c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b956c-109">語法</span><span class="sxs-lookup"><span data-stu-id="b956c-109">Syntax</span></span>


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a><span data-ttu-id="b956c-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="b956c-110">Property value</span></span>

<span data-ttu-id="b956c-111">錯誤資訊的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="b956c-111">The XML representation of the error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b956c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="b956c-112">Requirements</span></span>



| <span data-ttu-id="b956c-113">需求</span><span class="sxs-lookup"><span data-stu-id="b956c-113">Requirement</span></span> | <span data-ttu-id="b956c-114">值</span><span class="sxs-lookup"><span data-stu-id="b956c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b956c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b956c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b956c-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b956c-116">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b956c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b956c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b956c-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b956c-118">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b956c-119">標頭</span><span class="sxs-lookup"><span data-stu-id="b956c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b956c-120"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b956c-120"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b956c-121">Idl</span><span class="sxs-lookup"><span data-stu-id="b956c-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b956c-122"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b956c-122"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b956c-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="b956c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b956c-124"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b956c-124"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b956c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b956c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b956c-126"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b956c-126"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b956c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b956c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b956c-128">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="b956c-128">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





