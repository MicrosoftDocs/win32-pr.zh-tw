---
description: 在磁片區的配額檔案中，依名稱尋找使用者的專案。
title: DiskQuotaControl. FindUser 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: af1bc9c0398d37f04e47515a2b85cb4520795b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971965"
---
# <a name="diskquotacontrolfinduser-method"></a><span data-ttu-id="35fe4-103">DiskQuotaControl. FindUser 方法</span><span class="sxs-lookup"><span data-stu-id="35fe4-103">DiskQuotaControl.FindUser method</span></span>

<span data-ttu-id="35fe4-104">在磁片區的配額檔案中，依名稱尋找使用者的專案。</span><span class="sxs-lookup"><span data-stu-id="35fe4-104">Finds a user's entry, by name, in the volume's quota file.</span></span>

## <a name="syntax"></a><span data-ttu-id="35fe4-105">語法</span><span class="sxs-lookup"><span data-stu-id="35fe4-105">Syntax</span></span>


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="35fe4-106">參數</span><span class="sxs-lookup"><span data-stu-id="35fe4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fe4-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="35fe4-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="35fe4-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35fe4-108">Type: **String**</span></span>

<span data-ttu-id="35fe4-109">包含使用者登入名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="35fe4-109">A string value that contains the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35fe4-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="35fe4-110">Return value</span></span>

<span data-ttu-id="35fe4-111">傳回評估為使用者 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的物件運算式。</span><span class="sxs-lookup"><span data-stu-id="35fe4-111">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="35fe4-112">備註</span><span class="sxs-lookup"><span data-stu-id="35fe4-112">Remarks</span></span>

<span data-ttu-id="35fe4-113">即使配額檔案中沒有使用者的專案，這個方法也會傳回 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="35fe4-113">This method returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object even if there is no entry for the user in the quota file.</span></span> <span data-ttu-id="35fe4-114">傳回的使用者物件具有警告臨界值，且會將固定配額限制設定為磁片區的預設值。</span><span class="sxs-lookup"><span data-stu-id="35fe4-114">The returned user object has warning threshold and hard quota limits set to the volume's default values.</span></span>

<span data-ttu-id="35fe4-115">從 [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) 傳回的字串可以用來取代 *sLogonName* 參數。</span><span class="sxs-lookup"><span data-stu-id="35fe4-115">The string returned from [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) may be passed in place of the *sLogonName* parameter.</span></span> <span data-ttu-id="35fe4-116">當 **FindUser** 收到 sid 字串時，會使用對應的 sid 直接查閱磁片區上的使用者配額記錄。</span><span class="sxs-lookup"><span data-stu-id="35fe4-116">When **FindUser** receives a SID string it uses the corresponding SID for direct lookup of the user's quota record on the volume.</span></span> <span data-ttu-id="35fe4-117">這會略過 SID 名稱快取。</span><span class="sxs-lookup"><span data-stu-id="35fe4-117">This bypasses the SID-name cache.</span></span> <span data-ttu-id="35fe4-118">如果 **FindUser** 因格式不相符而失敗 (例如，提供的登入名稱與 SAM 相容的 UPN) ，以及快取的登入名稱，則可以使用 **TranslateLogonNameToSID** 將登入名稱轉譯成 SID 字串，然後再傳遞到 **FindUser**。</span><span class="sxs-lookup"><span data-stu-id="35fe4-118">In cases where **FindUser** fails due to a mismatch in format (for example, SAM-compatible and UPN) of the logon name provided and the logon name cached, the logon name can be translated to a SID string using **TranslateLogonNameToSID** then passed again to **FindUser**.</span></span> <span data-ttu-id="35fe4-119">下列 VBScript 程式碼說明這項技巧。</span><span class="sxs-lookup"><span data-stu-id="35fe4-119">The following VBScript code illustrates this technique.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="35fe4-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="35fe4-120">Requirements</span></span>



| <span data-ttu-id="35fe4-121">需求</span><span class="sxs-lookup"><span data-stu-id="35fe4-121">Requirement</span></span> | <span data-ttu-id="35fe4-122">值</span><span class="sxs-lookup"><span data-stu-id="35fe4-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35fe4-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35fe4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="35fe4-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35fe4-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35fe4-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35fe4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="35fe4-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35fe4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="35fe4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="35fe4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35fe4-128"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="35fe4-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35fe4-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35fe4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fe4-130">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="35fe4-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




