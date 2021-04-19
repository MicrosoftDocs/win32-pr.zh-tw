---
title: 'IWMDRMLicense GetInclusionList 方法 (Wmdrmsdk .h) '
description: GetInclusionList 方法會抓取目前授權或授權鏈的整個包含清單。
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- GetInclusionList 方法 windows Media 格式
- GetInclusionList 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，GetInclusionList 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetInclusionList
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0d2837a4bb84c07214cce3e4fbc3d4d96b9583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986789"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a><span data-ttu-id="1f664-106">IWMDRMLicense：： GetInclusionList 方法</span><span class="sxs-lookup"><span data-stu-id="1f664-106">IWMDRMLicense::GetInclusionList method</span></span>

<span data-ttu-id="1f664-107">**GetInclusionList** 方法會抓取目前授權或授權鏈的整個包含清單。</span><span class="sxs-lookup"><span data-stu-id="1f664-107">The **GetInclusionList** method retrieves the entire inclusion list for the current license or license chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f664-108">語法</span><span class="sxs-lookup"><span data-stu-id="1f664-108">Syntax</span></span>


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a><span data-ttu-id="1f664-109">參數</span><span class="sxs-lookup"><span data-stu-id="1f664-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f664-110">*ppGuids* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1f664-110">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f664-111">接收可識別內含技術的 Guid 陣列。</span><span class="sxs-lookup"><span data-stu-id="1f664-111">Receives an array of GUIDs identifying the included technologies.</span></span>

</dd> <dt>

<span data-ttu-id="1f664-112">*pcGuids* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1f664-112">*pcGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f664-113">接收 *ppGuids* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="1f664-113">Receives the number of elements in the *ppGuids* array.</span></span> <span data-ttu-id="1f664-114">陣列是使用 **CoTaskMemAlloc** 進行配置。</span><span class="sxs-lookup"><span data-stu-id="1f664-114">The array is allocated by using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="1f664-115">完成此清單之後，請呼叫 **CoTaskMemFree** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="1f664-115">When finished with the list, release the memory by calling **CoTaskMemFree**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f664-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f664-116">Return value</span></span>

<span data-ttu-id="1f664-117">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="1f664-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1f664-118">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="1f664-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1f664-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1f664-119">Return code</span></span>                                                                          | <span data-ttu-id="1f664-120">Description</span><span class="sxs-lookup"><span data-stu-id="1f664-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1f664-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1f664-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1f664-122">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="1f664-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f664-123">備註</span><span class="sxs-lookup"><span data-stu-id="1f664-123">Remarks</span></span>

<span data-ttu-id="1f664-124">授權簽發者可以指定可轉換加密內容的其他保護系統。</span><span class="sxs-lookup"><span data-stu-id="1f664-124">The license issuer can specify other protection systems to which the encrypted content may be converted.</span></span> <span data-ttu-id="1f664-125">這個方法所抓取的 Guid 清單會識別允許的保護系統。</span><span class="sxs-lookup"><span data-stu-id="1f664-125">The list of GUIDs retrieved by this method identifies the allowed protection systems.</span></span> <span data-ttu-id="1f664-126">當您輸入 Microsoft 的授權合約以取得存根程式庫時，您將會收到目前支援的保護系統清單，以及用來識別這些系統的 Guid。</span><span class="sxs-lookup"><span data-stu-id="1f664-126">When you enter into a license agreement with Microsoft to get the stub library, you will receive a list of currently supported protection systems and the GUIDs used to identify them.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f664-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f664-127">Requirements</span></span>



| <span data-ttu-id="1f664-128">需求</span><span class="sxs-lookup"><span data-stu-id="1f664-128">Requirement</span></span> | <span data-ttu-id="1f664-129">值</span><span class="sxs-lookup"><span data-stu-id="1f664-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f664-130">標頭</span><span class="sxs-lookup"><span data-stu-id="1f664-130">Header</span></span><br/>  | <dl> <span data-ttu-id="1f664-131"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f664-131"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f664-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="1f664-132">Library</span></span><br/> | <dl> <span data-ttu-id="1f664-133"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f664-133"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f664-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f664-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f664-135">**明確授權和包含清單**</span><span class="sxs-lookup"><span data-stu-id="1f664-135">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="1f664-136">**IWMDRMLicense 介面**</span><span class="sxs-lookup"><span data-stu-id="1f664-136">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





