---
title: 'INapSoHProcessor GetAttribute 方法 (NapProtocol .h) '
description: 在指定屬性位置時，抓取屬性型別和值。
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- GetAttribute 方法 NAP
- GetAttribute 方法 NAP，INapSoHProcessor 介面
- INapSoHProcessor 介面 NAP，GetAttribute 方法
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2d7d9cbafa5a44e0f6c24f4c42959c456722a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967315"
---
# <a name="inapsohprocessorgetattribute-method"></a><span data-ttu-id="b8d90-106">INapSoHProcessor：： GetAttribute 方法</span><span class="sxs-lookup"><span data-stu-id="b8d90-106">INapSoHProcessor::GetAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="b8d90-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="b8d90-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b8d90-108">**INapSoHProcessor：： GetAttribute** 方法會在指定屬性位置時，抓取屬性型別和值。</span><span class="sxs-lookup"><span data-stu-id="b8d90-108">The **INapSoHProcessor::GetAttribute** method retrieves the attribute type and value, given the attribute location.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d90-109">語法</span><span class="sxs-lookup"><span data-stu-id="b8d90-109">Syntax</span></span>


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a><span data-ttu-id="b8d90-110">參數</span><span class="sxs-lookup"><span data-stu-id="b8d90-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8d90-111">*attributeLocation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8d90-111">*attributeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d90-112">要抓取其類型和值的屬性位置 (索引) 。</span><span class="sxs-lookup"><span data-stu-id="b8d90-112">The location (index) of the attribute whose type and value are to be retrieved.</span></span> <span data-ttu-id="b8d90-113">*AttributeLocation* 的值會從先前的 [**INapSoHProcessor：： FindNextAttribute**](inapsohprocessor-findnextattribute-method.md)呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="b8d90-113">The value of *attributeLocation* is returned from a prior call to [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8d90-114">*類型* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b8d90-114">*type* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d90-115">[**SoHAttributeType**](sohattributetype-enum.md)結構的指標，此結構會指定屬性在 *值* 中的型別。</span><span class="sxs-lookup"><span data-stu-id="b8d90-115">A pointer to an [**SoHAttributeType**](sohattributetype-enum.md) structure that specifies the attribute's type in *value*.</span></span>

</dd> <dt>

<span data-ttu-id="b8d90-116">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b8d90-116">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d90-117">[**SoHAttributeValue**](sohattributevalue-union.md)結構指標的指標，該結構包含屬性的值，如 *類型* 所定義。</span><span class="sxs-lookup"><span data-stu-id="b8d90-117">A pointer to a pointer to a [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the attribute's value as defined by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8d90-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8d90-118">Return value</span></span>

<span data-ttu-id="b8d90-119">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b8d90-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b8d90-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b8d90-120">Return code</span></span>                                                                                     | <span data-ttu-id="b8d90-121">Description</span><span class="sxs-lookup"><span data-stu-id="b8d90-121">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8d90-122"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b8d90-122"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="b8d90-123">作業成功。</span><span class="sxs-lookup"><span data-stu-id="b8d90-123">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b8d90-124"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b8d90-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="b8d90-125">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="b8d90-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b8d90-126"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b8d90-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="b8d90-127">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="b8d90-127">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b8d90-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8d90-128">Requirements</span></span>



| <span data-ttu-id="b8d90-129">需求</span><span class="sxs-lookup"><span data-stu-id="b8d90-129">Requirement</span></span> | <span data-ttu-id="b8d90-130">值</span><span class="sxs-lookup"><span data-stu-id="b8d90-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d90-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8d90-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b8d90-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8d90-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b8d90-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8d90-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b8d90-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8d90-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b8d90-135">標頭</span><span class="sxs-lookup"><span data-stu-id="b8d90-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8d90-136"><dt>NapProtocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8d90-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8d90-137">Idl</span><span class="sxs-lookup"><span data-stu-id="b8d90-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b8d90-138"><dt>NapProtocol .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b8d90-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="b8d90-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b8d90-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8d90-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8d90-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="b8d90-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8d90-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8d90-142">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="b8d90-142">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





