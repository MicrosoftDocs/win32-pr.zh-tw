---
title: 'ResourceLocator. AddOption 方法 (WSManDisp .h) '
description: 新增處理要求所需的其他資料。 例如，某些 WMI 提供者可能需要具有提供者特定資訊的 IWbemCoNtext 或 SWbemNamedValueSet 物件。
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- AddOption 方法 Windows 遠端管理
- AddOption 方法 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理，AddOption 方法
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 882f400dd2c59d2395dd2755846245f4e4ad385e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024745"
---
# <a name="resourcelocatoraddoption-method"></a><span data-ttu-id="0a067-107">ResourceLocator. AddOption 方法</span><span class="sxs-lookup"><span data-stu-id="0a067-107">ResourceLocator.AddOption method</span></span>

<span data-ttu-id="0a067-108">新增處理要求所需的其他資料。</span><span class="sxs-lookup"><span data-stu-id="0a067-108">Adds additional data required to process the request.</span></span> <span data-ttu-id="0a067-109">例如，某些 WMI 提供者可能需要具有提供者特定資訊的 [**IWbemCoNtext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) 或 [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) 物件。</span><span class="sxs-lookup"><span data-stu-id="0a067-109">For example, some WMI providers may require an [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) or [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) object with provider-specific information.</span></span> <span data-ttu-id="0a067-110">您可以提供 [**ResourceLocator**](resourcelocator.md) 物件，而不是在 [**會話**](session.md) 物件作業中指定資源 URI，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。</span><span class="sxs-lookup"><span data-stu-id="0a067-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a067-111">語法</span><span class="sxs-lookup"><span data-stu-id="0a067-111">Syntax</span></span>


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a><span data-ttu-id="0a067-112">參數</span><span class="sxs-lookup"><span data-stu-id="0a067-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a067-113">*選項名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0a067-113">*OptionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a067-114">選擇性資料物件 (索引鍵) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a067-114">The name (key) of the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="0a067-115">*OptionValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0a067-115">*OptionValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a067-116">為選擇性資料物件提供的值。</span><span class="sxs-lookup"><span data-stu-id="0a067-116">A value supplied for the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="0a067-117">*mustComply* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0a067-117">*mustComply* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a067-118">指出必須處理選項的旗標。</span><span class="sxs-lookup"><span data-stu-id="0a067-118">A flag that indicates the option must be processed.</span></span> <span data-ttu-id="0a067-119">預設值為 **False** (0) 。</span><span class="sxs-lookup"><span data-stu-id="0a067-119">The default is **False** (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a067-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a067-120">Return value</span></span>

<span data-ttu-id="0a067-121">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0a067-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a067-122">備註</span><span class="sxs-lookup"><span data-stu-id="0a067-122">Remarks</span></span>

<span data-ttu-id="0a067-123">**IWSManResourceLocator：： AddOption** 是對應的 c + + 方法。</span><span class="sxs-lookup"><span data-stu-id="0a067-123">**IWSManResourceLocator::AddOption** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a067-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a067-124">Requirements</span></span>



| <span data-ttu-id="0a067-125">需求</span><span class="sxs-lookup"><span data-stu-id="0a067-125">Requirement</span></span> | <span data-ttu-id="0a067-126">值</span><span class="sxs-lookup"><span data-stu-id="0a067-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a067-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a067-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0a067-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a067-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="0a067-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a067-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0a067-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a067-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0a067-131">標頭</span><span class="sxs-lookup"><span data-stu-id="0a067-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a067-132"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a067-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a067-133">Idl</span><span class="sxs-lookup"><span data-stu-id="0a067-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0a067-134"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0a067-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="0a067-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="0a067-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a067-136"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0a067-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0a067-137">DLL</span><span class="sxs-lookup"><span data-stu-id="0a067-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a067-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a067-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0a067-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a067-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a067-140">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="0a067-140">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

