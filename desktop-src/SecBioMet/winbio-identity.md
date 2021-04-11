---
title: 'WINBIO_IDENTITY 結構 (Winbio \_ 類型 .h) '
description: 包含與生物識別範本相關聯的識別值。
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- WINBIO_IDENTITY 結構 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8092754b9107029e0be5800bbd5bc98bc3efb91c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103997"
---
# <a name="winbio_identity-structure"></a><span data-ttu-id="9b6ee-104">WINBIO \_ 識別結構</span><span class="sxs-lookup"><span data-stu-id="9b6ee-104">WINBIO\_IDENTITY structure</span></span>

<span data-ttu-id="9b6ee-105">**WINBIO \_ 識別** 結構包含與生物特徵辨識範本相關聯的識別值。</span><span class="sxs-lookup"><span data-stu-id="9b6ee-105">The **WINBIO\_IDENTITY** structure contains an identifying value associated with a biometric template.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b6ee-106">語法</span><span class="sxs-lookup"><span data-stu-id="9b6ee-106">Syntax</span></span>


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a><span data-ttu-id="9b6ee-107">成員</span><span class="sxs-lookup"><span data-stu-id="9b6ee-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9b6ee-108">**型別**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="9b6ee-109">指定此結構中所包含之身分識別資訊的格式。</span><span class="sxs-lookup"><span data-stu-id="9b6ee-109">Specifies the format of the identity information contained in this structure.</span></span> <span data-ttu-id="9b6ee-110">這個值可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="9b6ee-110">This can be one of the following values:</span></span>



| <span data-ttu-id="9b6ee-111">值</span><span class="sxs-lookup"><span data-stu-id="9b6ee-111">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="9b6ee-112">意義</span><span class="sxs-lookup"><span data-stu-id="9b6ee-112">Meaning</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="9b6ee-113"><dt>**WINBIO \_ 識別碼 \_ 類型 \_ Null**</dt></span><span class="sxs-lookup"><span data-stu-id="9b6ee-113"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="9b6ee-114">範本沒有相關聯的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b6ee-114">The template has no associated ID.</span></span><br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="9b6ee-115"><dt>**WINBIO \_ ID \_ 類型 \_ 萬用字元**</dt></span><span class="sxs-lookup"><span data-stu-id="9b6ee-115"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="9b6ee-116">結構符合所有範本識別。</span><span class="sxs-lookup"><span data-stu-id="9b6ee-116">The structure matches all template identities.</span></span><br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="9b6ee-117"><dt>**WINBIO \_ 識別碼 \_ 類型 \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="9b6ee-117"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="9b6ee-118">結構包含與範本相關聯的 GUID。</span><span class="sxs-lookup"><span data-stu-id="9b6ee-118">The structure contains a GUID associated with the template.</span></span><br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="9b6ee-119"><dt>**WINBIO \_ 識別碼 \_ 類型 \_ SID**</dt></span><span class="sxs-lookup"><span data-stu-id="9b6ee-119"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="9b6ee-120">結構包含與範本相關聯的帳戶 SID。</span><span class="sxs-lookup"><span data-stu-id="9b6ee-120">The structure contains the account SID associated with the template.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9b6ee-121">**值**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-121">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="9b6ee-122">可以包含下列其中一個值的聯集：</span><span class="sxs-lookup"><span data-stu-id="9b6ee-122">A union that can contain one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="9b6ee-123">**Null**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-123">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="9b6ee-124">如果 **類型** 成員是 **WINBIO \_ 識別碼 \_ 型別 \_ 為 Null**，則會包含1。</span><span class="sxs-lookup"><span data-stu-id="9b6ee-124">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9b6ee-125">**通 配 符**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-125">**Wildcard**</span></span>
</dt> <dd>

<span data-ttu-id="9b6ee-126">如果 **類型** 成員是 **WINBIO \_ 識別碼 \_ 類型 \_ 萬用字元**，則包含1。</span><span class="sxs-lookup"><span data-stu-id="9b6ee-126">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_WILDCARD**.</span></span>

</dd> <dt>

<span data-ttu-id="9b6ee-127">**TemplateGuid**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-127">**TemplateGuid**</span></span>
</dt> <dd>

<span data-ttu-id="9b6ee-128">包含128位 GUID 值，如果 **類型** 成員是 **WINBIO \_ 識別碼 \_ 型別 \_ guid**，則會識別範本。</span><span class="sxs-lookup"><span data-stu-id="9b6ee-128">Contains a 128-bit GUID value that identifies the template if the **Type** member is **WINBIO\_ID\_TYPE\_GUID**.</span></span>

</dd> <dt>

<span data-ttu-id="9b6ee-129">**AccountSid**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-129">**AccountSid**</span></span>
</dt> <dd>

<span data-ttu-id="9b6ee-130">結構，如果 **類型** 成員是 **WINBIO \_ 識別碼 \_ 類型 \_ sid**，則包含帳戶 SID。</span><span class="sxs-lookup"><span data-stu-id="9b6ee-130">A structure that contains an account SID if the **Type** member is **WINBIO\_ID\_TYPE\_SID**.</span></span>

<dl> <dt>

<span data-ttu-id="9b6ee-131">**大小**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-131">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="9b6ee-132">SID 中的字元數。</span><span class="sxs-lookup"><span data-stu-id="9b6ee-132">The number of characters in the SID.</span></span>

</dd> <dt>

<span data-ttu-id="9b6ee-133">**資料**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-133">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="9b6ee-134">包含 SID 的不帶正負號字元陣列。</span><span class="sxs-lookup"><span data-stu-id="9b6ee-134">An array of unsigned characters that contain the SID.</span></span> <span data-ttu-id="9b6ee-135">陣列目前的大小上限為68個字元。</span><span class="sxs-lookup"><span data-stu-id="9b6ee-135">The current maximum size of the array is 68 characters.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b6ee-136">備註</span><span class="sxs-lookup"><span data-stu-id="9b6ee-136">Remarks</span></span>

<span data-ttu-id="9b6ee-137">下列函式會使用此結構：</span><span class="sxs-lookup"><span data-stu-id="9b6ee-137">This structure is used in the following functions:</span></span>

-   [<span data-ttu-id="9b6ee-138">**WinBioDeleteTemplate**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-138">**WinBioDeleteTemplate**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [<span data-ttu-id="9b6ee-139">**WinBioEnrollCommit**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-139">**WinBioEnrollCommit**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [<span data-ttu-id="9b6ee-140">**WinBioEnumEnrollments**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-140">**WinBioEnumEnrollments**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [<span data-ttu-id="9b6ee-141">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-141">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [<span data-ttu-id="9b6ee-142">**WinBioIdentify**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-142">**WinBioIdentify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [<span data-ttu-id="9b6ee-143">**WinBioRemoveCredential**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-143">**WinBioRemoveCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [<span data-ttu-id="9b6ee-144">**WinBioVerify**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-144">**WinBioVerify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [<span data-ttu-id="9b6ee-145">**WinBioVerifyWithCallback**</span><span class="sxs-lookup"><span data-stu-id="9b6ee-145">**WinBioVerifyWithCallback**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a><span data-ttu-id="9b6ee-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b6ee-146">Requirements</span></span>



| <span data-ttu-id="9b6ee-147">需求</span><span class="sxs-lookup"><span data-stu-id="9b6ee-147">Requirement</span></span> | <span data-ttu-id="9b6ee-148">值</span><span class="sxs-lookup"><span data-stu-id="9b6ee-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b6ee-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b6ee-149">Minimum supported client</span></span><br/> | <span data-ttu-id="9b6ee-150">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b6ee-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="9b6ee-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b6ee-151">Minimum supported server</span></span><br/> | <span data-ttu-id="9b6ee-152">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b6ee-152">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9b6ee-153">標頭</span><span class="sxs-lookup"><span data-stu-id="9b6ee-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b6ee-154"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9b6ee-154"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b6ee-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b6ee-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b6ee-156">用戶端應用程式結構</span><span class="sxs-lookup"><span data-stu-id="9b6ee-156">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





