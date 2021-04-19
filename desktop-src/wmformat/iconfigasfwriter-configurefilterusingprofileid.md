---
title: IConfigAsfWriter ConfigureFilterUsingProfileId 方法
description: ConfigureFilterUsingProfileId 方法會設定篩選器，以從系統組態檔案清單中，使用設定檔識別碼 (識別碼) 索引來寫入 ASF 檔案。 僅適用于 Windows Media Format 4.0 設定檔的 (。 ) 。
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- ConfigureFilterUsingProfileId 方法 windows Media 格式
- ConfigureFilterUsingProfileId 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，ConfigureFilterUsingProfileId 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966463"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a><span data-ttu-id="c7246-107">IConfigAsfWriter：： ConfigureFilterUsingProfileId 方法</span><span class="sxs-lookup"><span data-stu-id="c7246-107">IConfigAsfWriter::ConfigureFilterUsingProfileId method</span></span>

<span data-ttu-id="c7246-108">**ConfigureFilterUsingProfileId** 方法會設定篩選器，以從系統組態檔案清單中，使用設定檔識別碼 (識別碼) 索引來寫入 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="c7246-108">The **ConfigureFilterUsingProfileId** method configures the filter to write an ASF file with a profile identifier (ID) index from the system profile list.</span></span> <span data-ttu-id="c7246-109">僅適用于 Windows Media Format 4.0 設定檔的 (。 ) </span><span class="sxs-lookup"><span data-stu-id="c7246-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="c7246-110">語法</span><span class="sxs-lookup"><span data-stu-id="c7246-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="c7246-111">參數</span><span class="sxs-lookup"><span data-stu-id="c7246-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7246-112">*dwProfileId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7246-112">*dwProfileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7246-113">Windows Media 格式 SDK 4.0 版中所定義的設定檔識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7246-113">Profile ID as defined in version 4.0 of the Windows Media Format SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7246-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7246-114">Return value</span></span>

<span data-ttu-id="c7246-115">傳回下列其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c7246-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="c7246-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c7246-116">Return code</span></span>                                                                                         | <span data-ttu-id="c7246-117">Description</span><span class="sxs-lookup"><span data-stu-id="c7246-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="c7246-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c7246-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="c7246-119">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="c7246-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="c7246-120"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="c7246-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="c7246-121">設定檔無效。</span><span class="sxs-lookup"><span data-stu-id="c7246-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="c7246-122"><dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="c7246-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="c7246-123">篩選圖形已停止。</span><span class="sxs-lookup"><span data-stu-id="c7246-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c7246-124">備註</span><span class="sxs-lookup"><span data-stu-id="c7246-124">Remarks</span></span>

<span data-ttu-id="c7246-125">此方法現在已過時，因為它採用4.0 版 Windows Media Format SDK 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c7246-125">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="c7246-126">若要設定7.0 和更新版本設定檔的篩選，請使用 [**IConfigAsfWriter：： ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) 或 [**IConfigAsfWriter：： ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md)。</span><span class="sxs-lookup"><span data-stu-id="c7246-126">To configure the filter for version 7.0 and later profiles, use [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) or [**IConfigAsfWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c7246-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7246-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7246-128">[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7246-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

