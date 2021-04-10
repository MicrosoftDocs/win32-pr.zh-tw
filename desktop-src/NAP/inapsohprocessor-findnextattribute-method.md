---
title: 'INapSoHProcessor FindNextAttribute 方法 (NapProtocol .h) '
description: 尋找 SoHAttributeType 所指定類型之下一個屬性的位置 (索引) 。
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- FindNextAttribute 方法 NAP
- FindNextAttribute 方法 NAP，INapSoHProcessor 介面
- INapSoHProcessor 介面 NAP，FindNextAttribute 方法
topic_type:
- apiref
api_name:
- INapSoHProcessor.FindNextAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a270e36f8254ed5dbfcd9776cf013f9d10d4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685588"
---
# <a name="inapsohprocessorfindnextattribute-method"></a><span data-ttu-id="25642-106">INapSoHProcessor：： FindNextAttribute 方法</span><span class="sxs-lookup"><span data-stu-id="25642-106">INapSoHProcessor::FindNextAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="25642-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="25642-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="25642-108">**INapSoHProcessor：： FindNextAttribute** 方法會尋找 *SoHAttributeType* 所指定類型之下一個屬性的位置 (索引) 。</span><span class="sxs-lookup"><span data-stu-id="25642-108">The **INapSoHProcessor::FindNextAttribute** method finds the location (index) of the next attribute of the type indicated by *SoHAttributeType*.</span></span>

## <a name="syntax"></a><span data-ttu-id="25642-109">語法</span><span class="sxs-lookup"><span data-stu-id="25642-109">Syntax</span></span>


```C++
HRESULT FindNextAttribute(
  [in]  UINT16           fromLocation,
  [in]  SoHAttributeType type,
  [out] UINT16           *attributeLocation
);
```



## <a name="parameters"></a><span data-ttu-id="25642-110">參數</span><span class="sxs-lookup"><span data-stu-id="25642-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25642-111">*fromLocation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25642-111">*fromLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25642-112">在健全狀況聲明中 (索引) 的起始位置 (SoH) 封包，以開始進行屬性搜尋。</span><span class="sxs-lookup"><span data-stu-id="25642-112">The starting location (index) in the Statement of Health (SoH) packet to begin the attribute search.</span></span> <span data-ttu-id="25642-113">這個值必須介於0到 (**numAttrib** -1) ，其中 **NumAttrib** 是使用 [**INapSoHProcessor：： GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md)抓取。</span><span class="sxs-lookup"><span data-stu-id="25642-113">This value must be in the range of 0 to (**numAttrib** - 1) where **numAttrib** is retrieved using [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="25642-114">SoH 封包使用以0為基底的屬性索引。</span><span class="sxs-lookup"><span data-stu-id="25642-114">The SoH packet uses 0-based attribute indices.</span></span>

 

</dd> <dt>

<span data-ttu-id="25642-115">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25642-115">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25642-116">[**SoHAttributeType**](sohattributetype-enum.md)結構，其中包含要尋找的屬性型別。</span><span class="sxs-lookup"><span data-stu-id="25642-116">An [**SoHAttributeType**](sohattributetype-enum.md) structure that contains the attribute type to locate.</span></span>

</dd> <dt>

<span data-ttu-id="25642-117">*attributeLocation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="25642-117">*attributeLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25642-118">指標，其中包含從索引 *FromLocation* *SoHAttributeType* 類型之第一個屬性之 SoH 封包中的位置 (索引) 。</span><span class="sxs-lookup"><span data-stu-id="25642-118">A pointer that contains the location (index) in the SoH packet of the first attribute of type *SoHAttributeType* from the index *fromLocation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25642-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="25642-119">Return value</span></span>

<span data-ttu-id="25642-120">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="25642-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="25642-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="25642-121">Return code</span></span>                                                                                            | <span data-ttu-id="25642-122">Description</span><span class="sxs-lookup"><span data-stu-id="25642-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="25642-123"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="25642-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="25642-124">作業成功。</span><span class="sxs-lookup"><span data-stu-id="25642-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="25642-125"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="25642-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="25642-126">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="25642-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="25642-127"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="25642-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="25642-128">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="25642-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="25642-129"><dt>**\_ \_ \_ 找不到錯誤檔案**</dt></span><span class="sxs-lookup"><span data-stu-id="25642-129"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="25642-130">找不到屬性。</span><span class="sxs-lookup"><span data-stu-id="25642-130">Attribute not found.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="25642-131">備註</span><span class="sxs-lookup"><span data-stu-id="25642-131">Remarks</span></span>

<span data-ttu-id="25642-132">**FindNextAttribute** 方法會從 *fromLocation* 和更新版本所指定的索引中搜尋 *SoHAttributeType* 類型的屬性，直到找到相符的屬性為止。</span><span class="sxs-lookup"><span data-stu-id="25642-132">The **FindNextAttribute** method searches for attributes of type *SoHAttributeType* from the index specified by *fromLocation* and higher until a match is found.</span></span> <span data-ttu-id="25642-133">如果找不到相符項，則會傳回 **錯誤 \_ \_ \_** 檔案。</span><span class="sxs-lookup"><span data-stu-id="25642-133">If no match is found, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="25642-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="25642-134">Requirements</span></span>



| <span data-ttu-id="25642-135">需求</span><span class="sxs-lookup"><span data-stu-id="25642-135">Requirement</span></span> | <span data-ttu-id="25642-136">值</span><span class="sxs-lookup"><span data-stu-id="25642-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="25642-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25642-137">Minimum supported client</span></span><br/> | <span data-ttu-id="25642-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25642-138">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="25642-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25642-139">Minimum supported server</span></span><br/> | <span data-ttu-id="25642-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25642-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="25642-141">標頭</span><span class="sxs-lookup"><span data-stu-id="25642-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="25642-142"><dt>NapProtocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="25642-142"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="25642-143">Idl</span><span class="sxs-lookup"><span data-stu-id="25642-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="25642-144"><dt>NapProtocol .idl</dt></span><span class="sxs-lookup"><span data-stu-id="25642-144"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="25642-145">DLL</span><span class="sxs-lookup"><span data-stu-id="25642-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25642-146"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25642-146"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="25642-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25642-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25642-148">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="25642-148">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





