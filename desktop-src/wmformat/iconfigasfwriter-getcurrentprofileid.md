---
title: IConfigAsfWriter GetCurrentProfileId 方法
description: GetCurrentProfileId 方法會抓取目前的設定檔識別碼。 僅適用于 Windows Media Format 4.0 設定檔的 (。 ) 。
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- GetCurrentProfileId 方法 windows Media 格式
- GetCurrentProfileId 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，GetCurrentProfileId 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967676"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a><span data-ttu-id="42a95-107">IConfigAsfWriter：： GetCurrentProfileId 方法</span><span class="sxs-lookup"><span data-stu-id="42a95-107">IConfigAsfWriter::GetCurrentProfileId method</span></span>

<span data-ttu-id="42a95-108">**GetCurrentProfileId** 方法會抓取目前的設定檔識別碼。</span><span class="sxs-lookup"><span data-stu-id="42a95-108">The **GetCurrentProfileId** method retrieves the current profile ID.</span></span> <span data-ttu-id="42a95-109">僅適用于 Windows Media Format 4.0 設定檔的 (。 ) </span><span class="sxs-lookup"><span data-stu-id="42a95-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="42a95-110">語法</span><span class="sxs-lookup"><span data-stu-id="42a95-110">Syntax</span></span>


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="42a95-111">參數</span><span class="sxs-lookup"><span data-stu-id="42a95-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a95-112">*pdwProfileId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="42a95-112">*pdwProfileId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42a95-113">接收目前設定檔識別碼之 **DWORD** 類型變數的指標。</span><span class="sxs-lookup"><span data-stu-id="42a95-113">Pointer to a variable of type **DWORD** that receives the current profile ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a95-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="42a95-114">Return value</span></span>

<span data-ttu-id="42a95-115">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="42a95-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="42a95-116">如果失敗，則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="42a95-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="42a95-117">備註</span><span class="sxs-lookup"><span data-stu-id="42a95-117">Remarks</span></span>

<span data-ttu-id="42a95-118">此方法現在已過時，因為它採用4.0 版 Windows Media Format SDK 設定檔。</span><span class="sxs-lookup"><span data-stu-id="42a95-118">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="42a95-119">請改用 [**IConfigAsfWriter：： GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) 或 [**IConfigAsfWriter：： GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) ，以正確識別7.0 版和更新版本的設定檔。</span><span class="sxs-lookup"><span data-stu-id="42a95-119">Use [**IConfigAsfWriter::GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) or [**IConfigAsfWriter::GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) instead to correctly identify a profile for version 7.0 and later.</span></span>

## <a name="see-also"></a><span data-ttu-id="42a95-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42a95-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="42a95-121">[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="42a95-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 