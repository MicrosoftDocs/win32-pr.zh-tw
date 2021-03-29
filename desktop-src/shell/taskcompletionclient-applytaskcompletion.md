---
description: 開始工作完成。
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: TaskCompletionClient：： ApplyTaskCompletion 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.ApplyTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 950d96ac46c18d741d5cf2337326f116fb79e36a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991706"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a><span data-ttu-id="12255-103">TaskCompletionClient：： ApplyTaskCompletion 方法</span><span class="sxs-lookup"><span data-stu-id="12255-103">TaskCompletionClient::ApplyTaskCompletion method</span></span>

<span data-ttu-id="12255-104">開始工作完成。</span><span class="sxs-lookup"><span data-stu-id="12255-104">Begins the task completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="12255-105">語法</span><span class="sxs-lookup"><span data-stu-id="12255-105">Syntax</span></span>


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a><span data-ttu-id="12255-106">參數</span><span class="sxs-lookup"><span data-stu-id="12255-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12255-107">*ptcfCategory*</span><span class="sxs-lookup"><span data-stu-id="12255-107">*ptcfCategory*</span></span> 
</dt> <dd>

<span data-ttu-id="12255-108">指出工作類別的值。</span><span class="sxs-lookup"><span data-stu-id="12255-108">A value indicating the category of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12255-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="12255-109">Return value</span></span>

<span data-ttu-id="12255-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="12255-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="12255-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="12255-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="12255-112">備註</span><span class="sxs-lookup"><span data-stu-id="12255-112">Remarks</span></span>

<span data-ttu-id="12255-113">唯一支援的 *ptcfCategory* 值為0x08000000。</span><span class="sxs-lookup"><span data-stu-id="12255-113">The only supported value for *ptcfCategory* is 0x08000000.</span></span>

## <a name="requirements"></a><span data-ttu-id="12255-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="12255-114">Requirements</span></span>



| <span data-ttu-id="12255-115">需求</span><span class="sxs-lookup"><span data-stu-id="12255-115">Requirement</span></span> | <span data-ttu-id="12255-116">值</span><span class="sxs-lookup"><span data-stu-id="12255-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12255-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12255-117">Minimum supported client</span></span><br/> | <span data-ttu-id="12255-118">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12255-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12255-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12255-119">Minimum supported server</span></span><br/> | <span data-ttu-id="12255-120">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12255-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="12255-121">DLL</span><span class="sxs-lookup"><span data-stu-id="12255-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12255-122"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12255-122"><dt>ExecModelClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12255-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12255-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12255-124">**TaskCompletionClient**</span><span class="sxs-lookup"><span data-stu-id="12255-124">**TaskCompletionClient**</span></span>](taskcompletionclient.md)
</dt> </dl>

 

 




