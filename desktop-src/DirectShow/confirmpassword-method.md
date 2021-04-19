---
description: DVDAdm. ConfirmPassword 方法會測試指定的密碼是否符合先前儲存的密碼。
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: 'ConfirmPassword 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987153"
---
# <a name="confirmpassword-method"></a><span data-ttu-id="43383-103">ConfirmPassword 方法</span><span class="sxs-lookup"><span data-stu-id="43383-103">ConfirmPassword Method</span></span>

> [!Note]  
> <span data-ttu-id="43383-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="43383-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="43383-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="43383-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="43383-106">`DVDAdm.ConfirmPassword`方法會測試指定的密碼是否符合先前儲存的密碼。</span><span class="sxs-lookup"><span data-stu-id="43383-106">The `DVDAdm.ConfirmPassword` method tests whether the specified password matches the previously saved password.</span></span>

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="43383-107">參數</span><span class="sxs-lookup"><span data-stu-id="43383-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43383-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="43383-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="43383-109">將使用者的名稱指定為字串。</span><span class="sxs-lookup"><span data-stu-id="43383-109">Specifies the user's name as a String.</span></span>

</dd> <dt>

<span data-ttu-id="43383-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="43383-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="43383-111">將新密碼指定為字串。</span><span class="sxs-lookup"><span data-stu-id="43383-111">Specifies the new password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43383-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="43383-112">Return Value</span></span>

<span data-ttu-id="43383-113">如果指定的密碼符合現有的密碼，則傳回 true，否則傳回 false。</span><span class="sxs-lookup"><span data-stu-id="43383-113">Returns true if the specified password matches the existing password, false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="43383-114">備註</span><span class="sxs-lookup"><span data-stu-id="43383-114">Remarks</span></span>

<span data-ttu-id="43383-115">目前，這個和所有相關的方法會忽略 *sUserName* 參數。</span><span class="sxs-lookup"><span data-stu-id="43383-115">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="43383-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="43383-116">Requirements</span></span>



| <span data-ttu-id="43383-117">需求</span><span class="sxs-lookup"><span data-stu-id="43383-117">Requirement</span></span> | <span data-ttu-id="43383-118">值</span><span class="sxs-lookup"><span data-stu-id="43383-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="43383-119">標頭</span><span class="sxs-lookup"><span data-stu-id="43383-119">Header</span></span><br/> | <dl> <span data-ttu-id="43383-120"><dt>區段。h</dt></span><span class="sxs-lookup"><span data-stu-id="43383-120"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43383-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43383-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43383-122">**ChangePassword**</span><span class="sxs-lookup"><span data-stu-id="43383-122">**ChangePassword**</span></span>](changepassword-method.md)
</dt> <dt>

[<span data-ttu-id="43383-123">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="43383-123">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




