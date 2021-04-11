---
title: 'FreeUiInfo 函式 (Ndattributils) '
description: 將內部配置的記憶體解除配置至 UiInfo 結構。
ms.assetid: 41d923fd-2fb3-406e-a5cf-f3ba475685f6
keywords:
- FreeUiInfo 函式 NDF
topic_type:
- apiref
api_name:
- FreeUiInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a96d859faa80e3e2269981d206c96e780d05c37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094235"
---
# <a name="freeuiinfo-function"></a><span data-ttu-id="93ed0-104">FreeUiInfo 函式</span><span class="sxs-lookup"><span data-stu-id="93ed0-104">FreeUiInfo function</span></span>

<span data-ttu-id="93ed0-105">**FreeUiInfo** 函式會將內部配置的記憶體解除配置至 [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)結構。</span><span class="sxs-lookup"><span data-stu-id="93ed0-105">The **FreeUiInfo** function deallocates the memory allocated internally to a [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) structure.</span></span> <span data-ttu-id="93ed0-106">此函數會呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) 來解除配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="93ed0-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="93ed0-107">語法</span><span class="sxs-lookup"><span data-stu-id="93ed0-107">Syntax</span></span>


```C++
VOID FreeUiInfo(
  _In_ UiInfo *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="93ed0-108">參數</span><span class="sxs-lookup"><span data-stu-id="93ed0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93ed0-109">*pInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93ed0-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ed0-110">類型： \**[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="93ed0-110">Type: \**[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)\** _</span></span>

<span data-ttu-id="93ed0-111">結構。</span><span class="sxs-lookup"><span data-stu-id="93ed0-111">The structure.</span></span> <span data-ttu-id="93ed0-112">將會釋放此結構所指向的配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="93ed0-112">The allocated memory pointed to by this structure will be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93ed0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="93ed0-113">Return value</span></span>

<span data-ttu-id="93ed0-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="93ed0-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="93ed0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="93ed0-115">Requirements</span></span>



| <span data-ttu-id="93ed0-116">需求</span><span class="sxs-lookup"><span data-stu-id="93ed0-116">Requirement</span></span> | <span data-ttu-id="93ed0-117">值</span><span class="sxs-lookup"><span data-stu-id="93ed0-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="93ed0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93ed0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="93ed0-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93ed0-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="93ed0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93ed0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="93ed0-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93ed0-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="93ed0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="93ed0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="93ed0-123"><dt>Ndattributils。h</dt></span><span class="sxs-lookup"><span data-stu-id="93ed0-123"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93ed0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93ed0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ed0-125">_ *UiInfo*\*</span><span class="sxs-lookup"><span data-stu-id="93ed0-125">_ *UiInfo*\*</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)
</dt> <dt>

[<span data-ttu-id="93ed0-126">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="93ed0-126">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

