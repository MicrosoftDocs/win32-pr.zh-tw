---
title: 'IADsDomain 屬性方法 (Iads .h) '
description: IADsDomain 介面方法會讀取及寫入本主題中所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: ff2c4cbc-a8d5-4db5-85d4-da3367f27fa0
ms.tgt_platform: multiple
keywords:
- IADsDomain 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsDomain Property Methods
- IADsDomain.AutoUnlockInterval
- IADsDomain.get_AutoUnlockInterval
- IADsDomain.put_AutoUnlockInterval
- IADsDomain.IsWorkgroup
- IADsDomain.get_IsWorkgroup
- IADsDomain.LockoutObservationInterval
- IADsDomain.get_LockoutObservationInterval
- IADsDomain.put_LockoutObservationInterval
- IADsDomain.MinPasswordAge
- IADsDomain.get_MinPasswordAge
- IADsDomain.put_MinPasswordAge
- IADsDomain.MinPasswordLength
- IADsDomain.get_MinPasswordLength
- IADsDomain.put_MinPasswordLength
- IADsDomain.MaxBadPasswordsAllowed
- IADsDomain.get_MaxBadPasswordsAllowed
- IADsDomain.put_MaxBadPasswordsAllowed
- IADsDomain.MaxPasswordAge
- IADsDomain.get_MaxPasswordAge
- IADsDomain.put_MaxPasswordAge
- IADsDomain.PasswordAttributes
- IADsDomain.get_PasswordAttributes
- IADsDomain.put_PasswordAttributes
- IADsDomain.PasswordHistoryLength
- IADsDomain.get_PasswordHistoryLength
- IADsDomain.put_PasswordHistoryLength
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a10c6377c7e97f83046f60d46312a03db68cadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934820"
---
# <a name="iadsdomain-property-methods"></a><span data-ttu-id="4a287-105">IADsDomain 屬性方法</span><span class="sxs-lookup"><span data-stu-id="4a287-105">IADsDomain Property Methods</span></span>

<span data-ttu-id="4a287-106">[**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain)介面方法會讀取及寫入本主題中所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="4a287-106">The [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="4a287-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="4a287-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4a287-108">屬性</span><span class="sxs-lookup"><span data-stu-id="4a287-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="4a287-109">**AutoUnlockInterval**</span><span class="sxs-lookup"><span data-stu-id="4a287-109">**AutoUnlockInterval**</span></span>
<span data-ttu-id="4a287-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4a287-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="4a287-111">指出在自動重新啟用帳戶之前，必須經過的最短時間。</span><span class="sxs-lookup"><span data-stu-id="4a287-111">Indicates the minimum time that must elapse before the account is automatically reenabled.</span></span>

<dt>

<span data-ttu-id="4a287-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4a287-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4a287-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="4a287-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AutoUnlockInterval(
  [out] LONG* plAutoUnlockInterval
);
HRESULT put_AutoUnlockInterval(
  [in] LONG lAutoUnlockInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a287-114">**IsWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="4a287-114">**IsWorkgroup**</span></span>
<span data-ttu-id="4a287-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4a287-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="4a287-116">這個屬性已不會再執行。</span><span class="sxs-lookup"><span data-stu-id="4a287-116">This property is no longer implemented.</span></span>

<dt>

<span data-ttu-id="4a287-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4a287-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a287-118">腳本資料類型： **VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="4a287-118">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsWorkgroup(
  [out] VARIANT_BOOL* retval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a287-119">**LockoutObservationInterval**</span><span class="sxs-lookup"><span data-stu-id="4a287-119">**LockoutObservationInterval**</span></span>
<span data-ttu-id="4a287-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4a287-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="4a287-121">表示在決定是否要鎖定帳戶之前，會監視和累積錯誤密碼計數的時間範圍。例如，如果帳戶的錯誤密碼嘗試次數超過閾值 (在指定期間內允許的錯誤密碼上限)  (鎖定觀察間隔) 帳戶將會被鎖定，方法是在 [登入參數] 屬性集中設定適當的屬性。</span><span class="sxs-lookup"><span data-stu-id="4a287-121">Indicates the time window during which the bad password count is monitored and accumulated before determining whether the account needs to be locked out. For example, if the number of bad password attempts on an account exceed the threshold (Maximum Bad Passwords Allowed) during the specified time period (Lockout Observation Interval) the account will be locked out by setting the appropriate property in the Login Parameter property set.</span></span>

<dt>

<span data-ttu-id="4a287-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4a287-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4a287-123">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="4a287-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockoutObservationInterval(
  [out] LONG* plLockoutObservationInterval
);
HRESULT put_LockoutObservationInterval(
  [in] LONG lLockoutObservationInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a287-124">**MaxBadPasswordsAllowed**</span><span class="sxs-lookup"><span data-stu-id="4a287-124">**MaxBadPasswordsAllowed**</span></span>
<span data-ttu-id="4a287-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4a287-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="4a287-126">指出帳戶鎖定前允許的錯誤密碼登入數目上限。</span><span class="sxs-lookup"><span data-stu-id="4a287-126">Indicates the maximum number of bad password logins allowed before an account lockout.</span></span>

<dt>

<span data-ttu-id="4a287-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4a287-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4a287-128">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="4a287-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxBadPasswordsAllowed(
  [out] LONG* plMaxBadPasswordsAllowed
);
HRESULT put_MaxBadPasswordsAllowed(
  [in] LONG lMaxBadPasswordsAllowed
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a287-129">**MaxPasswordAge**</span><span class="sxs-lookup"><span data-stu-id="4a287-129">**MaxPasswordAge**</span></span>
<span data-ttu-id="4a287-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4a287-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="4a287-131">指出使用者必須變更密碼的最大時間間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4a287-131">Indicates the maximum time interval, in seconds, after which the password must be changed by the user.</span></span>

<dt>

<span data-ttu-id="4a287-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4a287-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4a287-133">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="4a287-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxPasswordAge(
  [out] LONG* plMaxPasswordAge
);
RESULT put_MaxPasswordAge(
  [in] LONG lMaxPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a287-134">**MinPasswordAge**</span><span class="sxs-lookup"><span data-stu-id="4a287-134">**MinPasswordAge**</span></span>
<span data-ttu-id="4a287-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4a287-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="4a287-136">指出密碼可以變更之前的最小時間間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4a287-136">Indicates the minimum time interval, in seconds, before the password can be changed.</span></span>

<dt>

<span data-ttu-id="4a287-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4a287-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4a287-138">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="4a287-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordAge(
  [out] LONG* plMinPasswordAge
);
HRESULT put_MinPasswordAge(
  [in] LONG lMinPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a287-139">**MinPasswordLength**</span><span class="sxs-lookup"><span data-stu-id="4a287-139">**MinPasswordLength**</span></span>
<span data-ttu-id="4a287-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4a287-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="4a287-141">指出密碼必須使用的最小字元數。</span><span class="sxs-lookup"><span data-stu-id="4a287-141">Indicates the minimum number of characters that must be used for a password.</span></span>

<dt>

<span data-ttu-id="4a287-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4a287-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4a287-143">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="4a287-143">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordLength(
  [out] LONG* plMinPasswordLength
);
HRESULT put_MinPasswordLength(
  [in] LONG lMinPasswordLength
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a287-144">**PasswordAttributes**</span><span class="sxs-lookup"><span data-stu-id="4a287-144">**PasswordAttributes**</span></span>
<span data-ttu-id="4a287-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4a287-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="4a287-146">指出密碼的限制，如下列屬性和值清單所定義。</span><span class="sxs-lookup"><span data-stu-id="4a287-146">Indicates restrictions on passwords, as defined by the following list of attributes and values.</span></span>

> [!Note]  
> <span data-ttu-id="4a287-147">針對密碼 \_ ATTR \_ 複雜，密碼必須包含至少一個標點符號或不可列印字元。</span><span class="sxs-lookup"><span data-stu-id="4a287-147">For PASSWORD\_ATTR\_COMPLEX, the password must include at least one punctuation mark or non-printable character.</span></span>

 

<dt>

<span id="PASSWORD_ATTR_NONE"></span><span id="password_attr_none"></span>

<span data-ttu-id="4a287-148">**密碼 \_ATTR \_ 無** (0x00000000) </span><span class="sxs-lookup"><span data-stu-id="4a287-148">**PASSWORD\_ATTR\_NONE** (0x00000000)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_MIXED_CASE"></span><span id="password_attr_mixed_case"></span>

<span data-ttu-id="4a287-149">**密碼 \_ATTR \_ 混合 \_ 案例** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="4a287-149">**PASSWORD\_ATTR\_MIXED\_CASE** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_COMPLEX"></span><span id="password_attr_complex"></span>

<span data-ttu-id="4a287-150">**密碼 \_ATTR \_ 複雜** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="4a287-150">**PASSWORD\_ATTR\_COMPLEX** (0x00000002)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="4a287-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4a287-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4a287-152">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="4a287-152">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordAttributes(
  [out] LONG* plPasswordAttributes
);
HRESULT put_PasswordAttributes(
  [in] LONG lPasswordAttributes
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a287-153">**Msds-passwordhistorylength**</span><span class="sxs-lookup"><span data-stu-id="4a287-153">**PasswordHistoryLength**</span></span>
<span data-ttu-id="4a287-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4a287-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="4a287-155">指出記錄清單中儲存的舊密碼數目。</span><span class="sxs-lookup"><span data-stu-id="4a287-155">Indicates the number of previous passwords saved in the history list.</span></span> <span data-ttu-id="4a287-156">使用者無法重複使用歷程記錄清單中的密碼。</span><span class="sxs-lookup"><span data-stu-id="4a287-156">The user cannot reuse a password in the history list.</span></span>

<dt>

<span data-ttu-id="4a287-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4a287-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4a287-158">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="4a287-158">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordHistoryLength(
  [out] LONG* plPasswordHistoryLength
);
HRESULT put_PasswordHistoryLength(
  [in] LONG lPasswordHistoryLength
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="4a287-159">範例</span><span class="sxs-lookup"><span data-stu-id="4a287-159">Examples</span></span>

<span data-ttu-id="4a287-160">下列程式碼範例會顯示 **msds-passwordhistorylength** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="4a287-160">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```VB
Dim dom As IADsDomain
On Error Resume Next

Set dom = GetObject("WinNT://myDomain")

debug.print "PasswordHistoryLength" & dom.PasswordHistoryLength
```



<span data-ttu-id="4a287-161">下列程式碼範例會顯示 **msds-passwordhistorylength** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="4a287-161">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```C++
LPWSTR adsPath = L"WinNT://myDomain";
LONG nPasswordHistoryLength = 0;

// Bind to the domain object.
hr = ADsGetObject(adsPath,IID_IADsDomain,(void**)&pDomain);
if(FAILED(hr)) {goto Cleanup;}

hr = pDomain->get_PasswordHistoryLength(&nPasswordHistoryLength);
if(FAILED(hr)) {goto Cleanup;}
printf("Password history length: %d",nPasswordHistoryLength);

Cleanup:
    if(pDomain) pDomain->Release();
```



## <a name="requirements"></a><span data-ttu-id="4a287-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a287-162">Requirements</span></span>



| <span data-ttu-id="4a287-163">需求</span><span class="sxs-lookup"><span data-stu-id="4a287-163">Requirement</span></span> | <span data-ttu-id="4a287-164">值</span><span class="sxs-lookup"><span data-stu-id="4a287-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a287-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a287-165">Minimum supported client</span></span><br/> | <span data-ttu-id="4a287-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a287-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a287-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a287-167">Minimum supported server</span></span><br/> | <span data-ttu-id="4a287-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a287-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a287-169">標頭</span><span class="sxs-lookup"><span data-stu-id="4a287-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a287-170"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a287-170"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="4a287-171">DLL</span><span class="sxs-lookup"><span data-stu-id="4a287-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a287-172"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a287-172"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="4a287-173">IID</span><span class="sxs-lookup"><span data-stu-id="4a287-173">IID</span></span><br/>                      | <span data-ttu-id="4a287-174">IID \_ IADsDomain 定義為00E4C220-FD16-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="4a287-174">IID\_IADsDomain is defined as 00E4C220-FD16-11CE-ABC4-02608C9E7553</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="4a287-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a287-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a287-176">**IADsDomain**</span><span class="sxs-lookup"><span data-stu-id="4a287-176">**IADsDomain**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdomain)
</dt> <dt>

[<span data-ttu-id="4a287-177">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="4a287-177">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





