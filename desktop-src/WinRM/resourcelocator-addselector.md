---
title: 'ResourceLocator. AddSelector 方法 (WSManDisp .h) '
description: 將選取器加入至 ResourceLocator 物件。 選取器會指定資源的特定實例。
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- AddSelector 方法 Windows 遠端管理
- AddSelector 方法 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理，AddSelector 方法
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064108f535c9f46dc074d1b37754e626dc3f1d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934424"
---
# <a name="resourcelocatoraddselector-method"></a><span data-ttu-id="e83f2-107">ResourceLocator. AddSelector 方法</span><span class="sxs-lookup"><span data-stu-id="e83f2-107">ResourceLocator.AddSelector method</span></span>

<span data-ttu-id="e83f2-108">將 [*選取器*](windows-remote-management-glossary.md) 加入至 [**ResourceLocator**](resourcelocator.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e83f2-108">Adds a [*selector*](windows-remote-management-glossary.md) to the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="e83f2-109">選取器會指定 *資源* 的特定實例。</span><span class="sxs-lookup"><span data-stu-id="e83f2-109">The selector specifies a particular instance of a *resource*.</span></span> <span data-ttu-id="e83f2-110">您可以提供 [**ResourceLocator**](resourcelocator.md) 物件，而不是在 [**會話**](session.md) 物件作業中指定資源 URI，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。</span><span class="sxs-lookup"><span data-stu-id="e83f2-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e83f2-111">語法</span><span class="sxs-lookup"><span data-stu-id="e83f2-111">Syntax</span></span>


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a><span data-ttu-id="e83f2-112">參數</span><span class="sxs-lookup"><span data-stu-id="e83f2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e83f2-113">*resourceSelName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e83f2-113">*resourceSelName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e83f2-114">選取器名稱。</span><span class="sxs-lookup"><span data-stu-id="e83f2-114">The selector name.</span></span> <span data-ttu-id="e83f2-115">例如，在要求 WMI 資料時，此參數是 WMI 類別的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="e83f2-115">For example, when requesting WMI data, this parameter is the key property for a WMI class.</span></span>

</dd> <dt>

<span data-ttu-id="e83f2-116">*selValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e83f2-116">*selValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e83f2-117">選取器的值。</span><span class="sxs-lookup"><span data-stu-id="e83f2-117">The selector value.</span></span> <span data-ttu-id="e83f2-118">例如，對於 WMI 資料而言，此參數包含識別特定實例之索引鍵屬性的值。</span><span class="sxs-lookup"><span data-stu-id="e83f2-118">For example, for WMI data, this parameter contains a value for a key property that identifies a specific instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e83f2-119">備註</span><span class="sxs-lookup"><span data-stu-id="e83f2-119">Remarks</span></span>

<span data-ttu-id="e83f2-120">**IWSManResourceLocator：： AddSelector** 是對應的 c + + 方法。</span><span class="sxs-lookup"><span data-stu-id="e83f2-120">**IWSManResourceLocator::AddSelector** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e83f2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e83f2-121">Requirements</span></span>



| <span data-ttu-id="e83f2-122">需求</span><span class="sxs-lookup"><span data-stu-id="e83f2-122">Requirement</span></span> | <span data-ttu-id="e83f2-123">值</span><span class="sxs-lookup"><span data-stu-id="e83f2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e83f2-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e83f2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e83f2-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e83f2-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e83f2-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e83f2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e83f2-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e83f2-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e83f2-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e83f2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e83f2-129"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e83f2-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e83f2-130">Idl</span><span class="sxs-lookup"><span data-stu-id="e83f2-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e83f2-131"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e83f2-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e83f2-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="e83f2-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="e83f2-133"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e83f2-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e83f2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e83f2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e83f2-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e83f2-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e83f2-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e83f2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e83f2-137">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="e83f2-137">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





