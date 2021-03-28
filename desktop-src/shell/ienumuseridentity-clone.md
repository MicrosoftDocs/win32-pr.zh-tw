---
description: IEnumUserIdentity：： Clone 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: dde9afca-db8d-41ba-afa0-94eadecb695b
title: 'IEnumUserIdentity：： Clone 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Clone
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: ebdec426fe7ab591c801c00b637211e903cf5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991530"
---
# <a name="ienumuseridentityclone-method"></a><span data-ttu-id="f886c-104">IEnumUserIdentity：： Clone 方法</span><span class="sxs-lookup"><span data-stu-id="f886c-104">IEnumUserIdentity::Clone method</span></span>

<span data-ttu-id="f886c-105">\[**IEnumUserIdentity：： Clone** 不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="f886c-105">\[**IEnumUserIdentity::Clone** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="f886c-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="f886c-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="f886c-107">取得目前列舉的複本。</span><span class="sxs-lookup"><span data-stu-id="f886c-107">Gets a copy of the current enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="f886c-108">語法</span><span class="sxs-lookup"><span data-stu-id="f886c-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumUserIdentity **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="f886c-109">參數</span><span class="sxs-lookup"><span data-stu-id="f886c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f886c-110">*ppenum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f886c-110">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f886c-111">類型： **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f886c-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="f886c-112">接收此列舉複本之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="f886c-112">The address of a pointer that receives a copy of this enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f886c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f886c-113">Return value</span></span>

<span data-ttu-id="f886c-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f886c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="f886c-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f886c-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f886c-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f886c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f886c-117">備註</span><span class="sxs-lookup"><span data-stu-id="f886c-117">Remarks</span></span>

<span data-ttu-id="f886c-118">[**IEnumUserIdentity**](ienumuseridentity.md) 會保留內部計數，以指定要取出的介面。</span><span class="sxs-lookup"><span data-stu-id="f886c-118">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="f886c-119">此計數的值將會套用至 *ppenum* 所接收的介面。</span><span class="sxs-lookup"><span data-stu-id="f886c-119">The value of this count will be applied to the interface received by *ppenum*.</span></span> <span data-ttu-id="f886c-120">若要重設計數，請呼叫 [**IEnumUserIdentity：： reset**](ienumuseridentity-reset.md)。</span><span class="sxs-lookup"><span data-stu-id="f886c-120">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f886c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f886c-121">Requirements</span></span>



| <span data-ttu-id="f886c-122">需求</span><span class="sxs-lookup"><span data-stu-id="f886c-122">Requirement</span></span> | <span data-ttu-id="f886c-123">值</span><span class="sxs-lookup"><span data-stu-id="f886c-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f886c-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f886c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f886c-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f886c-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f886c-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f886c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f886c-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f886c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f886c-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f886c-128">End of client support</span></span><br/>    | <span data-ttu-id="f886c-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f886c-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="f886c-130">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f886c-130">End of server support</span></span><br/>    | <span data-ttu-id="f886c-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f886c-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="f886c-132">標頭</span><span class="sxs-lookup"><span data-stu-id="f886c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f886c-133"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="f886c-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="f886c-134">Idl</span><span class="sxs-lookup"><span data-stu-id="f886c-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f886c-135"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f886c-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="f886c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f886c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f886c-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f886c-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f886c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f886c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f886c-139">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="f886c-139">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="f886c-140">**IEnumUserIdentity：： Reset**</span><span class="sxs-lookup"><span data-stu-id="f886c-140">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> </dl>

 

 




