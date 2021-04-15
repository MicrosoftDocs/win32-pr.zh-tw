---
title: IConfigAsfWriter ConfigureFilterUsingProfileGuid 方法
description: ConfigureFilterUsingProfileGuid 方法會設定篩選準則，以根據指定的預先定義設定檔來寫入 ASF 檔案。  (已淘汰。 ) 。
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- ConfigureFilterUsingProfileGuid 方法 windows Media 格式
- ConfigureFilterUsingProfileGuid 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，ConfigureFilterUsingProfileGuid 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1521738af4411baa2c11f3d20722e09e2d22a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508072"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a><span data-ttu-id="10922-107">IConfigAsfWriter：： ConfigureFilterUsingProfileGuid 方法</span><span class="sxs-lookup"><span data-stu-id="10922-107">IConfigAsfWriter::ConfigureFilterUsingProfileGuid method</span></span>

<span data-ttu-id="10922-108">**ConfigureFilterUsingProfileGuid** 方法會設定篩選準則，以根據指定的預先定義設定檔來寫入 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="10922-108">The **ConfigureFilterUsingProfileGuid** method configures the filter to write an ASF file based on the specified predefined profile.</span></span> <span data-ttu-id="10922-109">(已取代。)</span><span class="sxs-lookup"><span data-stu-id="10922-109">(Deprecated.)</span></span>

## <a name="syntax"></a><span data-ttu-id="10922-110">語法</span><span class="sxs-lookup"><span data-stu-id="10922-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a><span data-ttu-id="10922-111">參數</span><span class="sxs-lookup"><span data-stu-id="10922-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10922-112">*guidProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="10922-112">*guidProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10922-113">識別設定檔的 **GUID** ，如 Windows MEDIA Format SDK 標頭檔 Wmsysprf 中所定義。</span><span class="sxs-lookup"><span data-stu-id="10922-113">**GUID** identifying a profile as defined in the Windows Media Format SDK header file Wmsysprf.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10922-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="10922-114">Return value</span></span>

<span data-ttu-id="10922-115">傳回下列其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="10922-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="10922-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="10922-116">Return code</span></span>                                                                                         | <span data-ttu-id="10922-117">Description</span><span class="sxs-lookup"><span data-stu-id="10922-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="10922-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="10922-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="10922-119">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="10922-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="10922-120"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="10922-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="10922-121">設定檔無效。</span><span class="sxs-lookup"><span data-stu-id="10922-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="10922-122"><dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="10922-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="10922-123">篩選圖形已停止。</span><span class="sxs-lookup"><span data-stu-id="10922-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="10922-124">備註</span><span class="sxs-lookup"><span data-stu-id="10922-124">Remarks</span></span>

<span data-ttu-id="10922-125">從 Windows Media Format 9 系列 SDK 開始，尚未定義任何新的系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="10922-125">Beginning with the Windows Media Format 9 Series SDK, no new system profiles have been defined.</span></span> <span data-ttu-id="10922-126">只有第8版 (或較早的) 系統設定檔 Guid 可搭配此方法使用。</span><span class="sxs-lookup"><span data-stu-id="10922-126">Only version 8 (or earlier) system profile GUIDs can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="10922-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10922-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="10922-128">[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10922-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

