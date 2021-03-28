---
description: 以字串格式將登入名稱轉譯為對應的使用者安全識別碼。
title: DiskQuotaControl. TranslateLogonNameToSID 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: ec5e6c0bbd013c8fbd3f6616671ee006109566d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027059"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a><span data-ttu-id="2d332-103">DiskQuotaControl. TranslateLogonNameToSID 方法</span><span class="sxs-lookup"><span data-stu-id="2d332-103">DiskQuotaControl.TranslateLogonNameToSID method</span></span>

<span data-ttu-id="2d332-104">以字串格式將登入名稱轉譯為對應的使用者安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d332-104">Translates a logon name to the corresponding user security ID in string format.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d332-105">語法</span><span class="sxs-lookup"><span data-stu-id="2d332-105">Syntax</span></span>


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a><span data-ttu-id="2d332-106">參數</span><span class="sxs-lookup"><span data-stu-id="2d332-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d332-107">*logonname*</span><span class="sxs-lookup"><span data-stu-id="2d332-107">*logonname*</span></span> 
</dt> <dd>

<span data-ttu-id="2d332-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2d332-108">Type: **String**</span></span>

<span data-ttu-id="2d332-109">指定使用者登入名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="2d332-109">A string value that specifies the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d332-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d332-110">Return value</span></span>

<span data-ttu-id="2d332-111">以對應至所提供登入名稱的字串格式，傳回 (SID) 的使用者安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d332-111">Returns the user security ID (SID) in string format corresponding to the provided logon name.</span></span> <span data-ttu-id="2d332-112">傳回的字串包含標準的封閉括弧。</span><span class="sxs-lookup"><span data-stu-id="2d332-112">The returned string includes the standard enclosing braces.</span></span> <span data-ttu-id="2d332-113">例如：</span><span class="sxs-lookup"><span data-stu-id="2d332-113">For example:</span></span>

<span data-ttu-id="2d332-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span><span class="sxs-lookup"><span data-stu-id="2d332-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span></span>

## <a name="remarks"></a><span data-ttu-id="2d332-115">備註</span><span class="sxs-lookup"><span data-stu-id="2d332-115">Remarks</span></span>

<span data-ttu-id="2d332-116">傳回的 SID 字串可以傳遞至 [**FindUser**](diskquotacontrol-finduser.md) 方法，以取代登入名稱。</span><span class="sxs-lookup"><span data-stu-id="2d332-116">The returned SID string can be passed to the [**FindUser**](diskquotacontrol-finduser.md) method in place of a logon name.</span></span>

<span data-ttu-id="2d332-117">[**FindUser**](diskquotacontrol-finduser.md) ( *logonname*) 方法的呼叫失敗時，可能是因為表單 (（例如，安全性帳戶管理員 \[ SAM 相容） \] 和使用者主體名稱 \[ UPN \]) 所提供的登入名稱和儲存在 SID 名稱快取中的表單不符。</span><span class="sxs-lookup"><span data-stu-id="2d332-117">When a call to the [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) method fails, it could be due to a mismatch between the form (for example, Security Account Manager \[SAM\] compatible and User Principal Name \[UPN\]) of the logon name provided and the form stored in the SID-name cache.</span></span> <span data-ttu-id="2d332-118">在這種情況下，登入名稱可以轉換為 SID，並重複呼叫 **FindUser** 。</span><span class="sxs-lookup"><span data-stu-id="2d332-118">In such cases, the logon name can be converted to a SID and the call to **FindUser** repeated.</span></span> <span data-ttu-id="2d332-119">**FindUser** 會辨識 sid 字串，且會略過 sid 名稱快取查閱。</span><span class="sxs-lookup"><span data-stu-id="2d332-119">**FindUser** recognizes a SID string and will bypass the SID-name cache lookup.</span></span> <span data-ttu-id="2d332-120">下列 Microsoft Visual Basic Scripting Edition (VBScript) 程式碼說明這項技巧。</span><span class="sxs-lookup"><span data-stu-id="2d332-120">The following Microsoft Visual Basic Scripting Edition (VBScript) code illustrates this technique.</span></span>


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



<span data-ttu-id="2d332-121">相較于 SID 名稱快取中的查閱，名稱對 SID 轉譯可能會是較慢的進程。</span><span class="sxs-lookup"><span data-stu-id="2d332-121">Name-to-SID translation can be a slow process when compared to lookups in the SID-name cache.</span></span> <span data-ttu-id="2d332-122">因此，建議您先使用登入名稱來呼叫 [**FindUser**](diskquotacontrol-finduser.md) 。</span><span class="sxs-lookup"><span data-stu-id="2d332-122">Therefore, it is recommended that [**FindUser**](diskquotacontrol-finduser.md) first be called with a logon name.</span></span> <span data-ttu-id="2d332-123">上述範例使用這項技術。</span><span class="sxs-lookup"><span data-stu-id="2d332-123">The example above uses this technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d332-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d332-124">Requirements</span></span>



| <span data-ttu-id="2d332-125">需求</span><span class="sxs-lookup"><span data-stu-id="2d332-125">Requirement</span></span> | <span data-ttu-id="2d332-126">值</span><span class="sxs-lookup"><span data-stu-id="2d332-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d332-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d332-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2d332-128">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d332-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d332-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d332-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2d332-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d332-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2d332-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2d332-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d332-132"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="2d332-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d332-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d332-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d332-134">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="2d332-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




