---
description: 更新用戶端的 wizard 框架中的 [上一頁]、[下一頁] 和 [完成] 按鈕。
title: 'WebWizardHost. SetWizardButtons 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: 18af31eac1042e84a41e5651c517279869f03697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973497"
---
# <a name="webwizardhostsetwizardbuttons-method"></a><span data-ttu-id="ae6cb-103">WebWizardHost. SetWizardButtons 方法</span><span class="sxs-lookup"><span data-stu-id="ae6cb-103">WebWizardHost.SetWizardButtons method</span></span>

<span data-ttu-id="ae6cb-104">更新用戶端的 wizard 框架中的 [ **上一頁**]、 **[下一頁**] 和 **[完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ae6cb-104">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae6cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="ae6cb-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a><span data-ttu-id="ae6cb-106">參數</span><span class="sxs-lookup"><span data-stu-id="ae6cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae6cb-107">*vbEnableBack* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae6cb-107">*vbEnableBack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae6cb-108">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ae6cb-108">Type: **Boolean**</span></span>

<span data-ttu-id="ae6cb-109">啟用 [ **上一頁** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ae6cb-109">Enables the **Back** button.</span></span>

</dd> <dt>

<span data-ttu-id="ae6cb-110">*vbEnableNext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae6cb-110">*vbEnableNext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae6cb-111">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ae6cb-111">Type: **Boolean**</span></span>

<span data-ttu-id="ae6cb-112">啟用 [下一步] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ae6cb-112">Enables the **Next** button.</span></span>

</dd> <dt>

<span data-ttu-id="ae6cb-113">*vbLastPage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae6cb-113">*vbLastPage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae6cb-114">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ae6cb-114">Type: **Boolean**</span></span>

<span data-ttu-id="ae6cb-115">啟用 [ **完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ae6cb-115">Enables the **Finish** button.</span></span> <span data-ttu-id="ae6cb-116">指出這是最後一個伺服器端頁面。</span><span class="sxs-lookup"><span data-stu-id="ae6cb-116">States that this is the last server-side page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae6cb-117">備註</span><span class="sxs-lookup"><span data-stu-id="ae6cb-117">Remarks</span></span>

<span data-ttu-id="ae6cb-118">請務必在 OnBack () 和 OnNext () 的每個伺服器端頁面中，執行處理常式函式，這會對應至 wizard 按鈕 **回來** 和 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="ae6cb-118">Be sure to implement handler functions in each server-side page for OnBack() and OnNext(), corresponding to the wizard buttons **Back** and **Next**.</span></span> <span data-ttu-id="ae6cb-119">OnBack () 和 OnNext () 函數會回應 **SetWizardButtons**。</span><span class="sxs-lookup"><span data-stu-id="ae6cb-119">The OnBack() and OnNext() functions respond to **SetWizardButtons**.</span></span> <span data-ttu-id="ae6cb-120">在適當的時間，OnNext () 函式會呼叫 **SetWizardButtons** 和 *vbLastPage* = **true**，以啟用 **[完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ae6cb-120">At the appropriate time, the OnNext() function calls **SetWizardButtons** with *vbLastPage*=**true**, which can enable a **Finish** button.</span></span> <span data-ttu-id="ae6cb-121">OnNext () 也會在使用者按一下 [**完成]** 按鈕時呼叫 [**FinalNext**](iwebwizardhost-finalnext.md) 。</span><span class="sxs-lookup"><span data-stu-id="ae6cb-121">OnNext() also calls [**FinalNext**](iwebwizardhost-finalnext.md) when a user clicks the **Finish** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae6cb-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae6cb-122">Requirements</span></span>



| <span data-ttu-id="ae6cb-123">需求</span><span class="sxs-lookup"><span data-stu-id="ae6cb-123">Requirement</span></span> | <span data-ttu-id="ae6cb-124">值</span><span class="sxs-lookup"><span data-stu-id="ae6cb-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6cb-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae6cb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ae6cb-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae6cb-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ae6cb-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae6cb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ae6cb-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae6cb-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ae6cb-129">標頭</span><span class="sxs-lookup"><span data-stu-id="ae6cb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae6cb-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae6cb-130"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae6cb-131">Idl</span><span class="sxs-lookup"><span data-stu-id="ae6cb-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ae6cb-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ae6cb-132"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




