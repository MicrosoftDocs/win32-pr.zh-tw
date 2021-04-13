---
title: 'INapSoHProcessor GetNumberOfAttributes 方法 (NapProtocol .h) '
description: 捕獲 SoH 中的屬性總數。
ms.assetid: ee0b1857-65a7-47bb-ae91-c939344a24d0
keywords:
- GetNumberOfAttributes 方法 NAP
- GetNumberOfAttributes 方法 NAP，INapSoHProcessor 介面
- INapSoHProcessor 介面 NAP，GetNumberOfAttributes 方法
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetNumberOfAttributes
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1336362b44d49c71ce81b197f9f95b1a1b8fc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508571"
---
# <a name="inapsohprocessorgetnumberofattributes-method"></a><span data-ttu-id="06279-106">INapSoHProcessor：： GetNumberOfAttributes 方法</span><span class="sxs-lookup"><span data-stu-id="06279-106">INapSoHProcessor::GetNumberOfAttributes method</span></span>

> [!Note]  
> <span data-ttu-id="06279-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="06279-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="06279-108">**INapSoHProcessor：： GetNumberOfAttributes** 方法會抓取 SoH 中的屬性總數。</span><span class="sxs-lookup"><span data-stu-id="06279-108">The **INapSoHProcessor::GetNumberOfAttributes** method retrieves the total number of attributes in the SoH.</span></span>

## <a name="syntax"></a><span data-ttu-id="06279-109">語法</span><span class="sxs-lookup"><span data-stu-id="06279-109">Syntax</span></span>


```C++
HRESULT GetNumberOfAttributes(
  [out] UINT16 *attributeCount
);
```



## <a name="parameters"></a><span data-ttu-id="06279-110">參數</span><span class="sxs-lookup"><span data-stu-id="06279-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06279-111">*attributeCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="06279-111">*attributeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06279-112">傳回之屬性計數的指標。</span><span class="sxs-lookup"><span data-stu-id="06279-112">A pointer to the returned attribute count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06279-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="06279-113">Return value</span></span>

<span data-ttu-id="06279-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="06279-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="06279-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="06279-115">Return code</span></span>                                                                                     | <span data-ttu-id="06279-116">Description</span><span class="sxs-lookup"><span data-stu-id="06279-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="06279-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="06279-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="06279-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="06279-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="06279-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="06279-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="06279-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="06279-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="06279-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="06279-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="06279-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="06279-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="06279-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="06279-123">Requirements</span></span>



| <span data-ttu-id="06279-124">需求</span><span class="sxs-lookup"><span data-stu-id="06279-124">Requirement</span></span> | <span data-ttu-id="06279-125">值</span><span class="sxs-lookup"><span data-stu-id="06279-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="06279-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06279-126">Minimum supported client</span></span><br/> | <span data-ttu-id="06279-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06279-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="06279-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06279-128">Minimum supported server</span></span><br/> | <span data-ttu-id="06279-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06279-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="06279-130">標頭</span><span class="sxs-lookup"><span data-stu-id="06279-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="06279-131"><dt>NapProtocol。h</dt></span><span class="sxs-lookup"><span data-stu-id="06279-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="06279-132">Idl</span><span class="sxs-lookup"><span data-stu-id="06279-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06279-133"><dt>NapProtocol .idl</dt></span><span class="sxs-lookup"><span data-stu-id="06279-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="06279-134">DLL</span><span class="sxs-lookup"><span data-stu-id="06279-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06279-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06279-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="06279-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06279-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06279-137">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="06279-137">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





