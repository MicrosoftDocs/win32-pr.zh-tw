---
description: GetFileCapabilities 方法會從目前的檔案抓取檔案功能的清單。
ms.assetid: 0d24efd2-d411-4fb3-95c2-4742a58aeb5e
title: ISCardFileAccess：： GetFileCapabilities 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetFileCapabilities
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca22f02d327cdfbea527fba3a87f3f149774c091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193473"
---
# <a name="iscardfileaccessgetfilecapabilities-method"></a><span data-ttu-id="7ebbb-103">ISCardFileAccess：： GetFileCapabilities 方法</span><span class="sxs-lookup"><span data-stu-id="7ebbb-103">ISCardFileAccess::GetFileCapabilities method</span></span>

<span data-ttu-id="7ebbb-104">\[**GetFileCapabilities** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-104">\[The **GetFileCapabilities** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7ebbb-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7ebbb-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="7ebbb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7ebbb-107">**GetFileCapabilities** 方法會從目前的檔案抓取檔案功能的清單。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-107">The **GetFileCapabilities** method retrieves a list of file capabilities from the current file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ebbb-108">語法</span><span class="sxs-lookup"><span data-stu-id="7ebbb-108">Syntax</span></span>


```C++
HRESULT GetFileCapabilities(
  [in, out] LPTLV_TABLE *ppProperties,
  [in, out] LONG        *plProperties,
  [in]      SCARD_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="7ebbb-109">參數</span><span class="sxs-lookup"><span data-stu-id="7ebbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ebbb-110">*ppProperties* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="7ebbb-110">*ppProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebbb-111"> (標記、長度、值) 結構的 TLV 指標。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-111">Pointer to TLV (tag, length, value) structures.</span></span> <span data-ttu-id="7ebbb-112">在輸入時，這個參數會指出要取得屬性的檔案;在輸出時，此參數包含屬性。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-112">On input, this parameter indicates the files for which to get properties; on output, this parameter contains the properties.</span></span> <span data-ttu-id="7ebbb-113">下列範例是 TLV 結構的定義。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-113">The following example is a definition of the TLV structure.</span></span>


```C++
#include <windows.h>

typedef struct
{
  DWORD  Tag;
  DWORD  Length;
  BYTE[]  Value;
  BOOL  Valid;
} TLV;
```



<span data-ttu-id="7ebbb-114">如需有關 TLV 結構的詳細資訊，請參閱 [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) 。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-114">For more information on TLV structures, see [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/).</span></span>

</dd> <dt>

<span data-ttu-id="7ebbb-115">*plProperties* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="7ebbb-115">*plProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebbb-116">*PpProperties* 中的 TLV 專案數目指標。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-116">Pointer to the number of TLV entries in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="7ebbb-117">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="7ebbb-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebbb-118">指定是否必須使用安全訊息，並預先配置資料。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-118">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="7ebbb-119">**SC \_ FL \_ 安全 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="7ebbb-119">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="7ebbb-120">**SC \_ FL 預先配置 \_**</span><span class="sxs-lookup"><span data-stu-id="7ebbb-120">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ebbb-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ebbb-121">Return value</span></span>

<span data-ttu-id="7ebbb-122">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-122">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7ebbb-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7ebbb-123">Return code</span></span>                                                                                   | <span data-ttu-id="7ebbb-124">Description</span><span class="sxs-lookup"><span data-stu-id="7ebbb-124">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="7ebbb-125"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebbb-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7ebbb-126">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-126">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="7ebbb-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebbb-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7ebbb-128">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-128">Invalid parameter.</span></span><br/>                    |
| <dl> <span data-ttu-id="7ebbb-129"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebbb-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7ebbb-130">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-130">A bad pointer was passed in.</span></span><br/>          |
| <dl> <span data-ttu-id="7ebbb-131"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7ebbb-131"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7ebbb-132">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-132">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="7ebbb-133">備註</span><span class="sxs-lookup"><span data-stu-id="7ebbb-133">Remarks</span></span>

<span data-ttu-id="7ebbb-134">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="7ebbb-135">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7ebbb-136">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="7ebbb-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ebbb-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ebbb-137">Requirements</span></span>



| <span data-ttu-id="7ebbb-138">需求</span><span class="sxs-lookup"><span data-stu-id="7ebbb-138">Requirement</span></span> | <span data-ttu-id="7ebbb-139">值</span><span class="sxs-lookup"><span data-stu-id="7ebbb-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ebbb-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ebbb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="7ebbb-141">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ebbb-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7ebbb-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ebbb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="7ebbb-143">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ebbb-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7ebbb-144">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7ebbb-144">End of client support</span></span><br/>    | <span data-ttu-id="7ebbb-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7ebbb-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="7ebbb-146">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="7ebbb-146">End of server support</span></span><br/>    | <span data-ttu-id="7ebbb-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ebbb-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="7ebbb-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ebbb-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ebbb-149">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="7ebbb-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
