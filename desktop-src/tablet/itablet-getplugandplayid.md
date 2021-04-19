---
description: 傳回字串，其中包含平板電腦裝置的隨插即用識別碼。
ms.assetid: a0b6619b-f80c-470b-aa3f-f0b30a9dbda8
title: ITablet：： GetPlugAndPlayId 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetPlugAndPlayId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3fb6ce7d59cb29aac4b06b7245bc6246b0688a7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975757"
---
# <a name="itabletgetplugandplayid-method"></a><span data-ttu-id="3de7e-103">ITablet：： GetPlugAndPlayId 方法</span><span class="sxs-lookup"><span data-stu-id="3de7e-103">ITablet::GetPlugAndPlayId method</span></span>

<span data-ttu-id="3de7e-104">傳回字串，其中包含平板電腦裝置的隨插即用識別碼。</span><span class="sxs-lookup"><span data-stu-id="3de7e-104">Returns a string containing the Plug and Play ID for the tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de7e-105">語法</span><span class="sxs-lookup"><span data-stu-id="3de7e-105">Syntax</span></span>


```C++
HRESULT GetPlugAndPlayId(
  [out] LPWSTR *ppwszPPId
);
```



## <a name="parameters"></a><span data-ttu-id="3de7e-106">參數</span><span class="sxs-lookup"><span data-stu-id="3de7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de7e-107">*ppwszPPId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3de7e-107">*ppwszPPId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3de7e-108">字串的指標，包含平板電腦裝置的隨插即用識別碼。</span><span class="sxs-lookup"><span data-stu-id="3de7e-108">Pointer to a string containing the Plug and Play ID for the tablet device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3de7e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3de7e-109">Return value</span></span>

<span data-ttu-id="3de7e-110">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3de7e-110">This method can return one of these values.</span></span>



| <span data-ttu-id="3de7e-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3de7e-111">Return code</span></span>                                                                            | <span data-ttu-id="3de7e-112">Description</span><span class="sxs-lookup"><span data-stu-id="3de7e-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3de7e-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3de7e-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3de7e-114">成功。</span><span class="sxs-lookup"><span data-stu-id="3de7e-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="3de7e-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="3de7e-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3de7e-116">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3de7e-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3de7e-117">備註</span><span class="sxs-lookup"><span data-stu-id="3de7e-117">Remarks</span></span>

<span data-ttu-id="3de7e-118">呼叫端會負責使用 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)釋放從此方法傳回的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3de7e-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="3de7e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3de7e-119">Requirements</span></span>



| <span data-ttu-id="3de7e-120">需求</span><span class="sxs-lookup"><span data-stu-id="3de7e-120">Requirement</span></span> | <span data-ttu-id="3de7e-121">值</span><span class="sxs-lookup"><span data-stu-id="3de7e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3de7e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3de7e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3de7e-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3de7e-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3de7e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3de7e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3de7e-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="3de7e-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3de7e-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="3de7e-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3de7e-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3de7e-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3de7e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3de7e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de7e-129">**ITablet 介面**</span><span class="sxs-lookup"><span data-stu-id="3de7e-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

