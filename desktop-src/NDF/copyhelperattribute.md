---
title: 'CopyHelperAttribute 函式 (Ndattributils) '
description: 建立 HELPER 屬性結構的複本 \_ 。
ms.assetid: ff49be29-4cd8-4730-929f-c66a7325704f
keywords:
- CopyHelperAttribute 函式 NDF
topic_type:
- apiref
api_name:
- CopyHelperAttribute
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59fac3449ee48659980681c836d24406c4db7e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968755"
---
# <a name="copyhelperattribute-function"></a><span data-ttu-id="0df1a-104">CopyHelperAttribute 函式</span><span class="sxs-lookup"><span data-stu-id="0df1a-104">CopyHelperAttribute function</span></span>

<span data-ttu-id="0df1a-105">**CopyHelperAttribute** 函式會建立 [**HELPER \_ 屬性**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)結構的複本。</span><span class="sxs-lookup"><span data-stu-id="0df1a-105">The **CopyHelperAttribute** function creates a copy of a [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df1a-106">語法</span><span class="sxs-lookup"><span data-stu-id="0df1a-106">Syntax</span></span>


```C++
HRESULT CopyHelperAttribute(
  _Out_       HELPER_ATTRIBUTE *Dest,
  _In_  const HELPER_ATTRIBUTE *Source
);
```



## <a name="parameters"></a><span data-ttu-id="0df1a-107">參數</span><span class="sxs-lookup"><span data-stu-id="0df1a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0df1a-108">*目的地* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0df1a-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0df1a-109">類型： \* 協助程式 *[**\_ 屬性**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _</span><span class="sxs-lookup"><span data-stu-id="0df1a-109">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="0df1a-110">要更新的結構。</span><span class="sxs-lookup"><span data-stu-id="0df1a-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="0df1a-111">_Source \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0df1a-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0df1a-112">類型： \**Const [**HELPER \_ 屬性**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _</span><span class="sxs-lookup"><span data-stu-id="0df1a-112">Type: \**const [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="0df1a-113">要複製的現有結構。</span><span class="sxs-lookup"><span data-stu-id="0df1a-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0df1a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0df1a-114">Return value</span></span>

<span data-ttu-id="0df1a-115">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="0df1a-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="0df1a-116">可能的傳回值包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="0df1a-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="0df1a-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0df1a-117">Return code</span></span>                                                                                   | <span data-ttu-id="0df1a-118">Description</span><span class="sxs-lookup"><span data-stu-id="0df1a-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0df1a-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0df1a-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0df1a-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="0df1a-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="0df1a-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0df1a-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0df1a-122">未正確提供一或多個參數。</span><span class="sxs-lookup"><span data-stu-id="0df1a-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="0df1a-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0df1a-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0df1a-124">沒有足夠的記憶體可完成此作業。</span><span class="sxs-lookup"><span data-stu-id="0df1a-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0df1a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0df1a-125">Requirements</span></span>



| <span data-ttu-id="0df1a-126">需求</span><span class="sxs-lookup"><span data-stu-id="0df1a-126">Requirement</span></span> | <span data-ttu-id="0df1a-127">值</span><span class="sxs-lookup"><span data-stu-id="0df1a-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0df1a-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0df1a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0df1a-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0df1a-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0df1a-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0df1a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0df1a-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0df1a-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0df1a-132">標頭</span><span class="sxs-lookup"><span data-stu-id="0df1a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0df1a-133"><dt>Ndattributils。h</dt></span><span class="sxs-lookup"><span data-stu-id="0df1a-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0df1a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0df1a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df1a-135">**HELPER \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="0df1a-135">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> </dl>

 

 





