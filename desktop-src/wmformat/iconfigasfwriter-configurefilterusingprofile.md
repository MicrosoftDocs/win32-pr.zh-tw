---
title: IConfigAsfWriter ConfigureFilterUsingProfile 方法
description: ConfigureFilterUsingProfile 方法是設定設定檔的建議方式。 它會根據指定的應用程式定義設定檔，設定篩選來寫入 ASF 檔案。
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- ConfigureFilterUsingProfile 方法 windows Media 格式
- ConfigureFilterUsingProfile 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，ConfigureFilterUsingProfile 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b8d87fbf7e8b2d1d46acf55fe96bfdfef472b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106980278"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a><span data-ttu-id="d4049-107">IConfigAsfWriter：： ConfigureFilterUsingProfile 方法</span><span class="sxs-lookup"><span data-stu-id="d4049-107">IConfigAsfWriter::ConfigureFilterUsingProfile method</span></span>

<span data-ttu-id="d4049-108">**ConfigureFilterUsingProfile** 方法是設定設定檔的建議方式。</span><span class="sxs-lookup"><span data-stu-id="d4049-108">The **ConfigureFilterUsingProfile** method is the recommended way to set a profile.</span></span> <span data-ttu-id="d4049-109">它會根據指定的應用程式定義設定檔，設定篩選來寫入 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="d4049-109">It configures the filter to write an ASF file based on the specified application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4049-110">語法</span><span class="sxs-lookup"><span data-stu-id="d4049-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a><span data-ttu-id="d4049-111">參數</span><span class="sxs-lookup"><span data-stu-id="d4049-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4049-112">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4049-112">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4049-113">應用程式定義設定檔上 [**IWMProfile**](iwmprofile.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d4049-113">Pointer to the [**IWMProfile**](iwmprofile.md) interface on the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4049-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4049-114">Return value</span></span>

<span data-ttu-id="d4049-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d4049-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d4049-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="d4049-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d4049-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d4049-117">Return code</span></span>                                                                                         | <span data-ttu-id="d4049-118">Description</span><span class="sxs-lookup"><span data-stu-id="d4049-118">Description</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="d4049-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d4049-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="d4049-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="d4049-120">The method succeeded.</span></span><br/>                              |
| <dl> <span data-ttu-id="d4049-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d4049-121"><dt>**E\_POINTER**</dt></span></span> </dl>           | <span data-ttu-id="d4049-122">**IWMProfile** 介面指標無效。</span><span class="sxs-lookup"><span data-stu-id="d4049-122">The **IWMProfile** interface pointer is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="d4049-123"><dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="d4049-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="d4049-124">圖形已停止。</span><span class="sxs-lookup"><span data-stu-id="d4049-124">The graph is stopped.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="d4049-125">備註</span><span class="sxs-lookup"><span data-stu-id="d4049-125">Remarks</span></span>

<span data-ttu-id="d4049-126">如果成功，這個方法會導致將 **EC \_ GRAPH \_ 變更** 事件傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="d4049-126">If successful, this method will cause an **EC\_GRAPH\_CHANGED** event to be sent to the application.</span></span> <span data-ttu-id="d4049-127">您可以使用這個方法，利用 Windows Media 格式 SDK 的方法，使用您已 (建立的自訂 Windows Media 9 系列設定檔來設定寫入器，或從現有的 prx 檔案載入該設定檔) 。</span><span class="sxs-lookup"><span data-stu-id="d4049-127">Use this method to configure the writer with a custom Windows Media 9 Series profile you have created (or loaded from an existing .prx file) using the methods of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4049-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4049-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="d4049-129">[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d4049-129">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

