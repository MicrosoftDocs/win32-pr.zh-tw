---
description: 模擬 [取消] 按鈕的按一下。
title: 'WebWizardHost. Cancel 方法 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.Cancel
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: ea53c8ad-d6dd-4ff7-92e4-681d807a3d98
ms.openlocfilehash: 79ad23dc0f419e884ad291ab911ddb66d156e1a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026029"
---
# <a name="webwizardhostcancel-method"></a><span data-ttu-id="62bed-103">WebWizardHost. Cancel 方法</span><span class="sxs-lookup"><span data-stu-id="62bed-103">WebWizardHost.Cancel method</span></span>

<span data-ttu-id="62bed-104">模擬 [ **取消** ] 按鈕的按一下。</span><span class="sxs-lookup"><span data-stu-id="62bed-104">Simulates a **Cancel** button click.</span></span>

## <a name="syntax"></a><span data-ttu-id="62bed-105">語法</span><span class="sxs-lookup"><span data-stu-id="62bed-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.Cancel()
```



## <a name="parameters"></a><span data-ttu-id="62bed-106">參數</span><span class="sxs-lookup"><span data-stu-id="62bed-106">Parameters</span></span>

<span data-ttu-id="62bed-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="62bed-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="62bed-108">備註</span><span class="sxs-lookup"><span data-stu-id="62bed-108">Remarks</span></span>

<span data-ttu-id="62bed-109">用戶端會藉由關閉嚮導，負責回應此方法的預期行為。</span><span class="sxs-lookup"><span data-stu-id="62bed-109">The client is responsible for responding to this method with the expected behavior by closing the wizard.</span></span>

## <a name="requirements"></a><span data-ttu-id="62bed-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="62bed-110">Requirements</span></span>



| <span data-ttu-id="62bed-111">需求</span><span class="sxs-lookup"><span data-stu-id="62bed-111">Requirement</span></span> | <span data-ttu-id="62bed-112">值</span><span class="sxs-lookup"><span data-stu-id="62bed-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62bed-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62bed-113">Minimum supported client</span></span><br/> | <span data-ttu-id="62bed-114">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62bed-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="62bed-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62bed-115">Minimum supported server</span></span><br/> | <span data-ttu-id="62bed-116">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62bed-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="62bed-117">標頭</span><span class="sxs-lookup"><span data-stu-id="62bed-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="62bed-118"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="62bed-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="62bed-119">Idl</span><span class="sxs-lookup"><span data-stu-id="62bed-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62bed-120"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="62bed-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




