---
description: 設定出現在 wizard 標頭中的標題和副標題。 一般而言，用戶端會將標頭顯示在 HTML 和標題列下方。
title: 'WebWizardHost. SetHeaderText 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: d524f9ae6d1031d518e237d393bbb1dc0d35b2bd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841829"
---
# <a name="webwizardhostsetheadertext-method"></a><span data-ttu-id="40ec0-104">WebWizardHost. SetHeaderText 方法</span><span class="sxs-lookup"><span data-stu-id="40ec0-104">WebWizardHost.SetHeaderText method</span></span>

<span data-ttu-id="40ec0-105">設定出現在 wizard 標頭中的標題和副標題。</span><span class="sxs-lookup"><span data-stu-id="40ec0-105">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="40ec0-106">一般而言，用戶端會將標頭顯示在 HTML 和標題列下方。</span><span class="sxs-lookup"><span data-stu-id="40ec0-106">In general, the client will display the header above the HTML and below the title bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="40ec0-107">語法</span><span class="sxs-lookup"><span data-stu-id="40ec0-107">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a><span data-ttu-id="40ec0-108">參數</span><span class="sxs-lookup"><span data-stu-id="40ec0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40ec0-109">*bstrHeaderTitle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40ec0-109">*bstrHeaderTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40ec0-110">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="40ec0-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="40ec0-111">包含標題的字串。</span><span class="sxs-lookup"><span data-stu-id="40ec0-111">String containing the title.</span></span>

</dd> <dt>

<span data-ttu-id="40ec0-112">*bstrHeaderSubtitle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40ec0-112">*bstrHeaderSubtitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40ec0-113">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="40ec0-113">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="40ec0-114">包含子標題的字串。</span><span class="sxs-lookup"><span data-stu-id="40ec0-114">String containing the subtitle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40ec0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="40ec0-115">Requirements</span></span>



| <span data-ttu-id="40ec0-116">需求</span><span class="sxs-lookup"><span data-stu-id="40ec0-116">Requirement</span></span> | <span data-ttu-id="40ec0-117">值</span><span class="sxs-lookup"><span data-stu-id="40ec0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40ec0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40ec0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="40ec0-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40ec0-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="40ec0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40ec0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="40ec0-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40ec0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="40ec0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="40ec0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="40ec0-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="40ec0-123"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="40ec0-124">Idl</span><span class="sxs-lookup"><span data-stu-id="40ec0-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="40ec0-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="40ec0-125"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 
